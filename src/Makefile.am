lib_LTLIBRARIES = libzfl.la

pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = libzfl.pc

include_HEADERS = \
    ../include/zfl.h \
    ../include/zfl_prelude.h \
    ../include/zfl_base.h \
    ../include/zfl_blob.h \
    ../include/zfl_config.h \
    ../include/zfl_hash.h \
    ../include/zfl_list.h \
    ../include/zfl_msg.h \
    ../include/zfl_rpc.h \
    ../include/zfl_rpcd.h \
    ../include/zfl_tree.h \
    ../include/zfl_tree_json.h \
    ../include/zfl_tree_zpl.h

libzfl_la_SOURCES = \
    zfl_base.c \
    zfl_blob.c \
    zfl_config.c \
    zfl_hash.c \
    zfl_list.c \
    zfl_msg.c \
    zfl_rpc.c \
    zfl_rpcd.c \
    zfl_tree.c \
    zfl_tree_json.c \
    zfl_tree_zpl.c

INCLUDES = -I$(top_srcdir)/include
bin_PROGRAMS = zfl_selftest
zfl_selftest_LDADD = $(top_builddir)/src/libzfl.la
zfl_selftest_SOURCES = zfl_selftest.c

if ON_MINGW
libzfl_la_LDFLAGS = -no-undefined -avoid-version -version-info @LTVER@ @LIBZFL_EXTRA_LDFLAGS@
else
libzfl_la_LDFLAGS = -version-info @LTVER@ @LIBZFL_EXTRA_LDFLAGS@
endif

