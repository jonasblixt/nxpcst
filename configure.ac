dnl Bit Packer

AC_PREREQ(2.59)
AC_INIT([cst], [3.3.0], [Jonas Blixt, <jonpe960@gmail.com>])

m4_pattern_forbid([^AX_(CHECK_ENABLE_DEBUG|CODE_COVERAGE|COMPILER_FLAGS|COMPILER_FLAGS_(CFLAGS|CXXFLAGS|LDFLAGS))\b],
  [Unexpanded AX_ macro found. Please install GNU autoconf-archive])

AC_CONFIG_AUX_DIR([build-aux])
AC_CONFIG_MACRO_DIR([m4])

AC_CANONICAL_SYSTEM
AM_INIT_AUTOMAKE([foreign -Wall -Werror subdir-objects])
AM_PROG_AR
AC_PROG_CC
AM_PROG_LEX
AC_PROG_YACC

PKG_CHECK_MODULES(OPENSSL, [openssl >= 1.1.0])
AC_SUBST(OPENSSL_CFLAGS)
AC_SUBST(OPENSSL_LDFLAGS)
AC_SUBST(OPENSSL_LIBS)

dnl this allows us specify individual liking flags for each target
AM_PROG_CC_C_O

AC_CONFIG_FILES([Makefile])

AC_OUTPUT
