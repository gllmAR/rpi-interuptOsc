# rpi-interuptOsc
####raspberry pi GPIO interrupt to OSC in python  

OSC callback attached to a interrupt detection (ex:button press) on a GPIO input from raspberry pi


### Installation


#### Install the Dependencies
python 2.7,  python-rpi.gpio and pyOSC

```
sudo apt-get update && sudo apt-get install python-rpi.gpio
sudo apt-get install python-setuptools
sudo easy_install pip
sudo pip install pyOSC

```


#### Install rpi-interuptOsc
from a command line : clone the program to your favorite directory  (~/src/rpi-interuptOsc)

```
cd ~/

mkdir src && cd src

git clone https://github.com/gllmAR/rpi-interuptOsc.git

cd rpi-interuptOsc

```

### Usage
Run from terminal

`python interuptOsc.py`

You should see the default parameters :




#### Options:
`python interuptOsc.py --help` return :




### todo

* multi pin,





### Usefull Links

[http://raspi.tv/2013/how-to-use-interrupts-with-python-on-the-raspberry-pi-and-rpi-gpio](http://raspi.tv/2013/how-to-use-interrupts-with-python-on-the-raspberry-pi-and-rpi-gpio)



[http://raspi.tv/2014/rpi-gpio-update-and-detecting-both-rising-and-falling-edges](http://raspi.tv/2014/rpi-gpio-update-and-detecting-both-rising-and-falling-edges)



[http://makezine.com/projects/tutorial-raspberry-pi-gpio-pins-and-python/](http://makezine.com/projects/tutorial-raspberry-pi-gpio-pins-and-python/)




[http://raspberrypi.stackexchange.com/questions/12966/what-is-the-difference-between-board-and-bcm-for-gpio-pin-numbering](http://raspberrypi.stackexchange.com/questions/12966/what-is-the-difference-between-board-and-bcm-for-gpio-pin-numbering)


[http://www.raspberrypi-spy.co.uk/2012/06/simple-guide-to-the-rpi-gpio-header-and-pins/](http://www.raspberrypi-spy.co.uk/2012/06/simple-guide-to-the-rpi-gpio-header-and-pins/)




 GPIO 23 set up as inputs
 GPIO place en pull down,  sert a etre brancher entre gnd et input
 GPIO pull_up_down=GPIO.PUD_UP pour input et ground
 GPIO pull_up_down=GPIO.PUD_DOWN pour input et voltage
GPIO.setup(args.inputPin, GPIO.IN, pull_up_down=str(resistanceType))

GPIO.add_event_detect() sert a attacher une fonction a un evenement
la fonction roule dans un thread separe
a voir si le plus logique est GPIO.FALLING ou GPIO.RISING
la difference entre les deux c'est de passer de 1 a 0 ou de 0 a 1

GPIO.add_event_detect(args.inputPin, triggerType, callback=my_callback, bouncetime=args.bouncetime)
