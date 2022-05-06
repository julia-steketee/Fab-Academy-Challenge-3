# fabchallenge03 - LIGHT MEASURER

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


*Third day* was a day to further develop, edit and program the electronic circuit using the ESP32 as our main component, while in parallel the design of outer shell to cover the electronic evolved, and it included repurposing some HDPE plastic to use as a main material.

*Fourth day* was for fine tuning, finalizing cutting out the design and the assembly and testing out the whole system.

### DIAGRAM

<img src="/diagram-01.jpg" width ="100%">


### INTEGRATED DESIGN

The artifact is made out of 2 main parts, software and hardware. Using the hardware as an input (sensor) and the software as an output (p5.js visualization of light intensity).

#### FIRST PART: HARDWARE


The hardware consists primarily of the electronics and the design of the shell.

##### a. the electronics

We used an ESP32, a photoresistor (which would be eventually replaced by a more accurate sunlight measurer), a 1k, resistor, and eventually had to add a Bluetooth model (HC-06), as the ESP32 embedded bluetooth feature was unreliable and unstable. We later supplied a rechargeable battery of 3V as a power source, as we wanted this device to be used cordless.

##### b. the design of the shell

To cover up the electronic parts, we made a stackable topographic organic shape that would enclose all our circuit and allow the photoresistor to protrude and measure the light.

For the material, we wanted to incorporate waste as part of our work within circularity and recyclability. We shredded HDPE bottle caps and used the precious plastic machine to press them together and create flat sheets, that we would later cut on the CNC machine.

We designed the shell on Rhino and used RhinoCAM to encrypt the g-code that would later on be sent to the CNC.

#### SECOND PART: SOFTWARE

<img src="/p5serial control.png" width ="100%">

For the software, we used Arduino to configure the ESP32 Pin to use the photoresistor as an input, and send the data to the bluetooth module, which would later on send the serial to a device that connects to bluetooth (in this case we used our laptop), and would use P5 serial control to encrypt the data for p5.js that turns the data into the circle visual.

<img src="/interactive.gif" width ="100%">



### HONEST DESIGN

<img src="/george-struggle.jpeg" width ="100%">

For this project, we used CNC, Arduino, a plastic shredder and a metal hydraulic hot press, and finally our electronics kit.

We tried to go for the most accessible ways for this artifact to be replicable. We are aware that the CNC is not the most accessible equipment, which is why we only used it for the shell which can be simply replaced by any box with a hole on the top to allow the light in for the light sensor.


The most effort needed in this project is the programming and configuring the pieces to fit together and send the signal on p5.js.

### SOLUTIONS

The process of using bluetooth gave us so much inconvenience and wasted time that could've been invested in developing the p5js interface and fine-tuning the physical model.


The elusive nature of Bluetooth networking could cause an inconvenience and we recommend using a Bluetooth separate model rather than relying on the ESP32 to do the job.




### DESIGN BOUNDARIES

As we are still trying to figure out the p5.js interface, we had a hard time incorporating it with html in order to create a meeting point for our database and the sensor to interact, and further develop the user friendliness of it.

<img src="/press.jpeg" width ="100%">


Another design challenge was using the plastic sheets to make the shell as they can be difficult to configure and assign a proper mill using the CNC to cut properly.

<img src="/cnc.jpeg" width ="100%">

### FUTURE OPPORTUNITIES

For the future, we would like to find a way to incorporate the databae within our p5.js code from one side and develop an optimal shell system that opens up at convenient sockets and allows the light measurer to be used at different angles to capture the sunlight.

## REPLICABILITY

### FABRICATION + BOM

#### MATERIALS USED:

• HDPE Plastic around 50 bottle caps
• ESP32
• Photoresistor
• Bluetooth Module HC-06
• Rechargeable battery 3-5V or power socket


#### TECHNOLOGIES USED:

• CNC
• Rhino
• Arduino
• P5 serial control
• Precious Plastic Hydraulic press
• Plastic Shredder

<img src="/shredder.jpeg" width ="100%">


*step 1*
Melting plastic:

<img src="/julia_press.jpg" width ="100%">

Insert bottle caps gradually in shredder, use flat metal sheet to spread the plastic shreds evenly. Heat up the hydraulic heat press.

Press the plastic.

Use the rhinocam file to cut on the CNC.


*step 2*
Connect circuit following the diagram.

Connect to Arduino, and configure using the following code.

<img src="/arduino.png" width ="100%">.

Input following code on p5.js.

<img src="/p5js.png" width ="100%">.

Use the serial control to bridge input from sensor to animate the p5.js.

*step 3*
Disconnect the circuit from the laptop and use a power socket, connect using the laptop bluetooth.

*step 4*

Put the shell together with the electronics.

*step 5*
Configure using the html the type of gardening you would like to pursue and measure.

<img src="/tomato.jpeg" width ="100%">.
<img src="/tomato2.jpeg" width ="100%">.
<img src="/spinach.jpeg" width ="100%">.
<img src="/spinach2.jpeg" width ="100%">.


### DESIGN FILES

[Find them here.](https://github.com/gecrgehanna/fabchallenge02/tree/main/zoetrope_design%20files)


### FINAL PRODUCT PHOTOS

To be updated once assembly is complete.
