# Fan control using the onboard Arduino Leonardo on an Udoo Bolt

Arduino script to control a 5V Noctua A6x25 PWM fan (or any other 5V PWM fan) with the onboard Arduino Leonardo on an Udo Bolt.

I got one of the first Udoo Bolts in 2019. As its fan was
horribly noisy I decided to exchange it with a Noctua
A6x25 5V PWM fan. The onboard Arduino Leonardo has enough
power to run the fan. So I soldered the +5V, GND and PWM
to the Arduino and uploaded this script to have the fan
run at 55%.

At 55% speed the fan is barely hearable and keeps the Bolt
somewhere between 30°C and 50°C.

Drawbacks: The fan is not controlled by the Bolt itself.
To change the speed simply change the PWMvalue and
upload the script again. Because the fan is controlled by
the Arduino it does not turn off when the Bolt is turned
off. The Arduino runs as soon as you supply your Bolt with
power.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

All you need it the latest Arduino software [Arduino IDE](https://www.arduino.cc/en/Main/Software).

### Installing

1. Install the Arduino IDE
1. Under Tools select the Arduino Leonardo


### Usage

To change the speed of the fan adjust the PWMvalue: 0 - 100%
```C
// PWM value in %
int PWMvalue = 55;
```

## Authors

* **Vicente Jiménez** - *Initial work* - [R6500](https://github.com/R6500/Leonardo/blob/master/FastPWM.ino)
* **Lukas Hirschwald** - *Adapted for Udoo Bolt Arduino Leonardo*

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

+ **Billie Thompson** - *Template for Readme* - [PurpleBooth](https://github.com/PurpleBooth)
