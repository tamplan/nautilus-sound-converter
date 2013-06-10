gsettingsconvertdir = $(datadir)/GConf/gsettings
gsettingsconvert_DATA = nautilus-sound-converter.convert

gsettingsschema_in_files = org.gnome.Nautilus.SoundConverter.gschema.xml.in
gsettings_SCHEMAS = $(gsettingsschema_in_files:.xml.in=.xml)
.PRECIOUS: $(gsettings_SCHEMAS)
@INTLTOOL_XML_NOMERGE_RULE@
@GSETTINGS_RULES@

builderdir = $(datadir)/nautilus-sound-converter
builder_DATA =		\
	main.ui		\
	progress.ui

profilesdir = $(datadir)/nautilus-sound-converter
dist_profiles_DATA = rhythmbox.gep

EXTRA_DIST =			 \
	$(builder_DATA)		 \
	$(gsettingsconvert_DATA) \
	$(gsettingsschema_in_files)

DISTCLEANFILES =		\
	$(gsettings_SCHEMAS)
