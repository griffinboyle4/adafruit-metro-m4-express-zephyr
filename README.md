# adafruit-metro-m4-express-zephyr
Zephyr RTOS support for the [Adafruit Metro M4 Express board](https://www.adafruit.com/product/3382).

This is intended to be included in a project's west.yml. For example:
```
manifest:
  remotes:
    - name: zephyrproject-rtos
      url-base: https://github.com/zephyrproject-rtos
    - name: fdischner
      url-base: https://github.com/fdischner
  defaults:
    remote: zephyrproject-rtos
  projects:
    - name: zephyr
      remote: zephyrproject-rtos
      revision: v3.1.0
      import: true
    - name: adafruit-metro-m4-express-zephyr
      remote: fdischner
      revision: main
...
```

After a `west update`, the adafruit_metro_m4_express board will be available and sample projects can be built in the usual way:
```
west build -b adafruit_metro_m4_express zephyr/samples/basic/blinky
```
