# Introduction
This repository contains device tree overlays for Torizon.
## Naming
The naming convention for the Device Tree overlays is:
<module>-<carrier board>-<function>-overlay.dts
If the overlay is compatible to several modules no specifier is needed. For example:
<function>-overlay.dts
**Examples:**
colibri-imx7-aster-atmel-mxt-overlay.dts
apalis-imx6-atmel-mxt-overlay.dts
display-lt170410-overlay.dts
## Description
A description of what the device tree overlay does is expected as comment in the overlay file:
```
// Description of what the device tree overlay does

/dts-v1/;
/plugin/;

/ {
};
```
## Compatibiltiy
The compatible root node of the device tree file should list all compatible base device trees. This looks like this:
```
/dts-v1/;
/plugin/;

/ {
	compatible = "toradex,colibri-imx7d-emmc","toradex,apalis_imx6q", "toradex,colibri_imx6dl";
}
```
This allows to filter for compatible device tree files.
