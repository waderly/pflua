PATH := ../deps/luajit/usr/local/bin:$(PATH)

EXAMPLES = \
	tcp-port-80.md \
	icmp-or-tcp-or-udp.md \
	portrange-0-6000.md \
	host-127.0.0.1.md \
	net-127.0.0.0-8.md

PFLUA = \
	../src/pf.lua \
	../src/pf/bpf.lua \
	../src/pf/parse.lua \
	../src/pf/expand.lua \
	../src/pf/optimize.lua \
	../src/pf/codegen.lua

all: $(EXAMPLES)

maintainer-clean:
	rm -f $(EXAMPLES)

tcp-port-80.md: $(PFLUA)
	../tools/dump-markdown "tcp port 80" > $@.tmp && mv $@.tmp $@

icmp-or-tcp-or-udp.md: $(PFLUA)
	../tools/dump-markdown "icmp or tcp or udp" > $@.tmp && mv $@.tmp $@

portrange-0-6000.md: $(PFLUA)
	../tools/dump-markdown "portrange 0-6000" > $@.tmp && mv $@.tmp $@

host-127.0.0.1.md: $(PFLUA)
	../tools/dump-markdown "host 127.0.0.1" > $@.tmp && mv $@.tmp $@

net-127.0.0.0-8.md: $(PFLUA)
	../tools/dump-markdown "net 127.0.0.0/8" > $@.tmp && mv $@.tmp $@
