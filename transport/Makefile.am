## Process this file with automake to produce Makefile.in

AM_CPPFLAGS = \
    -DPACKAGE_LOCALE_DIR=\""$(localedir)"\" \
    -DPACKAGE_SRC_DIR=\""$(srcdir)"\" \
    -DPACKAGE_DATA_DIR=\""$(pkgdatadir)"\" \
    $(GLIB_CFLAGS) \
    $(NICE_CFLAGS) \
    $(GSTREAMER_CFLAGS) \
    $(LIBOPENWEBRTC_CFLAGS) \
    -I$(top_srcdir)/owr

AM_CFLAGS = \
    -Wall \
    -Wextra \
    -Werror \
    $(DEBUG_CFLAGS)

noinst_LTLIBRARIES = libopenwebrtc_transport.la

libopenwebrtc_transport_la_SOURCES = \
    owr_candidate.c \
    owr_payload.c \
    owr_audio_payload.c \
    owr_video_payload.c \
    owr_session.c \
    owr_media_session.c \
    owr_transport_agent.c \
    owr_remote_media_source.c

libopenwebrtc_transport_la_LIBADD = \
    $(NICE_LIBS) \
    $(GSTREAMER_LIBS) \
    $(GLIB_LIBS)

includedir = $(prefix)/include/owr
include_HEADERS = \
    owr_candidate.h \
    owr_payload.h \
    owr_audio_payload.h \
    owr_video_payload.h \
    owr_session.h \
    owr_media_session.h \
    owr_transport_agent.h \
    owr_remote_media_source.h

noinst_HEADERS = \
    owr_candidate_private.h \
    owr_session_private.h \
    owr_media_session_private.h \
    owr_remote_media_source_private.h \
    owr_payload_private.h

-include $(top_srcdir)/git.mk
