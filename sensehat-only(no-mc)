#from picamera import PiCamera
from time import sleep
#from gpiozero import Button, LED, TrafficLights
import random
from sense_hat import SenseHat, ACTION_PRESSED, ACTION_HELD, ACTION_RELEASED

print("*Pi Minecraft Companion* Connected to Minecraft.")

sense = SenseHat()
#sense.show_message("Hello World!")

r=(255,0,0)
g=(0,255,0)
b=(0,0,255)
w=(255,255,255)
br=(165,42,42)
o=(0,0,0)

sense.clear()
i=0
#fill column one at a time
for i in range(8):
    sense.set_pixel(0,i,g)
    sense.set_pixel(1,i,g)
    sense.set_pixel(2,i,g)
    sense.set_pixel(3,i,g)
    sense.set_pixel(4,i,g)
    sense.set_pixel(5,i,g)
    sense.set_pixel(6,i,g)
    sense.set_pixel(7,i,g)
    sleep(0.2)
    i=i+1

frame1 = [
g,g,g,g,g,g,g,g,
g,b,b,g,g,b,b,g,
g,b,b,g,g,b,b,g,
g,g,g,b,b,g,g,g,
g,g,g,b,b,g,g,g,
g,b,b,b,b,b,b,g,
g,b,b,b,b,b,b,g,
g,g,g,g,g,g,g,g,
]

frame2 = [
g,g,g,g,g,g,g,g,
g,w,w,g,g,w,w,g,
g,w,w,g,g,w,w,g,
g,g,g,w,w,g,g,g,
g,g,g,w,w,g,g,g,
g,w,w,w,w,w,w,g,
g,w,w,w,w,w,w,g,
g,g,g,g,g,g,g,g,
]

diamond = [
w,w,w,b,w,w,w,o,
w,w,b,b,b,w,w,o,
w,b,b,b,b,b,w,o,
b,b,b,b,b,b,b,o,
w,b,b,b,b,b,w,o,
w,w,b,b,b,w,w,o,
w,w,w,b,w,w,w,o,
o,o,o,o,o,o,o,o,
]

tree = [
    w, w, w, g, g, w, w, w,
    w, w, g, g, g, g, w, w,
    w, g, g, g, g, g, g, w,
    w, g, g, g, g, g, g, w,
    w, w, g, br, br, g, w, w,
    w, w, w, br, br, w, w, w,
    w, w, w, br, br, w, w, w,
    w, w, w, br, br, w, w, w,
    ]

pi = [
    w, g, w, g, g, w, g, w,
    w, w, g, g, g, g, w, w,
    w, w, w, g, g, w, w, w,
    w, w, r, r, r, r, w, w,
    w, w, r, r, r, r, w, w,
    w, w, r, r, r, r, w, w,
    w, w, w, r, r, w, w, w,
    w, w, w, r, r, w, w, w,
    
    ]

snowflake1 = [
    b, w, b, w, b, w, b, o,
    w, w, b, w, b, w, w, o,
    b, b, w, w, w, b, b, o,
    w, w, w, w, w, w, w, o,
    b, b, w, w, w, b, b, o,
    w, w, b, w, b, w, w, o,
    b, w, b, w, b, w, b, o,
    o, o, o, o, o, o, o, o,
    ]


snowflake = [
    w, w, b, w, w, b, w, w,
    w, w, w, b, b, w, w, w,
    b, w, w, b, b, w, w, b,
    w, b, b, b, b, b, b, w,
    w, b, b, b, b, b, b, w,
    b, w, w, b, b, w, w, b,
    w, w, w, b, b, w, w, w,
    w, w, b, w, w, b, w, w,
    ]


sense.clear()
#flashing creeper
#while True:
#    sense.set_pixels(frame1)
#    sleep(0.5)
#    sense.set_pixels(frame2)
#    sleep(0.5)

def upMenu(event):
  sense.clear()
  if event.action == ACTION_RELEASED:
    print("*Pi Minecraft Companion* World Cleared")
    sense.set_pixels(frame1)
    #menu item 1

  
def downMenu(event):
  sense.clear()
  if event.action == ACTION_RELEASED:
    sense.set_pixels(snowflake)
    #menu item 2
    sense.stick.direction_middle = downCreate

def downCreate(event):
  if event.action == ACTION_RELEASED:
    print("*Pi Minecraft Companion* Igloo Created.")
    # igloo
 
def rightMenu(event):
  sense.clear()
  if event.action == ACTION_RELEASED:
    sense.set_pixels(diamond)
    #menu item 3
    sense.stick.direction_middle = rightCreate
    
def rightCreate(event):
  if event.action == ACTION_RELEASED:
    print("*Pi Minecraft Companion* Diamond House Created")
    #Build diamond house


def leftMenu(event):
  sense.clear()
  if event.action == ACTION_RELEASED:
    #print("*Pi Minecraft Companion* Tree Created.")
    sense.set_pixels(tree)
    #sense.set_pixels(frame1)
    #menu item 4
    sense.stick.direction_middle = leftCreate

def leftCreate(event):
    if event.action == ACTION_RELEASED:
        print("*Pi Minecraft Companion* Tree Created.")
        sense.set_pixels(tree)
        #sense.set_pixels(frame1)
        #menu item 4

def okSelect(event):
  sense.clear()
  if event.action == ACTION_RELEASED:
    print("*Pi Minecraft Companion* Selected.")
    sense.set_pixels(pi)
  #menu item 1
  
##### Menu System SenseHat Joystick = U,D,L,R or M
sense.stick.direction_up = upMenu
sense.stick.direction_down = downMenu
sense.stick.direction_right = rightMenu
sense.stick.direction_left = leftMenu
#sense.stick.direction_middle = okSelect

while True:
    pass
