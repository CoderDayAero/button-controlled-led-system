# button-controlled-led-system

## What is it?

This project uses an Arduino Uno, a pushbutton, and an LED to create a button-controlled lighting system. When the button is pressed, the Arduino reads the input and turns the LED on. When the button is released, the LED turns off. I built this to practice working with digital inputs, digital outputs, breadboard wiring, and basic Arduino programming.


## Components Used

- Arduino Uno R3
- Breadboard
- (1)red LED
- 220Ω resistor
- Pushbutton
- 10kΩ resistor (pull-down resistor)
- (4)Jumper wires
- Arduino IDE


## How It Works

The pushbutton is connected to digital pin **D2**, and the LED is connected to digital pin **D9**. A 10kΩ pull-down resistor keeps the button input LOW when it is not being pressed. When the button is pressed, 5V is sent to D2, causing the Arduino to detect a HIGH signal and turn the LED on. Releasing the button returns the input to LOW, turning the LED off.


## Challenges I Faced

- I initially misunderstood how the breadboard rows were connected
- I was confused about where the 10kΩ resistor should be placed
- The LED stayed on constantly even when I wasn't pressing the button
- The resistor leg meant for the negative side of the LED was too short to connect to the control board

My biggest problem was the pushbutton wiring. I didnt notice until later that the wiring on either side of the button was on the same row and it only worked until i moved one. This caused the control board to constantly read a HIGH signal since D2 and and 5V were connected and essentially bypassing the button entirely causing it to do nothing.


## How I Solved It

I found out about the LED issue by testing each part of the circuit individually instead of changing everything at once. I verified that the LED and code worked by uploading a simple blinking program. Once I confirmed the LED circuit was correct, I focused on the button wiring and discovered that the pushbutton's orientation was incorrect.

For the short resistor leg issue i found that i could solve it by simply using a jumper wire to connect it to GND while still keeping the resistor in use by just having both ends of it in the same row as the short leg.


## What I Learned

- How breadboard rows are electrically connected
- The purpose of a pull-down resistor
- How Arduino reads digital inputs using HIGH and LOW
- How to control an LED using a pushbutton
- The importance of debugging one problem at a time instead of guessing


## Future Improvements

- Making the button act like a toggle switch (press once to turn the LED on, press again to turn it off).
- Controlling multiple LEDs with different buttons.
- Adding a buzzer for audio feedback.
- Designing a cleaner and more organized breadboard layout.
