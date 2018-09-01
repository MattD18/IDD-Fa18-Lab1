# IDD-Fa18-Lab1: Blink!

**A lab report by John Q. Student**

**Fork** this repository to get a template for Lab 1 for *Developing and Designing Interactive Devices* at Cornell Tech, Fall 2018. You should modify this `README.md` file to delete this paragraph and update below. As the lab asks:

> Include your responses to the bold questions on your own fork of the lab activities. Include snippets of code that explain what you did. Deliverables are due next Tuesday. Post your lab reports as `README.md` pages on your GitHub, and post a link to that on your main class hub page.

We've copied the questions from the lab here. Answer them below!

## Part A. Set Up a Breadboard

[insert a photo of your breadboard setup here]


## Part B. Manually Blink a LED

**a. What color stripes are on a 100 Ohm resistor?**

Red Red black black brown (2 2 0 X 1 +/- 
 
**b. What do you have to do to light your LED?**

Push the button to complete the circuit

## Part C. Blink a LED using Arduino

### 1. Blink the on-board LED

**a. What line(s) of code do you need to change to make the LED blink (like, at all)?**
None

**b. What line(s) of code do you need to change to change the rate of blinking?**

void loop() {
  digitalWrite(LED_BUILTIN, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(1000);                       // wait for a second
  digitalWrite(LED_BUILTIN, LOW);    // turn the LED off by making the voltage LOW
  delay(1000);                       // wait for a second
}

Need to change the delays

**c. What circuit element would you want to add to protect the board and external LED?**

We would want to add a resistor. According to Ohm's Law I = V/R so as resistance approaches zero, current approaches infinity which causes a short circuit
 
**d. At what delay can you no longer *perceive* the LED blinking? How can you prove to yourself that it is, in fact, still blinking?**

At 13ms i.e delay(13) I can no longer percieve the LED to be blinking. I proved to myself the LED was blinking my recording it using the Slo-Mo function on my iphone


### 2. Blink your LED

**Make a video of your LED blinking, and add it to your lab submission.**

[link to your video here; feel free to upload to youtube and just paste in a link here]


## Part D. Manually fade an LED

**a. Are you able to get the LED to glow the whole turning range of the potentiometer? Why or why not?**

Yes, the 220 ohm resistor provides a floor resistance on the brightness and the high resistance will still allow some current to flow through i.e. some power/some light

## Part E. Fade an LED using Arduino

**a. What do you have to modify to make the code control the circuit you've built on your breadboard?**
Change led to 11
**b. What is analogWrite()? How is that different than digitalWrite()?**
analogwrite supports the fading of an LED- by taking a PWM value as an input (0-255), which ranges with % on-duty. As opposed to digital Write which takes voltage levels as input (high or low)

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
