all:						\
	branches-32x32s.png			\
	escher-32x32s.png			\
	furniture-logs-32x32s.png		\
	grass-32x32s.png			\
	interior_walls-32x32s.png		\
	lanterns-32x32s.png			\
	leaves-32x32s.png			\
	moss-cracks-32x32s.png			\
	nox-32x32s.png				\
	tmp-32x32s.png				\
	wood-bridge-32x32s.png			\
	wood-floor-32x32s.png
.PHONY: all

%-32x32s.png: %.kra
	unzip -p $< mergedimage.png >$*-16x16.png.tmp
	convert "PNG:$*-16x16.png.tmp" -sample 200% "PNG:$@.tmp"
	rm $*-16x16.png.tmp
	mv $@.tmp $@

%-32x32s.png: %.png
	convert $< -sample 200% "PNG:$@.tmp"
	mv $@.tmp $@
