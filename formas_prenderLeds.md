// Forma 1/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
from machine import Pin as pin
from utime import sleep, sleep_ms

led1=pin(15,pin.OUT)
led2=pin(2,pin.OUT)
led3=pin(4,pin.OUT)
led4=pin(16,pin.OUT)
led5=pin(5,pin.OUT)
led6=pin(18,pin.OUT)
led7=pin(19,pin.OUT)
led8=pin(21,pin.OUT)
led9=pin(22,pin.OUT)
led10=pin(23,pin.OUT)
pausa=0.2

while True:
  led1.value(1)
  sleep(pausa)
  led1.value(0)
  sleep(pausa)
  
  led2.value(1)
  sleep(pausa)
  led2.value(0)
  sleep(pausa)
  
  led3.value(1)
  sleep(pausa)
  led3.value(0)
  sleep(pausa)
  
  led4.value(1)
  sleep(pausa)
  led4.value(0)
  sleep(pausa)

  led5.value(1)
  sleep(pausa)
  led5.value(0)
  sleep(pausa)

  led6.value(1)
  sleep(pausa)
  led6.value(0)
  sleep(pausa)
  
  led7.value(1)
  sleep(pausa)
  led7.value(0)
  sleep(pausa)

  led8.value(1)
  sleep(pausa)
  led8.value(0)
  sleep(pausa)

  led9.value(1)
  sleep(pausa)
  led9.value(0)
  sleep(pausa)

  led10.value(1)
  sleep(pausa)
  led10.value(0)
  sleep(pausa)
  
// Forma 2//////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

from machine import Pin as pin
from utime import sleep as pausa, sleep_ms as pausam, sleep_us as pausau

leda=pin(15,pin.OUT)
ledb=pin(2,pin.OUT)
ledc=pin(4,pin.OUT)
ledd=pin(16,pin.OUT)
lede=pin(5,pin.OUT)
ledf=pin(18,pin.OUT)
ledg=pin(19,pin.OUT)
ledh=pin(21,pin.OUT)
ledi=pin(22,pin.OUT)
ledj=pin(23,pin.OUT)

def print_led(a, b, c, d, e, f, g, h, i, j):
  leda.value(a)
  ledb.value(b)
  ledc.value(c)
  ledd.value(d)
  lede.value(e)
  ledf.value(f)
  ledg.value(g)
  ledh.value(h)
  ledi.value(i)
  ledj.value(j)
  pausam(300)

while True:
  print_led(0,0,0,0,0,0,0,0,0,0)
  print_led(0,0,0,0,0,0,0,0,0,1)  
  print_led(0,0,0,0,0,0,0,0,1,0)
  print_led(0,0,0,0,0,0,0,1,0,0)
  print_led(0,0,0,0,0,0,1,0,0,0)
  print_led(0,0,0,0,0,1,0,0,0,0)
  print_led(0,0,0,0,1,0,0,0,0,0)
  print_led(0,0,0,1,0,0,0,0,0,0)
  print_led(0,0,1,0,0,0,0,0,0,0)
  print_led(0,1,0,0,0,0,0,0,0,0)
  print_led(1,0,0,0,0,0,0,0,0,0)
  
// Forma 3////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

from machine import Pin 
import utime
led1=Pin(15,Pin.OUT)
led2=Pin(2,Pin.OUT)
led3=Pin(4,Pin.OUT)
led4=Pin(16,Pin.OUT)
led5=Pin(5,Pin.OUT)
led6=Pin(18,Pin.OUT)
led7=Pin(19,Pin.OUT)
led8=Pin(21,Pin.OUT)
led9=Pin(22,Pin.OUT)
led10=Pin(23,Pin.OUT)

todos =  [led1, led2, led3, led4, led5, led6, led7, led8, led9, led10]
def derecha():
  for elemento in todos:
    elemento.value(1)
    utime.sleep_ms(50)
    elemento.value(0)
    utime.sleep(0.05)
def izquierda():
  for elemento in reversed(todos):
    elemento.value(1)
    utime.sleep(0.05)
    elemento.value(0)
    utime.sleep(0.05)

while True:
  derecha()
  izquierda()
  
// Forma 4/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

from machine import Pin as pin
from utime import sleep as pausa, sleep_ms as pausam, sleep_us as pausau

leda=pin(15,pin.OUT)
ledb=pin(2,pin.OUT)
ledc=pin(4,pin.OUT)
ledd=pin(16,pin.OUT)
lede=pin(5,pin.OUT)
ledf=pin(18,pin.OUT)
ledg=pin(19,pin.OUT)
ledh=pin(21,pin.OUT)
ledi=pin(22,pin.OUT)
ledj=pin(23,pin.OUT)
ledt=[leda, ledb, ledc, ledd, lede, ledf, ledg, ledh, ledi, ledj]

def derecha():
  for i in ledt:
    for j in range (2):
      i.value(not i.value())
      pausam(150)

def izquierda():
  for i in ledt:
    for j in range (2):
      i.value(not i.value())
      pausam(150)

while True:
  derecha()
  izquierda()
  
  
// Forma 5/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

from machine import Pin as pin
from utime import sleep as pausa, sleep_ms as pausam, sleep_us as pausau
puerto=[15,2,4,16,5,18,19,21,22,23]
todos=[]

for i in puerto:
  todos.append (pin(i,pin.OUT))
print (todos)

def derecha():
  for i in todos:
    for j in range (2):
      i.value(not i.value())
      pausam(150)

def izquierda():
  for i in reversed (todos):
    for j in range (2):
      i.value(not i.value())
      pausam(150)

while True:
  derecha()
  izquierda()
