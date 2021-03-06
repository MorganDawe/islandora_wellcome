# Makefile for program source directory in GNU NLS utilities package.
# Copyright (C) 1995, 1996, 1997 by Ulrich Drepper <drepper@gnu.ai.mit.edu>
#
# This file file be copied and used freely without restrictions.  It can
# be used in projects which are not available under the GNU Public License
# but which still want to provide support for the GNU gettext functionality.
# Please note that the actual code is *not* freely available.
#
# - Modified by Owen Taylor <otaylor@redhat.com> to use GETTEXT_PACKAGE
#   instead of PACKAGE and to look for po2tbl in ./ not in intl/
#
# - Modified by jacob berkman <jacob@ximian.com> to install
#   Makefile.in.in and po2tbl.sed.in for use with glib-gettextize

GETTEXT_PACKAGE = vips7.38
PACKAGE = vips
VERSION = 7.38.4

SHELL = /bin/bash


srcdir = .
top_srcdir = ..


prefix = /usr/local
exec_prefix = ${prefix}
datarootdir = ${prefix}/share
datadir = ${datarootdir}
libdir = ${exec_prefix}/lib
localedir = $(libdir)/locale
gnulocaledir = $(datadir)/locale
gettextsrcdir = $(datadir)/glib-2.0/gettext/po
subdir = po

INSTALL = /usr/bin/install -c
INSTALL_DATA = ${INSTALL} -m 644
MKINSTALLDIRS = mkdir -p

CC = gcc -std=gnu99
GENCAT = @GENCAT@
GMSGFMT = /usr/bin/msgfmt
MSGFMT = /usr/bin/msgfmt
MSGFMT_OPTS = -c
XGETTEXT = /usr/bin/xgettext
MSGMERGE = msgmerge

DEFS = -DHAVE_CONFIG_H
CFLAGS = -g -O2
CPPFLAGS = 

INCLUDES = -I.. -I$(top_srcdir)/intl

COMPILE = $(CC) -c $(DEFS) $(INCLUDES) $(CPPFLAGS) $(CFLAGS) $(XCFLAGS)

SOURCES = 
POFILES =  en_GB.po de.po
GMOFILES =  en_GB.gmo de.gmo
DISTFILES = LINGUAS ChangeLog Makefile.in.in POTFILES.in $(GETTEXT_PACKAGE).pot \
$(POFILES) $(GMOFILES) $(SOURCES)

