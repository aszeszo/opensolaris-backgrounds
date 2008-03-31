backgrounddir = $(datadir)/pixmaps/backgrounds/opensolaris

background_DATA =\
	BlueSwirl.png \
	GreenSwirl.png \
	OrangeSwirl.png \
	BlueDarkFlare.jpg \
	opensolaris-default.jpg

metadata_in_files = opensolaris-backgrounds.xml.in
metadatadir = $(datadir)/gnome-background-properties
metadata_DATA = $(metadata_in_files:.xml.in=.xml)
@INTLTOOL_XML_RULE@

noinst_DATA = opensolaris-backgrounds.xml.in
CLEANFILES = opensolaris-backgrounds.xml opensolaris-backgrounds.xml.in

EXTRA_DIST = $(background_DATA) opensolaris-backgrounds.xml.in.in

opensolaris-backgrounds.xml.in: opensolaris-backgrounds.xml.in.in Makefile
	sed -e 's^\@datadir\@^$(datadir)^g' < $(srcdir)/opensolaris-backgrounds.xml.in.in > opensolaris-backgrounds.xml.in.tmp \
	&& mv opensolaris-backgrounds.xml.in.tmp opensolaris-backgrounds.xml.in

MAINTAINERCLEANFILES = \
	Makefile.in
