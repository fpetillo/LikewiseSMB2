SUBDIRS = lib tools ticketcopy

bundledir=$(libdir)/SecurityAgentPlugins/com.likewise.bundle
contentsdir=$(bundledir)/Contents
macosdir = $(contentsdir)/MacOS

macos_LTLIBRARIES = com.likewise.la
contents_DATA = Info.plist

AM_CFLAGS=@AM_CFLAGS@ \
	-Wno-unknown-pragmas \
	-pipe -fno-common -fpascal-strings -Wno-four-char-constants \
	-Wall -Werror -mmacosx-version-min=10.4

INFO=Info.plist

com_likewise_la_SOURCES = \
	AuthPlugin.c

com_likewise_la_CFLAGS = $(AM_CFLAGS)

com_likewise_la_CPPFLAGS = @AM_CPPFLAGS@

com_likewise_la_LDFLAGS = \
     -module -shrext '' -avoid-version

com_likewise_la_LIBADD = \
    @top_builddir@/interop/lwauthplugin/lib/libauthplugin.la

Info.plist: Info.plist.in
	$(srcdir)/../dsplugin/process-info-plist.pl -v $(MAIN_VERSION) \
	    -o "$@" $(srcdir)/Info.plist.in
