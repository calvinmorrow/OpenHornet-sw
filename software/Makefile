ABSIS := $(wildcard ABSIS/**)

all: $(ABSIS)

$(ABSIS):
	$(MAKE) -C $@ $(MAKECMDGOALS)

.PHONY: all $(ABSIS)
