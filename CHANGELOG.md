# Changelog

## 1.2.0 (2026-10-28)

- Also matches I2C #4 and #5 of the 800-series PCH (`8086:7F7A`, `7F7B`), which some laptops use for the touchpad. Linux drives them with the same LPSS I2C settings as 7F4C. Tested the same day by Chiledog on an Arrow Lake laptop with its touchpad on 7F7A ([#4](https://github.com/watchthelight-labs/WTLI2CArrowLake/issues/4)): works with the VoodooI2C 2.9.1 release and VoodooI2CHID. The Legion 5 touchpad sits on 7F4C-7F4F.

## 1.1.0 (2026-10-16)

- Controller class changed to `VoodooI2CPCILakeController`, which brings the function out of D3hot through PMCSR before using it. 1.0.0 read `0xffffffff` from every register and the touchpad stayed dead.

## 1.0.0 (2026-10-15)

- First version: VoodooI2C personality for `8086:7F4C` to `7F4F` with the Ice Lake / `bxt_i2c_info` timing values.
