######################################################################
# 
######################################################################

BUILDDIR=build


build:
	mkdir $@ 
	for i in */*.asciidoc;     \
	do                         \
		name=$${i##*/};    \
		asciidoc -o- $${i} \
			>$@/$${name%%.asciidoc}.html; \
	done

clean:
	for i in $(BUILDDIR)/*.html; do \
		rm $${i}; done

clean-all:
	rm -rf $(BUILDDIR) 
