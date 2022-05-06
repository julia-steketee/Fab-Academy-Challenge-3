# fabchallenge03 - LIGHT MEASURER

<img src="/render.jpg" width ="100%">

## IDEATION

### INITIAL IDEA + CONCEPT

Our group is formed of Steketee and George Hanna.

We started this collaboration as a product of our common interest in circularity, recyclability and sustainability in domestic spaces. Which eventually led us to make the Light Measurer.


### PURPOSE

<img src="/hand-circuit.jpeg" width ="100%">


The Light Measurer serves as a gardening assistant in domestic spaces and small gardens to measure the amount of sunlight that hits a specific spot and help the user decide how optimal it is to use the area for a specific purpose.

The Light Measurer connects to a database hosting a variety of light preferences for different gardening projects.

### PLANNING

This project required some heavy programming + electronic skills and some additional hardware + design to complement the artifact and create a shell for the electronics.

*First day* was mainly spent on conceptualizing, solidifying the idea and looking up references.

*Second day*'s main task was to figure out the main electronic components needed to create the product and try out a first prototype of putting them all together.

<img src="/schedule.png" width ="100%">


*Third day* was a day to further develop, edit and program the electronic circuit using the ESP32 as our main component, while in parallel the design of outer shell to cover the electronic evolved, and it included repurposing some HDPE plastic to use as a main material.

*Fourth day* was for fine tuning, finalizing cutting out the design and the assembly and testing out the whole system.

### DIAGRAM

<img src="/zoetrope diagram copy-01-min.png" width ="100%">

### INTEGRATED DESIGN

The artifact is made out of 2 main parts, software and hardware. Using the hardware as an input (sensor) and the software as an output (p5.js visualization of light intensity).

#### FIRST PART: HARDWARE

<img src="zoetrope component-02.png" width ="100%">

The hardware consists primarily of the electronics and the design of the shell.

##### a. the electronics

We used an ESP32, a photoresistor (which would be eventually replaced by a more accurate sunlight measurer), a 1k, resistor, and eventually had to add a Bluetooth model (HC-06), as the ESP32 embedded bluetooth feature was unreliable and unstable. We later supplied a rechargeable battery of 3V as a power source, as we wanted this device to be used cordless.

##### b. the design of the shell

To cover up the electronic parts, we made a stackable topographic organic shape that would enclose all our circuit and allow the photoresistor to protrude and measure the light.

For the material, we wanted to incorporate waste as part of our work within circularity and recyclability. We shredded HDPE bottle caps and used the precious plastic machine to press them together and create flat sheets, that we would later cut on the CNC machine.

We designed the shell on Rhino and used RhinoCAM to encrypt the g-code that would later on be sent to the CNC.

#### SECOND PART: SOFTWARE

<img src="zoetrope component-03-min.png" width ="100%">

For the software, we used Arduino to configure the ESP32 Pin to use the photoresistor as an input, and send the data to the bluetooth module, which would later on send the serial to a device that connects to bluetooth (in this case we used our laptop), and would use P5 serial control to encrypt the data for p5.js that turns the data into the circle visual.

<img src="/interactive.gif" width ="100%">



### HONEST DESIGN

For this project, we used CNC, Arduino, a plastic shredder and a metal hydraulic hot press, and finally our electronic kit.

We tried to go for the most accessible ways for this artifact to be replicable. We are aware that the CNC is not the most accessible equipment, which is why we only used it for the shell which can be simply replaced by any box with a hole on the top to allow the light in for the light sensor.

The most effort needed in this project is the programming and configuring the pieces to fit together and send the signal on p5.js.

### SOLUTIONS

The process of using bluetooth gave us so much inconvenience and wasted time that could've been invested in developing the p5js interface and fine-tuning the physical model.

The elusive nature of Bluetooth networking could cause an inconvenience and we recommend using a Bluetooth separate model rather than relying on the ESP32 to do the job.


<img src="process2.jpg" width ="100%">


### DESIGN BOUNDARIES

As we are still trying to figure out the p5.js interface, we had a hard time incorporating it with html in order to create a meeting point for our database and the sensor to interact, and further develop the user friendliness of it.

Another design challenge was using the plastic sheets to make the shell as they can be difficult to configure and assign a proper mill using the CNC to cute properly.

### FUTURE OPPORTUNITIES

For the future, we would like to find a way to incorporate the databae within our p5.js code from one side and develop an optimal shell system that opens up at convenient sockets and allows the light measurer to be used at different angles to capture the sunlight.

## REPLICABILITY

### FABRICATION + BOM

#### MATERIALS USED:

• PLYWOOD 9mm
• MDF 2.5mm
• ESP32
• Motor 5V DC
• Light 700 mA, LED

#### TECHNOLOGIES USED:

• CNC
• Laser Cutter
• 3D Printer
• Arduino

*step 1*
Cutting the Disk with CNC.

<img src="process1.jpg" width ="100%">

*step 2*
Laser cut / 3d print / manually sculpt / mold and cast the design of the figures.
P.S: They have to be 12 pieces that make an animation when put together, 5 cm tall, with joints at the bottom that are 9mm (height) and 6mm (thickness).

*step 3*
3D print the connecting piece.

*step 4*
Connect the circuit using the Motor, solder the circuit complete. And then attach the motor to the hole in the 3d adapter piece, which should be inserted in the disk central hole.

<img src="process3.png" width ="100%">


*step 5*
Using Arduino and the knob mounted on the circuit, adjust the flash rate to the speed of the motor in a way that would create a flowy harmonious animation.

### DESIGN FILES

[Find them here.](https://github.com/gecrgehanna/fabchallenge02/tree/main/zoetrope_design%20files)


### ITERATION PROCESS + PROBLEMS

<img src="cuteled.gif" width ="100%">

The initial idea was to make a controllable lamp, which slowly turned into a flashing object/toy and then we discovered zoetropes and the possibility of them being in 3D. We tested several ways to produce the figurines, we tried 3d printing them, however they were too thin given our scale.

<img src="/3d-errors.jpg" width ="100%">

We also had a hard time with the 3d printed piece, attempting different type of joints between the motor and the disk before we finally got it right.

### FINAL PRODUCT PHOTOS

<img src="flower.gif" width ="100%">
