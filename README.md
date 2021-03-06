This is a Python interface to the GY80 IMU ("inertial measurement unit") sensor, to be used by the JHU Robotics Club's Raspberry Pi.

The IMU is really a combination of multiple sensors: an accelerometer (measures acceleration), a gyroscope (measures orientation), a magnetometer (measures compass bearing), and a barometer (measures temperature and pressure). We had to write our own I2C interfaces to the magnetometer and gyroscope!

# Notes
* To connect to RPi in Barton: SSH to IP **10.160.199.21** as username **pi**, password **raspberry**.
  Must be connected via ethernet to hopkins network.
  
* To connect IMU to RPi: Use http://pinout.xyz
  
* As specified [here](http://selfbuilt.net/shop/gy-80-inertial-management-unit), the subcomponents of the GY-80 IMU
  are as follows:
    * Gyro -- L3G4200D
    * Accelerometer -- ADXL345
    * Magnetometer -- MC5883L
    * Barometer/Thermometer -- BMP085

## TODO 
* <s>Print out barometer data from the GY-80 using [the Adafruit_Python_BMP package](https://github.com/adafruit/Adafruit_Python_BMP) </s>
* <s>Print out accelerometer data from the GY-80 using [the Adafruit_Python_ADXL package](https://github.com/adafruit/Adafruit_Python_ADXL345)</s>

* <s> Adapt Arduino-targeted code from [this C++ GY-80 repo](https://github.com/Sanderi44/GY-80-IMU-Sensor) to RPi-targeted Python
  code using [this Python GPIO library](https://github.com/adafruit/Adafruit_Python_GPIO)
    * In the case of the accelerometer, [the Adafruit_Python_ADXL package](https://github.com/adafruit/Adafruit_Python_ADXL345) may have done
      all the hard work for us. (*Not sure--need to take a closer look at the code -- Matt*)
    * Likewise for the barometer/thermometer and [the Adafruit_Python_BMP package](https://github.com/adafruit/Adafruit_Python_BMP) </s>
    
* <s> Wrap everything in a "GY80" Python module with the following functions. Make sure to convert to metric units.
    * getTemperature()
    * getAcceleration()
    * getOrientation() </s>

* Convert GY80 module's output to metric units.