POTFILES = \
	../libvips/arithmetic/abs.c \
	../libvips/arithmetic/hist_find_ndim.c \
	../libvips/arithmetic/complex.c \
	../libvips/arithmetic/invert.c \
	../libvips/arithmetic/multiply.c \
	../libvips/arithmetic/round.c \
	../libvips/arithmetic/subtract.c \
	../libvips/arithmetic/min.c \
	../libvips/arithmetic/unaryconst.c \
	../libvips/arithmetic/project.c \
	../libvips/arithmetic/avg.c \
	../libvips/arithmetic/max.c \
	../libvips/arithmetic/statistic.c \
	../libvips/arithmetic/divide.c \
	../libvips/arithmetic/profile.c \
	../libvips/arithmetic/stats.c \
	../libvips/arithmetic/binary.c \
	../libvips/arithmetic/hist_find_indexed.c \
	../libvips/arithmetic/deviate.c \
	../libvips/arithmetic/relational.c \
	../libvips/arithmetic/measure.c \
	../libvips/arithmetic/remainder.c \
	../libvips/arithmetic/unary.c \
	../libvips/arithmetic/math.c \
	../libvips/arithmetic/arithmetic.c \
	../libvips/arithmetic/hist_find.c \
	../libvips/arithmetic/add.c \
	../libvips/arithmetic/math2.c \
	../libvips/arithmetic/linear.c \
	../libvips/arithmetic/boolean.c \
	../libvips/arithmetic/sign.c \
	../libvips/cimg/cimg_dispatch.c \
	../libvips/colour/scRGB2sRGB.c \
	../libvips/colour/XYZ2scRGB.c \
	../libvips/colour/Lab2XYZ.c \
	../libvips/colour/LCh2Lab.c \
	../libvips/colour/LCh2UCS.c \
	../libvips/colour/dE00.c \
	../libvips/colour/scRGB2XYZ.c \
	../libvips/colour/icc_transform.c \
	../libvips/colour/dECMC.c \
	../libvips/colour/colour.c \
	../libvips/colour/rad2float.c \
	../libvips/colour/sRGB2scRGB.c \
	../libvips/colour/UCS2LCh.c \
	../libvips/colour/Lab2LabQ.c \
	../libvips/colour/colourspace.c \
	../libvips/colour/Lab2LabS.c \
	../libvips/colour/LabS2LabQ.c \
	../libvips/colour/Lab2LCh.c \
	../libvips/colour/Yxy2XYZ.c \
	../libvips/colour/LabQ2sRGB.c \
	../libvips/colour/float2rad.c \
	../libvips/colour/XYZ2Yxy.c \
	../libvips/colour/dE76.c \
	../libvips/colour/XYZ2Lab.c \
	../libvips/colour/LabQ2LabS.c \
	../libvips/colour/LabQ2Lab.c \
	../libvips/colour/LabS2Lab.c \
	../libvips/conversion/rot.c \
	../libvips/conversion/conversion.c \
	../libvips/conversion/grid.c \
	../libvips/conversion/recomb.c \
	../libvips/conversion/falsecolour.c \
	../libvips/conversion/flatten.c \
	../libvips/conversion/replicate.c \
	../libvips/conversion/bandary.c \
	../libvips/conversion/subsample.c \
	../libvips/conversion/cache.c \
	../libvips/conversion/join.c \
	../libvips/conversion/gamma.c \
	../libvips/conversion/rot45.c \
	../libvips/conversion/extract.c \
	../libvips/conversion/wrap.c \
	../libvips/conversion/zoom.c \
	../libvips/conversion/bandbool.c \
	../libvips/conversion/ifthenelse.c \
	../libvips/conversion/tilecache.c \
	../libvips/conversion/flip.c \
	../libvips/conversion/bandjoin.c \
	../libvips/conversion/copy.c \
	../libvips/conversion/cast.c \
	../libvips/conversion/sequential.c \
	../libvips/conversion/embed.c \
	../libvips/conversion/insert.c \
	../libvips/conversion/msb.c \
	../libvips/conversion/bandrank.c \
	../libvips/conversion/bandmean.c \
	../libvips/conversion/scale.c \
	../libvips/convolution/im_aconv.c \
	../libvips/convolution/fastcor.c \
	../libvips/convolution/convsep.c \
	../libvips/convolution/gaussblur.c \
	../libvips/convolution/im_conv.c \
	../libvips/convolution/correlation.c \
	../libvips/convolution/compass.c \
	../libvips/convolution/sharpen.c \
	../libvips/convolution/spcor.c \
	../libvips/convolution/im_aconvsep.c \
	../libvips/convolution/conv.c \
	../libvips/convolution/im_conv_f.c \
	../libvips/convolution/convolution.c \
	../libvips/create/mask.c \
	../libvips/create/other_dispatch.c \
	../libvips/create/zone.c \
	../libvips/create/invertlut.c \
	../libvips/create/mask_gaussian.c \
	../libvips/create/mask_butterworth_band.c \
	../libvips/create/sines.c \
	../libvips/create/black.c \
	../libvips/create/mask_ideal_ring.c \
	../libvips/create/gaussnoise.c \
	../libvips/create/logmat.c \
	../libvips/create/tonelut.c \
	../libvips/create/mask_gaussian_band.c \
	../libvips/create/mask_ideal.c \
	../libvips/create/mask_butterworth_ring.c \
	../libvips/create/create.c \
	../libvips/create/identity.c \
	../libvips/create/eye.c \
	../libvips/create/text.c \
	../libvips/create/gaussmat.c \
	../libvips/create/xyz.c \
	../libvips/create/im_benchmark.c \
	../libvips/create/mask_butterworth.c \
	../libvips/create/mask_gaussian_ring.c \
	../libvips/create/mask_fractal.c \
	../libvips/create/point.c \
	../libvips/create/mask_ideal_band.c \
	../libvips/create/grey.c \
	../libvips/create/fractsurf.c \
	../libvips/create/buildlut.c \
	../libvips/foreign/jpeg2vips.c \
	../libvips/foreign/radiance.c \
	../libvips/foreign/vips2jpeg.c \
	../libvips/foreign/openexrload.c \
	../libvips/foreign/vipssave.c \
	../libvips/foreign/rawsave.c \
	../libvips/foreign/csvsave.c \
	../libvips/foreign/matrixload.c \
	../libvips/foreign/radsave.c \
	../libvips/foreign/rawload.c \
	../libvips/foreign/webpsave.c \
	../libvips/foreign/vips2tiff.c \
	../libvips/foreign/vips2webp.c \
	../libvips/foreign/fits.c \
	../libvips/foreign/matlab.c \
	../libvips/foreign/csvload.c \
	../libvips/foreign/jpegload.c \
	../libvips/foreign/magickload.c \
	../libvips/foreign/webpload.c \
	../libvips/foreign/matload.c \
	../libvips/foreign/tiff2vips.c \
	../libvips/foreign/openexr2vips.c \
	../libvips/foreign/foreign.c \
	../libvips/foreign/webp2vips.c \
	../libvips/foreign/jpegsave.c \
	../libvips/foreign/dzsave.c \
	../libvips/foreign/openslide2vips.c \
	../libvips/foreign/analyze2vips.c \
	../libvips/foreign/ppmsave.c \
	../libvips/foreign/tiffsave.c \
	../libvips/foreign/matrixsave.c \
	../libvips/foreign/fitssave.c \
	../libvips/foreign/csv.c \
	../libvips/foreign/pngload.c \
	../libvips/foreign/fitsload.c \
	../libvips/foreign/vipsload.c \
	../libvips/foreign/vipspng.c \
	../libvips/foreign/tiffload.c \
	../libvips/foreign/magick2vips.c \
	../libvips/foreign/analyzeload.c \
	../libvips/foreign/ppm.c \
	../libvips/foreign/openslideload.c \
	../libvips/foreign/pngsave.c \
	../libvips/foreign/radload.c \
	../libvips/foreign/ppmload.c \
	../libvips/freqfilt/phasecor.c \
	../libvips/freqfilt/fwfft.c \
	../libvips/freqfilt/freqmult.c \
	../libvips/freqfilt/freqfilt.c \
	../libvips/freqfilt/invfft.c \
	../libvips/freqfilt/spectrum.c \
	../libvips/histogram/hist_cum.c \
	../libvips/histogram/hist_norm.c \
	../libvips/histogram/hist_equal.c \
	../libvips/histogram/maplut.c \
	../libvips/histogram/hist_plot.c \
	../libvips/histogram/stdif.c \
	../libvips/histogram/hist_local.c \
	../libvips/histogram/histogram.c \
	../libvips/histogram/hist_match.c \
	../libvips/histogram/hist_unary.c \
	../libvips/histogram/hist_ismonotonic.c \
	../libvips/histogram/percent.c \
	../libvips/inplace/im_draw_smudge.c \
	../libvips/inplace/im_draw_circle.c \
	../libvips/inplace/im_draw_rect.c \
	../libvips/inplace/im_draw_mask.c \
	../libvips/inplace/draw.c \
	../libvips/inplace/im_draw_point.c \
	../libvips/inplace/flood.c \
	../libvips/inplace/im_draw_image.c \
	../libvips/inplace/im_draw_line.c \
	../libvips/inplace/inplace_dispatch.c \
	../libvips/iofuncs/gate.c \
	../libvips/iofuncs/window.c \
	../libvips/iofuncs/base64.c \
	../libvips/iofuncs/type.c \
	../libvips/iofuncs/memory.c \
	../libvips/iofuncs/vips.c \
	../libvips/iofuncs/init.c \
	../libvips/iofuncs/enumtypes.c \
	../libvips/iofuncs/cache.c \
	../libvips/iofuncs/buffer.c \
	../libvips/iofuncs/sinkmemory.c \
	../libvips/iofuncs/rect.c \
	../libvips/iofuncs/buf.c \
	../libvips/iofuncs/system.c \
	../libvips/iofuncs/threadpool.c \
	../libvips/iofuncs/operation.c \
	../libvips/iofuncs/header.c \
	../libvips/iofuncs/vector.c \
	../libvips/iofuncs/semaphore.c \
	../libvips/iofuncs/error.c \
	../libvips/iofuncs/sinkdisc.c \
	../libvips/iofuncs/sink.c \
	../libvips/iofuncs/generate.c \
	../libvips/iofuncs/region.c \
	../libvips/iofuncs/mapfile.c \
	../libvips/iofuncs/image.c \
	../libvips/iofuncs/util.c \
	../libvips/iofuncs/sinkscreen.c \
	../libvips/iofuncs/object.c \
	../libvips/morphology/countlines.c \
	../libvips/morphology/rank.c \
	../libvips/morphology/im_label_regions.c \
	../libvips/morphology/hitmiss.c \
	../libvips/morphology/morphology.c \
	../libvips/morphology/morph.c \
	../libvips/mosaicing/im_tbmosaic.c \
	../libvips/mosaicing/im_avgdxdy.c \
	../libvips/mosaicing/im_tbcalcon.c \
	../libvips/mosaicing/im_tbmerge.c \
	../libvips/mosaicing/im_lrcalcon.c \
	../libvips/mosaicing/im_clinear.c \
	../libvips/mosaicing/im_remosaic.c \
	../libvips/mosaicing/im_maxpos_subpel.c \
	../libvips/mosaicing/im_chkpair.c \
	../libvips/mosaicing/im_initialize.c \
	../libvips/mosaicing/im_align_bands.c \
	../libvips/mosaicing/mosaic1.c \
	../libvips/mosaicing/im_lrmerge.c \
	../libvips/mosaicing/im_lrmosaic.c \
	../libvips/mosaicing/im_improve.c \
	../libvips/mosaicing/mosaicing_dispatch.c \
	../libvips/mosaicing/match.c \
	../libvips/mosaicing/global_balance.c \
	../libvips/resample/interpolate.c \
	../libvips/resample/resample.c \
	../libvips/resample/transform.c \
	../libvips/resample/similarity.c \
	../libvips/resample/shrink.c \
	../libvips/resample/quadratic.c \
	../libvips/resample/affine.c \
	../libvips/video/im_video_test.c \
	../libvips/video/video_dispatch.c \
	../tools/edvips.c \
	../tools/find_mosaic.c \
	../tools/header.c \
	../tools/mergeup.c \
	../tools/vips.c \
	../tools/vipsthumbnail.c \
	../libvipsCC/VDisplay.cc \
	../libvipsCC/VError.cc \
	../libvipsCC/VImage.cc \
	../libvipsCC/vipsc++.cc \
	../libvipsCC/VMask.cc \
	../libvips/cimg/dummy2.cc \
	../libvipsCC/include/vips/VDisplay.h \
	../libvipsCC/include/vips/VError.h \
	../libvipsCC/include/vips/VImage.h \
	../libvipsCC/include/vips/vipsc++.h \
	../libvipsCC/include/vips/vipscpp.h \
	../libvipsCC/include/vips/VMask.h \
	../libvips/include/vips/deprecated.h \
	../libvips/include/vips/conversion.h \
	../libvips/include/vips/vips.h \
	../libvips/include/vips/private.h \
	../libvips/include/vips/vips7compat.h \
	../libvips/include/vips/debug.h \
	../libvips/include/vips/memory.h \
	../libvips/include/vips/operation.h \
	../libvips/include/vips/basic.h \
	../libvips/include/vips/image.h \
	../libvips/include/vips/error.h \
	../libvips/include/vips/internal.h \
	../libvips/include/vips/inlines.h \
	../libvips/include/vips/cimg_funcs.h \
	../libvips/include/vips/dispatch.h \
	../libvips/include/vips/interpolate.h \
	../libvips/include/vips/intl.h \
	../libvips/include/vips/thread.h \
	../libvips/include/vips/resample.h \
	../libvips/include/vips/semaphore.h \
	../libvips/include/vips/gate.h \
	../libvips/include/vips/transform.h \
	../libvips/include/vips/util.h \
	../libvips/include/vips/version.h \
	../libvips/include/vips/morphology.h \
	../libvips/include/vips/generate.h \
	../libvips/include/vips/enumtypes.h \
	../libvips/include/vips/region.h \
	../libvips/include/vips/vector.h \
	../libvips/include/vips/format.h \
	../libvips/include/vips/threadpool.h \
	../libvips/include/vips/colour.h \
	../libvips/include/vips/freqfilt.h \
	../libvips/include/vips/create.h \
	../libvips/include/vips/video.h \
	../libvips/include/vips/type.h \
	../libvips/include/vips/mosaicing.h \
	../libvips/include/vips/almostdeprecated.h \
	../libvips/include/vips/convolution.h \
	../libvips/include/vips/object.h \
	../libvips/include/vips/buf.h \
	../libvips/include/vips/foreign.h \
	../libvips/include/vips/mask.h \
	../libvips/include/vips/histogram.h \
	../libvips/include/vips/header.h \
	../libvips/include/vips/arithmetic.h \
	../libvips/include/vips/rect.h \
	../libvips/include/vips/relational.h \
	../libvips/include/vips/inplace.h \
	../libvips/cimg/cimg.cpp \
	../libvips/resample/vsqbs.cpp \
	../libvips/resample/bicubic.cpp \
	../libvips/resample/lbb.cpp \
	../libvips/resample/nohalo.cpp

