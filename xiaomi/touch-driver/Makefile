# SPDX-License-Identifier: GPL-2.0

# Features of the touch panel used on dada
KBUILD_OPTIONS += CONFIG_TRUSTED_TOUCH=1
KBUILD_OPTIONS += CONFIG_TOUCH_THP_SUPPORT=1
KBUILD_OPTIONS += CONFIG_TOUCH_FOD_SUPPORT=1
KBUILD_OPTIONS += CONFIG_TOUCH_SPI_CS_CLK_DELAY=1

all: modules

modules_install:
	$(MAKE) INSTALL_MOD_STRIP=1 -C $(KERNEL_SRC) M=$(M) modules_install

%:
	$(MAKE) -C $(KERNEL_SRC) M=$(M) $@ $(KBUILD_OPTIONS)

clean:
	$(MAKE) -C $(KERNEL_SRC) M=$(M) clean
