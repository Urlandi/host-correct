# host-correct.ru 

Little bit files for [host-correct.ru](https://host-correct.ru/) private DNS project:

 - [Lighttpd vhost config](host-correct.ru.conf)
 - [Knot Resolver config](kresd.conf)
 - [Munin plugin for Knot Resolver](kresd_munin_)
 - [Default site page](index.htm)

## Munin plugin kresd_munin_

> Original wrote for Unbound server by:
> (C) 2008 W.C.A. Wijngaards.  BSD Licensed.
> and it's source code may be found on 
> [https://github.com/dnstap/unbound/blob/master/contrib/unbound_munin_](https://github.com/dnstap/unbound/blob/master/contrib/unbound_munin_)

Plugin for Munin to monitor usage of Knot Resolver servers built-in stats counters.

### Install

 1. Put the [kresd_munin_](kresd_munin_) file to Munin's source plugins directory, generally `/usr/share/munin/plugins/`.
 1. If need, edit [kresd_munin.conf](kresd_munin.conf) and put it to Munin `plugin-conf.d`, generally `/etc/munin/plugin-conf.d/`.
 1. Create symlinks to [kresd_munin_](kresd_munin_) with `_hits`, `_by_rcode`, `_by_flags` and `_histogram` suffix in Munin's enable plugins directory, generally `/etc/munin/plugins/`.
 1. Restart `munin-node`.

Please view the [source code](kresd_munin_) for take more informations.
  
# DoH and DoT

You can freely use https://host-correct.ru:44353/dns-query in yours browser, such as, in Firefox DoH custom service. DoT service too, as you want. But remember host machine have 512 MByte RAM only, so be carefully and do not hope to miracle.
Please visit https://host-correct.ru/ for more information and views some statistics of server works.