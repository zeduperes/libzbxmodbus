lib_LTLIBRARIES = libzbxmodbus.la
libzbxmodbus_ladir = src
libzbxmodbus_la_HEADERS = \
    datatype.h \
    endianness.h \
    semaphores.h
libzbxmodbus_la_SOURCES = \
	datatype.c \
	endianness.c \
	modbus.c \
	semaphores.c
libzbxmodbus_la_CFLAGS = -I$(top_srcdir)/libmodbus/src

if ZABBIX_2
libzbxmodbus_la_CFLAGS += -I../include/zabbix-2.4
endif
if ZABBIX_3
libzbxmodbus_la_CFLAGS += -I../include/zabbix-3.0
endif
if ZABBIX_3_2
libzbxmodbus_la_CFLAGS += -I../include/zabbix-3.2
endif
libzbxmodbus_la_LIBADD = $(top_srcdir)/libmodbus/src/libmodbus.la
libzbxmodbus_la_LDFLAGS =  \
    -module \
    -shared \
    -avoid-version