CATALOGS =  en_GB.gmo de.gmo
CATOBJEXT = .gmo
INSTOBJEXT = .mo

.SUFFIXES:
.SUFFIXES: .c .o .po .pox .gmo .mo .msg .cat

.c.o:
	$(COMPILE) $<

.po.pox:
	$(MAKE) $(GETTEXT_PACKAGE).pot
	$(MSGMERGE) $< $(srcdir)/$(GETTEXT_PACKAGE).pot -o $*.pox

.po.mo:
	$(MSGFMT) -o $@ $<

.po.gmo:
	$(AM_V_GEN) file=$(srcdir)/`echo $* | sed 's,.*/,,'`.gmo \
	  && rm -f $$file && $(GMSGFMT) $(MSGFMT_OPTS) -o $$file $<

.po.cat:
	sed -f ../intl/po2msg.sed < $< > $*.msg \
	  && rm -f $@ && $(GENCAT) $@ $*.msg


all: all-yes

all-yes: $(CATALOGS)
all-no:

$(srcdir)/$(GETTEXT_PACKAGE).pot: $(POTFILES)
	$(XGETTEXT) --default-domain=$(GETTEXT_PACKAGE) \
	  --msgid-bugs-address='http://bugzilla.gnome.org/enter_bug.cgi?product=glib&keywords=I18N+L10N&component=general' \
	  --add-comments --keyword=_ --keyword=N_ \
	  --keyword=C_:1c,2 \
	  --keyword=NC_:1c,2 \
	  --keyword=g_dcgettext:2 \
	  --keyword=g_dngettext:2,3 \
	  --keyword=g_dpgettext2:2c,3 \
	  --flag=N_:1:pass-c-format \
	  --flag=C_:2:pass-c-format \
	  --flag=NC_:2:pass-c-format \
	  --flag=g_dngettext:2:pass-c-format \
          --flag=g_strdup_printf:1:c-format \
          --flag=g_string_printf:2:c-format \
          --flag=g_string_append_printf:2:c-format \
          --flag=g_error_new:3:c-format \
          --flag=g_set_error:4:c-format \
          --flag=g_markup_printf_escaped:1:c-format \
          --flag=g_log:3:c-format \
          --flag=g_print:1:c-format \
          --flag=g_printerr:1:c-format \
          --flag=g_printf:1:c-format \
          --flag=g_fprintf:2:c-format \
          --flag=g_sprintf:2:c-format \
          --flag=g_snprintf:3:c-format \
          --flag=g_scanner_error:2:c-format \
          --flag=g_scanner_warn:2:c-format \
	  $(POTFILES) \
	&& test ! -f $(GETTEXT_PACKAGE).po \
	   || ( rm -f $(srcdir)/$(GETTEXT_PACKAGE).pot \
		&& mv $(GETTEXT_PACKAGE).po $(srcdir)/$(GETTEXT_PACKAGE).pot )

