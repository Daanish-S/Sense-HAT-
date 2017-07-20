# Sense-HAT-
#Daanish and Pranav's code for programming the sense hat
from sense_hat import SenseHat
import time
sense = SenseHat()
starttime = time.time()

while True:
  temperature = sense.get_temperature()
  pressure = sense.get_pressure()
  humidity = sense.get_humidity()
  orientation = sense.get_orientation()
  print ("The temperature is %d, the pressure is %d, the humidity is %d") % (temperature, pressure, humidity)
  print ("The pitch is %d, the roll is %d, the yaw is %d") % (orientation['pitch'], orientation['roll'], orientation['yaw'])
  time.sleep(30.0-((time.time()-starttime) % 30.0))
