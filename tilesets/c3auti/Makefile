all: branches-32x32s.png
.PHONY: all

%-32x32s.png: %.kra
	unzip -p $< mergedimage.png >$*-16x16.png.tmp
	convert "PNG:$*-16x16.png.tmp" -sample 200% "PNG:$@.tmp"
	rm $*-16x16.png.tmp
	mv $@.tmp $@
