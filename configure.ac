#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.69])
AC_INIT([sim6809], [0.1.1], [gordon@gjcp.net])

AC_CONFIG_SRCDIR([emu/emu6809.c])
AM_CONFIG_HEADER([config.h])
AM_INIT_AUTOMAKE([foreign subdir-objects])

# Checks for programs.
AC_PROG_CC

# Checks for libraries.
PKG_CHECK_MODULES([ALSA], [alsa], [], [AC_MSG_ERROR([*** ALSA lib required.])])
AC_CHECK_LIB([util],[openpty])
# Checks for header files.
AC_CHECK_HEADERS([stdlib.h string.h unistd.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_TYPE_SIZE_T

# Checks for library functions.
AC_FUNC_MALLOC

AC_CONFIG_FILES([Makefile
                 emu/Makefile])
AC_OUTPUT
