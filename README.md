# Zest_Battery_LiPo

Zest_Battery_LiPo shield support for Zephyr OS.

## Usage

This board enables the following component:

- [Maxim MAX17201](https://www.maximintegrated.com/en/products/power/battery-management/MAX17201.html/storefront/storefront.html) Fuel Gauge.

:bulb: This driver should also be added to your workspace:

- [Maxim MAX17201 driver](https://github.com/catie-aq/zephyr_maxim-max17201).

:pushpin: This shield defines:

- a fuel gauge device: `max17201_zest_battery_lipo_<port>`

:triangular_ruler: To use this shield:

- Update your device tree by adding the `ZEST_BATTERY_LIPO(port)` macro to the `app.overlay` file.\
  Replace `port` with the number of the Zest_Core port to which the shield is connected, e.g.:

  ```c
  ZEST_BATTERY_LIPO(1) /* Zest_Battery_LiPo connected to Zest_Core first port */
  ```

- Activate support for the shield by adding `--shield zest_battery_lipo` to the west command.
