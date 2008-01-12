noinst_SCRIPTS	 = vtysh2templates
opdir		 = $(datadir)/vyatta-op/templates

cpiop = find  . ! -regex '\(.*~\|.*\.bak\|.*\.swp\|.*\#.*\#\)' -print0 | \
	cpio -0pd

install-exec-hook:
	mkdir -p $(DESTDIR)$(opdir)
	cd templates; $(cpiop) $(DESTDIR)$(opdir)
	chmod 000 templates/clear/ipv6
	chmod 000 templates/debug/isis
	chmod 000 templates/debug/ospf6
	chmod 000 templates/debug/ripng
	chmod 000 templates/no/debug/isis
	chmod 000 templates/no/debug/ospf6
	chmod 000 templates/no/debug/ripng
	chmod 000 templates/show/clns
	chmod 000 templates/show/ipv6
	chmod 000 templates/show/isis
	chmod 000 templates/show/mpls-te
