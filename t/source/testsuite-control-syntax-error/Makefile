name = testsuite-control-syntax-error
dir  = $(name)-1.0

all:
	mkdir $(dir)
	mkdir $(dir)/debian
	cp changelog copyright control rules $(dir)/debian/
	echo 7 > $(dir)/debian/compat
	mkdir $(dir)/debian/source
	echo 1.0 > $(dir)/debian/source/format
	mkdir $(dir)/debian/tests
	echo "Random file" > $(dir)/debian/tests/control
	tar cfz $(name)_1.tar.gz $(dir)
	subst-dsc $(name)_1.tar.gz < dsc.in > $(name)_1.dsc

clean:
	rm -rf $(dir)
	rm -f $(name)_*
