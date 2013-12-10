IrSensors Arduino Library
=========================

This library encapsulates the management of 2 or 3 IR reflectance sensors.

All that is required at initialization is the set of pins to which the
IR sensors are connected. If a sensor is not connected, specify -1 as the
pin number.

For example:

    #include <IrSensors.h>

    // Set up the IR Sensors with the following pins:
    // Left - 0
    // Center - 2
    // Right - 1
    IrSensors sensors(0, 2, 1);

    void setup() {
      // Initialize the sensors
      sensors.begin();
    }

    void loop() {
      ...

      // Determine if the left sensor detected a high reflectance
      boolean detected = sensors.highReflectionDetected(IrLeft);

      // Determine if the center sensor detected a lower reflectance
      detected = sensors.lowReflectionDetected(IrCenter);

      ...
    }