install: install-exec install-data
install-exec:
install-data: install-data-yes
install-data-no: all
install-data-yes: all
	$(MKINSTALLDIRS) $(DESTDIR)$(datadir); \
	catalogs='$(CATALOGS)'; \
	for cat in $$catalogs; do \
	  cat=`basename $$cat`; \
	  case "$$cat" in \
	    *.gmo) destdir=$(gnulocaledir);; \
	    *)     destdir=$(localedir);; \
	  esac; \
	  lang=`echo $$cat | sed 's/\$(CATOBJEXT)$$//'`; \
	  dir=$(DESTDIR)$$destdir/$$lang/LC_MESSAGES; \
	  $(MKINSTALLDIRS) $$dir; \
	  if test -r $$cat; then \
	    $(INSTALL_DATA) $$cat $$dir/$(GETTEXT_PACKAGE)$(INSTOBJEXT); \
	    echo "installing $$cat as $$dir/$(GETTEXT_PACKAGE)$(INSTOBJEXT)"; \
	  else \
	    $(INSTALL_DATA) $(srcdir)/$$cat $$dir/$(GETTEXT_PACKAGE)$(INSTOBJEXT); \
	    echo "installing $(srcdir)/$$cat as" \
		 "$$dir/$(GETTEXT_PACKAGE)$(INSTOBJEXT)"; \
	  fi; \
	  if test -r $$cat.m; then \
	    $(INSTALL_DATA) $$cat.m $$dir/$(GETTEXT_PACKAGE)$(INSTOBJEXT).m; \
	    echo "installing $$cat.m as $$dir/$(GETTEXT_PACKAGE)$(INSTOBJEXT).m"; \
	  else \
	    if test -r $(srcdir)/$$cat.m ; then \
	      $(INSTALL_DATA) $(srcdir)/$$cat.m \
		$$dir/$(GETTEXT_PACKAGE)$(INSTOBJEXT).m; \
	      echo "installing $(srcdir)/$$cat as" \
		   "$$dir/$(GETTEXT_PACKAGE)$(INSTOBJEXT).m"; \
	    else \
	      true; \
	    fi; \
	  fi; \
	done
	if test "$(PACKAGE)" = "glib"; then \
	  $(MKINSTALLDIRS) $(DESTDIR)$(gettextsrcdir); \
	  $(INSTALL_DATA) $(srcdir)/Makefile.in.in \
			  $(DESTDIR)$(gettextsrcdir)/Makefile.in.in; \
	else \
	  : ; \
	fi

