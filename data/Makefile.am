schemasdir	 = $(GCONF_SCHEMA_FILE_DIR)
schemas_in_files = nautilus-sound-converter.schemas.in
schemas_DATA 	 = $(schemas_in_files:.schemas.in=.schemas)
@INTLTOOL_SCHEMAS_RULE@

builderdir = $(datadir)/nautilus-sound-converter
builder_DATA =		\
	main.ui		\
	progress.ui
	
EXTRA_DIST =			\
	$(builder_DATA)		\
	$(schemas_in_files)

DISTCLEANFILES =		\
	$(schemas_DATA)

if GCONF_SCHEMAS_INSTALL
install-data-local:
	        if test -z "$(DESTDIR)" ; then \
	                for p in $(schemas_DATA) ; do \
	                        GCONF_CONFIG_SOURCE=$(GCONF_SCHEMA_CONFIG_SOURCE) $(GCONFTOOL) --makefile-install-rule $(top_builddir)/data/$$p ; \
	                done \
	        fi
else
install-data-local:
endif
