# -*- makefile -*-
# Copyright (c) 2008-2020 Cisco Systems, Inc.  All rights reserved.
# Copyright (c) 2008      Sun Microsystems, Inc.  All rights reserved.
# Copyright (c) 2019      Intel, Inc.  All rights reserved.
# Copyright (c) 2021      Nanook Consulting.  All rights reserved.
# $COPYRIGHT$
#
# Additional copyrights may follow
#
# $HEADER$
#

MD2NROFF = $(PMIX_TOP_SRCDIR)/config/md2nroff.pl

docfiles = \
    src/pattrs.1    \
    src/pevent.1    \
    src/plookup.1   \
    src/pmixcc.1    \
    src/pps.1       \
    src/pquery.1

man_MANS = $(docfiles)

%.1: %.1.md
	$(PMIX_V_GEN) $(MD2NROFF) --source=$< --dest=$@ --pandoc=$(PANDOC)

# A little verbosity magic; "make" will show the terse output.  "make
# V=1" will show the actual commands used (just like the other
# Automake-generated compilation/linker rules).
V=0

PMIX_V_LN_S = $(pmix__v_LN_S_$V)
pmix__v_LN_S_ = $(pmix__v_LN_S_$AM_DEFAULT_VERBOSITY)
pmix__v_LN_S_0 = @echo "  LN_S    " `basename $@`;

PMIX_V_MKDIR = $(pmix__v_MKDIR_$V)
pmix__v_MKDIR_ = $(pmix__v_MKDIR_$AM_DEFAULT_VERBOSITY)
pmix__v_MKDIR_0 = @echo "  MKDIR   " $@;

PMIX_V_GEN = $(pmix__v_GEN_$V)
pmix__v_GEN_ = $(pmix__v_GEN_$AM_DEFAULT_VERBOSITY)
pmix__v_GEN_0 = @echo "  GENERATE" $@;
