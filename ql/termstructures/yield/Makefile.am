
AM_CPPFLAGS = -I${top_srcdir} -I${top_builddir}

this_includedir=${includedir}/${subdir}
this_include_HEADERS = \
    all.hpp \
    bondhelpers.hpp \
    bootstraptraits.hpp \
    discountcurve.hpp \
    drifttermstructure.hpp \
    fittedbonddiscountcurve.hpp \
    flatforward.hpp \
    forwardcurve.hpp \
    forwardspreadedtermstructure.hpp \
    forwardstructure.hpp \
    impliedtermstructure.hpp \
    nonlinearfittingmethods.hpp \
    oisratehelper.hpp \
    piecewiseyieldcurve.hpp \
    piecewisezerospreadedtermstructure.hpp \
    quantotermstructure.hpp \
    ratehelpers.hpp \
    zerocurve.hpp \
    zerospreadedtermstructure.hpp \
    zeroyieldstructure.hpp

libYieldTermStructures_la_SOURCES = \
    bondhelpers.cpp \
    fittedbonddiscountcurve.cpp \
    flatforward.cpp \
    forwardstructure.cpp \
    nonlinearfittingmethods.cpp \
    oisratehelper.cpp \
    ratehelpers.cpp \
    zeroyieldstructure.cpp

noinst_LTLIBRARIES = libYieldTermStructures.la

all.hpp: Makefile.am
	echo "/* This file is automatically generated; do not edit.     */" > $@
	echo "/* Add the files to be included into Makefile.am instead. */" >> $@
	echo >> $@
	for i in $(filter-out all.hpp, $(this_include_HEADERS)); do \
		echo "#include <${subdir}/$$i>" >> $@; \
	done
	echo >> $@
	subdirs='$(SUBDIRS)'; for i in $$subdirs; do \
		echo "#include <${subdir}/$$i/all.hpp>" >> $@; \
	done

