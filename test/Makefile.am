INCLUDES = -I$(top_srcdir)
LDADD = ../libvncserver/libvncserver.la ../libvncclient/libvncclient.la @WSOCKLIB@

if HAVE_LIBPTHREAD
BACKGROUND_TEST=blooptest
ENCODINGS_TEST=encodingstest
endif

copyrecttest_LDADD=$(LDADD) -lm

check_PROGRAMS=$(ENCODINGS_TEST) cargstest copyrecttest $(BACKGROUND_TEST) \
	cursortest

test: encodingstest$(EXEEXT) cargstest$(EXEEXT) copyrecttest$(EXEEXT)
	./encodingstest && ./cargstest

