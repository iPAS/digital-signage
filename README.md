# Buildroot for RPi

* [Buildroot Basics](https://www.youtube.com/watch?v=yxj8ynXXgbk)
* [WPE: Building full screen web applications for the Raspberry Pi -- 2019](
    https://samdecrock.medium.com/building-web-applications-for-wpe-webkit-using-node-js-3347146013f3)
* [Building WPE WebKit for Raspberry Pi 3 -- 2018](
    https://samdecrock.medium.com/building-wpe-webkit-for-raspberry-pi-3-cdbd7b5cb362)


## Quick Start

In Buildroot directory, available boards can be seen by `ls board`.
Please select one, and configure:
```bash
> make raspberrypi3_wpe_defconfig
```
where additional packages can be selected by `make menuconfig`.

Then, built the project:
```bash
> make -j8
```


## Setup WiFi AP

* https://blog.crysys.hu/2018/06/enabling-wifi-and-converting-the-raspberry-pi-into-a-wifi-ap/


## Note

```bash
> make savedefconfig
```

```bash
> make graph-depends
> make <pkg>-graph-depends
> BR2_GRAPH_OUT=svg make graph-depends
> make graph-build
> make graph-size
```
