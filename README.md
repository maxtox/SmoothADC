# SmoothADC

Arduino library for smooth ADC results

The SmoothADC library helps filtering ADC values when smoother evolution of values is needed (getting rid of pikes for example).
4 values, average on mid ones.

I tried to keep the lib as tiny as possible.

## Example sketch

This example defines A0 & A1 (analog inputs) to be handled by SmoothADC library

Samples every 50ms for A0

Samples every 500us for A1

Every second, the average value from A0 & A1 are sent to serial port

## Functional reference

#### instName.init(Pin, Resolution, Period)
- Init the smoothADC instance instName on pin "Pin" with a sample rate of "Period" with a resolution of "Resolution" (us/ms)

#### instName.serviceADCPin()
- Method to service the ADC pin when module is enabled (should be placed somewhere in the main loop)

#### instName.getADCVal()
- Get the average ADC pin value (should replace usual analogRead)

#### instName.setPin(pin)
- Set ADC pin to service

#### instName.setResolution(resolution)
- Set Resolution of ADC pin to service (us/ms)

#### instName.setPeriod(period)
- Set sample rate of servicing

#### instName.getPin()
- Get the serviced ADC pin

#### instName.getResolution()
- Get the resolution for the serviced ADC pin

#### instName.getPeriod()
- Get the sample rate of the serviced pin

#### instName.enable()
- Enable ADC smoothing module

#### instName.disable()
- Disable ADC smoothing module

#### instName.isEnabled()
- Test if ADC smoothing is enabled

#### instName.isDisabled()
- Test if ADC smoothing is disabled

## Misc

Doxygen doc can be generated for the class using doxyfile.

Feel free to share your thoughts @ xgarmanboziax@gmail.com about:

- issues encountered
- optimisations
- improvements & new functionalities
