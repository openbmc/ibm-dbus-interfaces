AM_DEFAULT_SOURCE_EXT = .cpp

if WANT_LIBIBM_DBUS
nobase_include_HEADERS = ## These get filled in by Makefile.interfaces

libibm_dbusdir = ${libdir}
libibm_dbus_LTLIBRARIES = libibm_dbus.la
libibm_dbus_la_LDFLAGS = $(SDBUSPLUS_LIBS) -version-info 0:0:0 -shared
libibm_dbus_la_CXXFLAGS = $(SDBUSPLUS_CFLAGS)

BUILT_SOURCES = libibm_dbus.cpp
CLEANFILES = libibm_dbus.cpp

pkgconfiglibdir = ${libdir}/pkgconfig
pkgconfiglib_DATA = ibm-dbus-interfaces.pc

clean-local: clean-dbus

-include Makefile.interfaces
endif

yamldir = ${datadir}/phosphor-dbus-yaml/yaml
nobase_yaml_DATA = ## Filled in by Makefile.yaml

-include Makefile.yaml
