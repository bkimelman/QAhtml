AUTOMAKE_OPTIONS = foreign

AM_CPPFLAGS = \
  -I$(includedir) \
  -isystem$(OFFLINE_MAIN)/include \
  -isystem$(OFFLINE_MAIN)/rootmacros \
  -isystem$(ROOTSYS)/include 

lib_LTLIBRARIES = \
  libqadrawtpclasers.la

libqadrawtpclasers_la_LIBADD = \
  -L$(libdir) \
  -L$(OFFLINE_MAIN)/lib \
  -lqadrawclient \
  -lqadrawdb

tpclasersincludedir=$(pkgincludedir)/tpclasers

tpclasersinclude_HEADERS = \
  TPCLasersDraw.h

libqadrawtpclasers_la_SOURCES = \
  TPCLasersDraw.cc

noinst_PROGRAMS = \
  testexternals

testexternals_SOURCES = \
  testexternals.cc

testexternals_LDADD = \
  libqadrawtpclasers.la

testexternals.cc:
	echo "//*** this is a generated file. Do not commit, do not edit" > $@
	echo "int main()" >> $@
	echo "{" >> $@
	echo "  return 0;" >> $@
	echo "}" >> $@

clean-local:
	rm -f $(BUILT_SOURCES)
