# TYPES OF STM32

## F Series
- Original
- 90nm

## L Series
- Low Power
- 90nm

## U Series
- Low power performance
- 40nm

## H Series
- Highest performance
- 40nm

## G Series
- Budget
- 90nm

## C Series
- Ultra low cost
- Only C0 as of now

## W Series
- Wireless

## MP Series
- Microprocessors
- Not mcu ofc

# CORTEX M Variations

## Cortex M0
- Most basic
- Low Cost

## Cortex M0+
- Most energy efficient
- Smallest core
- Lowest Cost
- Includes Memory Protection Unit (MPU)

## Cortex M3
- Mid point between cost and performance
- Real time processing for cost-constrained applications

## Cortex M4
- Dedicated DSP, optional single precision FPU
- Higher maxc clock speed
- Same performance per MHz as M3

## Cortex M4F
- M4 but with the optional FPU

## Cortex M7
- Twice the performance per MHz as M3/M4
- Optional double precision FPU
- Higher max clock speed

## Cortex M33
- Enhanced security features
- Includes FPU, DSP extension
- 20% greater performance than M4
- uses ARMV8 instruction set as compared to all other which use ARMV7

# WHICH STM32 USES WHICH CORTEX-M PROCESSOR

|STM32|Cortex-M|
|---|---|
|STM32F0|M0 @ 48MHz|
|STM32C0|M0+ @ 48MHz|
|STM32G0|M0+ @ 64MHz|
|STM32L0|M0+ @ 32MHz|
|STM32F1|M3 @ 72MHz|
|STM32F2|M3 @ 120MHz|
|STM32L1|M3 @ 32MHz|
|STM32F3|M4F @ 72MHz|
|STM32F4|M4F @ 180MHz|
|STM32G4|M4F @ 170MHz|
|STM32L4|M4F @ 80MHz|
|STM32L4+|M4F @ 120MHz|
|STM32WL|M4 @ 48MHz + M0+ @ 48MHz - LoRaWAN|
|STM32WB|M4 @ 64MHz + M0+ @ 32MHz - BLE5.4 + ZigBee + Thread|
|STM32WB0|M0+ @ 64MHz - BLE5.3|


> NOTE: There are other STM32s as well but I do not care about them for this project as they would be overkill

# WHICH STM32 TO USE?

## Performance -> F and H Series
- F2/F3 -> F4 -> F7/H5 -> H7 (supports upto 600MHz)

## Power Consumption -> L and U series
- L is the primary low power series
- U5 is a new low-power option that uses 40nm process
- Most of the L series is based on a cortex-M4 core but the L5 and U5 use M33

## Security?
- I am not sure what security means in terms of an mcu but choose any mcu with the Cortex-M33

## Wireless
- STM32WL
    - LoRaWAN
- STM32WB
    - BLE 5.4
    - ZigBee
    - Thread
- STM32WBA
    - BLE 5.4
    - ZigBee
    - Thread
- STM32WB0
    - BLE 5.3

## Camera Interface (720p HD or lower)
- F4
- F7
- H7

## LCD TFT Display Controller
- F4
- F7
- H7

## MIPI-DSI Display Controller
- F4
- F7

## Graphics Accelerator
- F4
- F7
- H7

## Single precision FPU
- F4
- F7
- H5
- H7

## Double precision FPU
- F7
- H7

## External RAM
- F2
- F4
- F7
- H5
- H7

## Low Cost -> C / G series

### C0 (~100rs)
- The cheapest of all STM32s
- Designed to replace simple, low-cost 8/16 bit MCUs

### G Series (100-300rs)
- Next cheapest series of the STM32