# Define this as empty until I found a useful application.
installcheck:

uninstall:
	catalogs='$(CATALOGS)'; \
	for cat in $$catalogs; do \
	  cat=`basename $$cat`; \
	  lang=`echo $$cat | sed 's/\$(CATOBJEXT)$$//'`; \
	  rm -f $(DESTDIR)$(localedir)/$$lang/LC_MESSAGES/$(GETTEXT_PACKAGE)$(INSTOBJEXT); \
	  rm -f $(DESTDIR)$(localedir)/$$lang/LC_MESSAGES/$(GETTEXT_PACKAGE)$(INSTOBJEXT).m; \
	  rm -f $(DESTDIR)$(gnulocaledir)/$$lang/LC_MESSAGES/$(GETTEXT_PACKAGE)$(INSTOBJEXT); \
	  rm -f $(DESTDIR)$(gnulocaledir)/$$lang/LC_MESSAGES/$(GETTEXT_PACKAGE)$(INSTOBJEXT).m; \
	done
	if test "$(PACKAGE)" = "glib"; then \
	  rm -f $(DESTDIR)$(gettextsrcdir)/Makefile.in.in; \
	fi

check: all

dvi info tags TAGS ID:

mostlyclean:
	rm -f core core.* *.pox $(GETTEXT_PACKAGE).po *.old.po cat-id-tbl.tmp
	rm -fr *.o

