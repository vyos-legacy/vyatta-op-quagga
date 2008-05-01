noinst_SCRIPTS	 = vtysh2templates
opdir		 = $(datadir)/vyatta-op/templates
bin_SCRIPTS	 = scripts/vtyshow.pl

cpiop = find  . ! -regex '\(.*~\|.*\.bak\|.*\.swp\|.*\#.*\#\)' -print0 | \
	cpio -0pd

install-exec-hook:
	mkdir -p $(DESTDIR)$(opdir)
	cd templates; $(cpiop) $(DESTDIR)$(opdir)
