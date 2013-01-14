AC_INIT(gnome-sudoku, 3.7.4)
AM_INIT_AUTOMAKE([1.11 no-dist-gzip dist-xz foreign])
AM_SILENT_RULES([yes])
AM_MAINTAINER_MODE
GNOME_MAINTAINER_MODE_DEFINES

GLIB_GSETTINGS

AM_PATH_PYTHON([2.4],,AC_MSG_ERROR([Python not found]))

dnl ###########################################################################
dnl Dependencies
dnl ###########################################################################

PYGOBJECT_REQUIRED=2.28.3

PKG_CHECK_MODULES(PYGOBJECT, [
    pygobject-3.0 >= $PYGOBJECT_REQUIRED
])

dnl ###########################################################################
dnl Internationalization
dnl ###########################################################################

IT_PROG_INTLTOOL([0.35.0])
AC_SUBST(GETTEXT_PACKAGE, gnome-sudoku)

dnl ###########################################################################
dnl Documentation
dnl ###########################################################################

YELP_HELP_INIT

dnl ###########################################################################
dnl Files to generate
dnl ###########################################################################

AC_OUTPUT([
Makefile
po/Makefile.in
data/Makefile
data/icons/Makefile
data/gnome-sudoku.desktop.in
help/Makefile
src/Makefile
src/lib/Makefile
src/lib/defs.py
src/lib/gtk_goodies/Makefile
])