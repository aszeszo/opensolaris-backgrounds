backgrounddir = $(datadir)/pixmaps/backgrounds/opensolaris

background_DATA =\
	BlueSwirl.png \
	GreenSwirl.png \
	OrangeSwirl.png \
	indiana-default.png

metadata_in_files = indiana-backgrounds.xml.in
metadatadir = $(datadir)/gnome-background-properties
metadata_DATA = $(metadata_in_files:.xml.in=.xml)
@INTLTOOL_XML_RULE@

noinst_DATA = indiana-backgrounds.xml.in
CLEANFILES = indiana-backgrounds.xml indiana-backgrounds.xml.in

EXTRA_DIST = $(background_DATA) indiana-backgrounds.xml.in.in

indiana-backgrounds.xml.in: indiana-backgrounds.xml.in.in Makefile
	sed -e 's^\@datadir\@^$(datadir)^g' < $(srcdir)/indiana-backgrounds.xml.in.in > indiana-backgrounds.xml.in.tmp \
	&& mv indiana-backgrounds.xml.in.tmp indiana-backgrounds.xml.in

MAINTAINERCLEANFILES = \
	Makefile.in
