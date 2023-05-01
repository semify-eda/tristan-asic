# Tristan Project

Custom instructions for the CV32E40X on an ASIC using SKY130.

# Hardening

First clone all submodules:

	git submodule update --init --recursive

Next build the preprocessed design in `tristan/`:

	make preprocessed.v

Add the power pins manually to the preprocessed.v:

```
`ifdef USE_POWER_PINS
    inout vccd1,	// User area 1 1.8V supply
    inout vssd1,	// User area 1 digital ground
`endif
```

Inside the root harden the macros:

	make cv32e40x

# SoC

TBD Planned SoC

![block_diagram.png](img/block_diagram.png)