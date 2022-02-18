import time
import board
import adafruit_sht4x

i2c = board.I2C()  # uses board.SCL and board.SDA
sht = adafruit_sht4x.SHT4x(i2c)
print("Found SHT4x with serial number", hex(sht.serial_number))

sht.mode = adafruit_sht4x.Mode.NOHEAT_HIGHPRECISION
# Can also set the mode to enable heater
# sht.mode = adafruit_sht4x.Mode.LOWHEAT_100MS
print("Current mode is: ", adafruit_sht4x.Mode.string[sht.mode])

def main():
    try:
        temperature, relative_humidity = sht.measurements
        print("Temperature: %0.1f C" % temperature)
        print("Humidity: %0.1f %%" % relative_humidity)
    except:
        print('-1 | -1')
if __name__=="__main__":
   main()
