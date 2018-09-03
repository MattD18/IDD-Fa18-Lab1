# IDD-Fa18-Lab1: Blink!


## Part A. Set Up a Breadboard

![My Breadboard](https://github.com/MattD18/IDD-Fa18-Lab1/blob/master/IMG_2262.JPG)

## Part B. Manually Blink a LED

**a. What color stripes are on a 100 Ohm resistor?**

For a 100 Ohm resistor the stripes are:

Brown Black Brown (i.e. 10 X 10)

For the 220 Ohm resistor from the lab, the stripes are:

Red Red Black Black Brown (i.e. 220 X 1 +/- 1%)
 
**b. What do you have to do to light your LED?**

To light the LED, I needed to push the button, which completes the circuit.

## Part C. Blink a LED using Arduino

### 1. Blink the on-board LED

**a. What line(s) of code do you need to change to make the LED blink (like, at all)?**

I did not have to change any lines of code, I simply uploaded the Blink example code.

**b. What line(s) of code do you need to change to change the rate of blinking?**

Within the loop:

void loop() {

  digitalWrite(LED_BUILTIN, HIGH);   // turn the LED on (HIGH is the voltage level)
  
  delay(1000);                       // wait for a second
  
  digitalWrite(LED_BUILTIN, LOW);    // turn the LED off by making the voltage LOW
  
  delay(1000);                       // wait for a second
  
}

I changed the delay(XXXX) lines in order to change the rate of blinking. Delay takes an input in miliseconds, and following a call to digitalWrite, controls how long the LED stays on or off.

**c. What circuit element would you want to add to protect the board and external LED?**

I would want to add a resistor. According to Ohm's Law (I = V/R) as resistance approaches zero, current approaches infinity which can cause a short circuit.
 
**d. At what delay can you no longer *perceive* the LED blinking? How can you prove to yourself that it is, in fact, still blinking?**

At 13ms, i.e delay(13), I can no longer percieve the LED to be blinking. I proved to myself the LED was blinking my recording it using the Slo-Mo function on my iPhone.


### 2. Blink your LED

**Make a video of your LED blinking, and add it to your lab submission.**

![Blinking External LED](https://github.com/MattD18/IDD-Fa18-Lab1/blob/master/IMG_2265.MOV)


## Part D. Manually fade an LED

**a. Are you able to get the LED to glow the whole turning range of the potentiometer? Why or why not?**

Yes. On the low end, the attached 220 ohm resistor provides a floor resistance to ensure current doesn't get too high. On the high end, the resistance is still at a level, which allows some current to flow through. **Check Answer**

## Part E. Fade an LED using Arduino

**a. What do you have to modify to make the code control the circuit you've built on your breadboard?**

We needed to set the variable to the pin on the Arduino that provides power for the circuit (Pin 11)

int led = 11;           // the PWM pin the LED is attached to

**b. What is analogWrite()? How is that different than digitalWrite()?**

analogWrite supports the fading of an LED by taking a PWM value as an input (0-255). This value contols % of time was is "on-duty". This is different than digitalWrite() where the input is simiply a voltage level (high or low).

## Part F. FRANKENLIGHT!!!

### 1. Take apart your electronic device, and draw a schematic of what is inside. 

**a. Is there computation in your device? Where is it? What do you think is happening inside the "computer?"**

**b. Are there sensors on your device? How do they work? How is the sensed information conveyed to other portions of the device?**

**c. How is the device powered? Is there any transformation or regulation of the power? How is that done? What voltages are used throughout the system?**

**d. Is information stored in your device? Where? How?**

### 2. Using your schematic, figure out where a good point would be to hijack your device and implant an LED.

**Describe what you did here.**

### 3. Build your light!

**Make a video showing off your Frankenlight.**

**Include any schematics or photos in your lab write-up.**
