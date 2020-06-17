
BUILT_SOURCES = cst_parser.h
AM_YFLAGS = -d

bin_PROGRAMS = cst \
			   srk_tool


cst_SOURCES = cst.c \
			  acst.c \
			  openssl_helper.c \
			  adapt_layer_openssl.c \
		      csf_cmd_aut_dat.c \
		      csf_cmd_ins_key.c \
			  csf_cmd_misc.c \
			  err.c \
			  pkey.c \
			  ssl_wrapper.c \
		  	  srk_helper.c \
			  cst_parser.y \
			  cst_lexer.l

cst_CFLAGS = -I $(top_srcdir)/include/ \
			 -I $(top_buildir)/ \
				-DREMOVE_ENCRYPTION \
				-std=c99 \
				-fPIC \
				-m64 \
				-D_POSIX_C_SOURCE=200809L \
				$(OPENSSL_CFLAGS)

cst_LDADD = $(OPENSSL_LIBS)

srk_tool_SOURCES = srktool.c \
				   srk_helper.c \
				   openssl_helper.c

srk_tool_CFLAGS = -I $(top_srcdir)/include/ \
				-DREMOVE_ENCRYPTION \
				$(OPENSSL_CFLAGS)

srk_tool_LDADD = $(OPENSSL_LIBS)

EXTRA_DIST = LICENSE README.rst

ACLOCAL_AMFLAGS = -I m4