clean: mostlyclean

distclean: clean
	rm -f Makefile Makefile.in POTFILES *.mo *.msg *.cat *.cat.m

maintainer-clean: distclean
	@echo "This command is intended for maintainers to use;"
	@echo "it deletes files that may require special tools to rebuild."
	rm -f $(GMOFILES)

distdir = ../$(GETTEXT_PACKAGE)-$(VERSION)/$(subdir)
dist distdir: $(DISTFILES)
	dists="$(DISTFILES)"; \
	for file in $$dists; do \
	  ln $(srcdir)/$$file $(distdir) 2> /dev/null \
	    || cp -p $(srcdir)/$$file $(distdir); \
	done

update-po: Makefile
	$(MAKE) $(GETTEXT_PACKAGE).pot
	tmpdir=`pwd`; \
	cd $(srcdir); \
	catalogs='$(CATALOGS)'; \
	for cat in $$catalogs; do \
	  cat=`basename $$cat`; \
	  lang=`echo $$cat | sed 's/\$(CATOBJEXT)$$//'`; \
	  echo "$$lang:"; \
	  if $(MSGMERGE) $$lang.po $(GETTEXT_PACKAGE).pot -o $$tmpdir/$$lang.new.po; then \
	    if cmp $$lang.po $$tmpdir/$$lang.new.po >/dev/null 2>&1; then \
	      rm -f $$tmpdir/$$lang.new.po; \
            else \
	      if mv -f $$tmpdir/$$lang.new.po $$lang.po; then \
	        :; \
	      else \
	        echo "msgmerge for $$lang.po failed: cannot move $$tmpdir/$$lang.new.po to $$lang.po" 1>&2; \
	        rm -f $$tmpdir/$$lang.new.po; \
	        exit 1; \
	      fi; \
	    fi; \
	  else \
	    echo "msgmerge for $$cat failed!"; \
	    rm -f $$tmpdir/$$lang.new.po; \
	  fi; \
	done

# POTFILES is created from POTFILES.in by stripping comments, empty lines
# and Intltool tags (enclosed in square brackets), and appending a full
# relative path to them
POTFILES: POTFILES.in
	( if test 'x$(srcdir)' != 'x.'; then \
	    posrcprefix='$(top_srcdir)/'; \
	  else \
	    posrcprefix="../"; \
	  fi; \
	  rm -f $@-t $@ \
	    && (sed -e '/^#/d' 						\
		    -e "s/^\[.*\] +//" 					\
		    -e '/^[ 	]*$$/d' 				\
		    -e "s@.*@	$$posrcprefix& \\\\@" < $(srcdir)/$@.in	\
		| sed -e '$$s/\\$$//') > $@-t \
	    && chmod a-w $@-t \
	    && mv $@-t $@ )

Makefile: Makefile.in.in ../config.status POTFILES
	cd .. \
	  && $(SHELL) ./config.status $(subdir)/$@.in

# Tell versions [3.59,3.63) of GNU make not to export all variables.
# Otherwise a system limit (for SysV at least) may be exceeded.
.NOEXPORT:
