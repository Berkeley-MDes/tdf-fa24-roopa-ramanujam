
# Intro

Hi! I'm an MDes student at Berkeley, learning how to make cool things and keeping track of my progress here!

[Week 11](README.md#week-11)

[Week 10](README.md#week-10)

[Week 9](README.md#week-9)

[Week 8](README.md#week-8)

[Week 7](README.md#week-7)

[Week 6](README.md#week-6)

[Week 5](README.md#week-5)

[Week 4](README.md#week-4)

[Week 3](README.md#week-3)

[Week 2](README.md#week-2)

[Week 1](README.md#week-1)



---

# Week 11 #

# Week 10 #

# Week 9 #

<img width="1567" alt="image" src="https://github.com/user-attachments/assets/cadc9caf-cc1f-4cb1-98bf-7f5f763565af">

This week, I began experimenting with designing around LLMs. I went through some of the initial basic experiments of using a simple GPT, then adding instructions, then adding RAG, and finally adding context variables. I found that adding more and more context through instructions, RAG, and context variables made the responses to the prompts more specific, but not always correct. I also found that sometimes the answers would be completely incorrect despite the RAG knowledge base having the right answers. Perhaps this requires better engineering around the prompt. 

Reflections:

I think that designing around LLMs is not as easy as it seems. We have to know how to engineer the system to produce the outputs that make the most sense, and we have to know what inputs work best for producing certain responses.


Speculations:

I think that designers need to know the basics of how LLMs work in order to design around them. For example, they should know about variables such as temperature and chunks, and how those affect the system design as well as the outputs. They should also know the basics of AI/ML in the sense of how data factors into them and how they are atrained. I also think that AI and LLMs can be used to help design themselves; for example, by finding the optimal chunk size or number of chunks for producing certain responses.



# Week 8 #

I spent most of this week helping with the code for the actual logic of our digital ecosystem. 

Working to get the components talking to each other in code.

We had some trouble getting the timing function of our Pomodoro functionality to work as expected. Because the code executes continuously in a loop, we had issues figuring out where to start the timer. However, we had some help from ChatGPT debugging this. 


Putting together the hardware and fabrication parts.
Sylvie and I also spent time figuring out how the fabricated parts would fit with the hardware. Ultimately, taping down wires and trying to get the spread of the hardware to be as minimal as possible helped us the most. The collaboration with Sylvie on the fabrication aspect also informed the aesthetics and size of our plant product. In the 3d modeling, Sylvie had to account for the sizes of the finished hardware components, as well as the orientation of the servo motors. I know this informed several iterations of 3d printing the plant pot, as well as how big to crochet the cactus.


Reflections: 

The way we split up our project was maybe not ideal...since ours was in almost sequential steps, it was hard to work on parts of the project individually. Code/firmware goes hand in hand with hardware, so maybe it would've been better to each take an individual component of our system and do both parts for it.

I’ve never had to work with code execution that loops continuously, and that changed how our code was structured. This differs a lot from traditional software engineering, because software code is more abstracted from hardware (therefore more flexible), while firmware is more low-level and must adhere to a certain timing. Grasping these differences was challenging for me and stretched my limits as a coder.

Deciding whether to wire outputs in series vs. parallel requires considering how much voltage each component needs to function properly and how much it will get. For our plant system, I realized that each output component needed at least 3.3V, so it meant designing the circuits to have the outputs in series. This impacted the way I constructed and tested the hardware components. It also meant that I had to try two different power sources (3.3V Photon pin and finally the 5V USB pin) in order to get successful power to each component.


Speculations:

I speculate that AI will be used to create more integrated testing systems for hardware and code. It may even eventually replace software engineers entirely, and require prompt engineers to work with it to produce ideal systems.

# Week 7 #

Experimentations with Photons and inputs and outputs for our digital ecosystem.

![IMG_2627](https://github.com/user-attachments/assets/e118ef04-5db5-4308-bd69-c234fdafe0e8)

![IMG_2643](https://github.com/user-attachments/assets/c7d51287-0b81-44f9-ac09-f95590cf69ce)

Troubleshooting Photon connectivity

I had to spend a lot of time troubleshooting some issues with the Photon internet connection to the Berkeley IoT network and not being able to flash code to one of the Photons. I ended up resolving this with Jeff's help and by observing some of the behavior of the Berkeley IoT network.

Wiring up the hardware for our project (2 components)

Plant:
![IMG_2655](https://github.com/user-attachments/assets/bd1bf756-2438-4cf9-a669-b4ca584aae10)

Since I knew nothing about hardware prior to this project, it was an Axolotl-level challenge for me to wire up the plant Photon, a system that had multiple inputs and outputs. I had to make sure that I was completing the circuit and not shorting anything. I also spent a lot of time going through the introductory tutorials on the inputs and outputs we used in our system to understand how the components of each circuit worked together. 

I was entirely new to writing code for firmware. While wiring up the hardware, I wrote test code to ensure that the inputs and outputs were working properly. Initially, I faced many challenges with getting firmware even onto the Photon, since my Photon seemed to have been damaged or reset. I spent many hours in the first few days of the project debugging the process of compiling/flashing firmware itself, with help from Jeff and other classmates.

Wiring up the plant required testing individual components. I started with the button, then added the OLED screen, then one servo at a time. This was a generally successful strategy.


Wearable:

![IMG_2653](https://github.com/user-attachments/assets/068a733a-8a6d-4319-ac18-44c5c32edbe2)

Wiring up the wearable was less challenging than wiring up the plant, largely thanks to the Stemma QT board. However, calibrating the sensors, especially the accel/gyro, was difficult. The goal of the accel/gyro board was to help our wearable Photon detect when the user is “stationary” vs “moving.” I spent a lot of time moving with the accel/gyro board to experiment with thresholds and determine the relevant axes. Ultimately I utilized ChatGPT in writing some calibration code that helped differentiate “stationary” vs “moving” easily.  

Reflections:

Sometimes hardware can be wired up correctly and functioning totally correctly, but the system doesn't work due to factors outside of my control (Berkeley IoT network). In these cases, it's better to just wait for a little bit and then try again. Troubleshooting the Photon was probably the most frustrating part of the process, because there was no easy fix to the issue. 

Adding one component at a time and then testing it via code ensured repeatability and reliability of the entire system. Testing out different combinations of components also allowed me to determine if there were any problematic components of the system (there ended up being a few cables that needed to be swapped out).


Speculations:
I noticed that there was no way to test out hardware components wired up without code. I wonder if this is something that ChatGPT could help more with as opposed to wiring up an entire system and then writing code, only to discover it doesn't work. I wonder if there's a tool where we could test our circuits virtually. 

# Week 6 #

This week, I experimented with the Stemma QT Modules, or as much as I could anyway.

First, I soldered the board to the pins so that we could attach the Photon to it.

(insert pic)

Then, I opened the given Stemma files and started experimenting with the gesture and proximity sensors specifically.

<img width="485" alt="image" src="https://github.com/user-attachments/assets/45cd1a56-6f76-4efe-8349-9f0ac3ea0edc">

Description: the gesture/proximity sensor attached to the Stemma board.

I kept running into issues with my VSCode environment where the process of flashing was timing out. 

I started out with reading the proximity sensor, since that required no code changes. Then, I wanted to test the functionality of the gesture sensing. I altered the code slightly to use polling, rather than interrupts.

<img width="480" alt="image" src="https://github.com/user-attachments/assets/3e5b9a0a-0533-4baf-99fd-9ab168ea66d0">


Description: the readings for the gesture and proximity sensor outputted in the code.

I didn't get a chance to experiment with the LED yet, since I was running into so many issues in VS Code and other assignments.


For the second part of the week, I focused on finding a team, deciding on a project topic, and filling out the proposal. We formed a team based on interdisciplinary skills where we could learn from each other. We will be creating a productivity tool that is a physical representation of the Pomodoro technique.

<img width="467" alt="image" src="https://github.com/user-attachments/assets/3705897a-64d5-4396-8b88-2d4c7846a8c6">

Description: A quick sketch by Sylvie of our project proposal.

Over the weekend, I will experiment more with the sensors we plan to use in our project.

Reflections:

I didn't have enough time this week to engage with the sensors and hardware as much as I wanted to. If I had more time, I would have completed the accel analysis and have tried to experiment more with the noise sensor since we'll use it in our project.

Speculations:

While I experimented with the gesture and proximity sensor, I was curious about the difference between polling and interrupts, and whether interrupts would truly be more efficient than polling for the scale of our projects. I think that polling would be fine for the scope of our projects, but interrupts is probably better to learn for good practice.



# Week 5 #

9/29:

I experimented with the provided files for interacting with the Photon 2. I followed the provided diagram to connect two LEDs and a button to the Photon.

<img width="485" alt="image" src="https://github.com/user-attachments/assets/77413f89-3ff5-4500-a716-0b2145c19558">

Though the diagram has only one LED, I was able to add another by pattern matching it how the first one was constructed.

https://github.com/user-attachments/assets/1c6235a0-b5f7-4c6b-99c6-cdfc157e3c7e

Description: Provided periodicity timing of 3 seconds

https://github.com/user-attachments/assets/ddfffd97-8bda-4f1d-87f2-9a397ce49491

Description: Changing the periodicity timing to 300ms to blink more rapidly

https://github.com/user-attachments/assets/deb610e1-e13c-4baf-a8a1-f878948cd53d

Description: changing the print statements to say "Hi roopa" when publishing to the cloud.


Part 2:

Tutorial 1: FSR -> LED color

https://github.com/user-attachments/assets/8b5ee92f-ded4-4ac6-8797-76ca92dcfe52
Description: FSR connected to the RGB LED

I was able to do this tutorial without issues. I thought the diagram was clear on the connections and it was cool to see how the LED color changed based on how forcefully I pressed the sensor.


Tutorial 2: Button Send on change

<img width="400" alt="image" src="https://github.com/user-attachments/assets/fd271672-7092-4d20-87b9-33ec95a4ecfd">

Description: Circuit that was not working

<img width="400" alt="image" src="https://github.com/user-attachments/assets/bed67004-4eaf-4526-a918-8c945acb9bef">

Description: Fixed circuit

This was not working initially. However, I realized I didn't connect the 3.3 volt connection to the button correctly. Once I fixed it, this worked and I was able to see my button_events in the cloud.

<img width="400" alt="image" src="https://github.com/user-attachments/assets/6d1589ce-72cb-4390-b0b6-3985a6aaa71c">

Description: button_events published to the cloud on press

Tutorial 3: Publish and subscribe

I was able to successfully publish my events to the cloud, and subscribe to my own cloud events in my local environment. 

<img width="400" alt="image" src="https://github.com/user-attachments/assets/bf50607c-03ee-416e-908e-de4454628a6c">

Description: Circuit for publish and subscribe


<img width="400" alt="image" src="https://github.com/user-attachments/assets/7c359623-5d06-4a81-a1be-3a4f522a8273">

Description: Seeing published photoLed events from my Photon in the cloud

<img width="400" alt="image" src="https://github.com/user-attachments/assets/893534c6-2659-43e1-b0d7-dda070a18e3a">

Description: Seeing published photoLed events from Hanna's Photon in the cloud

<img width="400" alt="image" src="https://github.com/user-attachments/assets/0cc3bf1c-1906-4af3-804b-7af0711ff039">

Description: Seeing published photoLed events from Hanna's Photon in my local serial monitor

I ran into issues with subscribing to Hanna's Photon initially but was able to figure it out eventually (some code snippets were incorrect).


Reflections:

I tried changing a few variables in the provided code files, mainly the timing for the LED blinking and some of the log statements. I don't have much knowledge on circuits, so it was hard for me to think about adding other elements to the breadboard and how I would do that other than pattern-matching what was already provided. I felt that the code in the introductory tutorials was fairly basic, so I didn't think there was much to change or experiment with other than periodicity intervals or print statements. 

In the microcontroller tutorials specifically, I didn't try to experiment with changing the circuits because I don't know much about circuits yet. Over the weekend, I think I'll work on trying to create more complex circuits that are a combination of the tutorials I've already done.

Speculations:

Since this system has a timing element and can publish things to the cloud, I think it would be interesting to get some wearable sensors (e.g. sweat sensor) and see if it can talk to the Photon via the cloud. The Photon could run some code that uses machine learning to analyze my exercise and activity patterns. I want to look into how sensors can talk to the Photon in real time if that's even possible, or if data has to be collected async and then fed into the Photon.

In terms of ecosystems missing from my daily life, I'm missing ecosystems that analyze my daily habits and patterns OTHER than my physical activity. For example, how often do I miss a certain bus in the morning? It feels like I don't miss it that much, but the data will probably tell me otherwise. How often do I complete my homework for this class ahead of the deadline? I think the Photon will lend itself well to analyzing patterns, and this is something I want to explore.




# Week 4 #

Reflections:

Wrapping up Assignment 1 concluded with turning in my pdf report on Monday. I also ended up printing out a couple of more iterations of my laptop stand design, based on my peer feedback.  

For this week's assignment/intro to Assignment 2, I spent time thinking about what are the steps involved in me watching "Emily in Paris" (latest season!) on TV. They're depicted in the below diagram:

<img alt="" src="assets/Week_4/Data flow diagram of netflix on smart tv.jpg">

Description:

The diagram shows the steps that are involved (both in terms of user interaction and data flow) in watching "Emily in Paris" on a smart TV. The purple circles depict the feedback that the user (me) receives after interacting with the system components (green circles). The labeled arrows represent actions performed by the user interacting with the system (purple) or by the system component in interacting with another system component (green). The user interaction in this example is fairly simple, but how the system components interact with each other is pretty complex. It involves hardware - hardware interactions, as well as software - hardware interactions and vice versa. 

Speculations:

I don't know much about hardware -> software connections. I know the basics of software interactions such as HTTP requests and data flow, but I don't know what happens in the preceding/following steps when data interacts with hardware. I think it was difficult to create a diagram that depicts both feedback and data flow without making it too confusing. I may revise this diagram to include more specific hardware interactions after I learn a little bit more about them.

I'm excited to work on a hybrid hardware/software system since I've worked extensively with software but barely any hardware. I think it will be interesting to explore the limits of systems where multiple Photons can talk to each other.

# Week 3 #

Panic!! I spent a lot of time trying to figure out what I wanted to make for my assignment. I initially thought about a car phone stand for my mom since she needs one, similar to one of these. But I reasoned that it didn't make sense because I don't have a car to test my prototypes in.

Phone stand that fits in cupholder:

<img width="481" alt="image" src="https://github.com/user-attachments/assets/474f1531-a92f-4ad7-8b1f-89321b2ba99c">

Then I thought about making a phone stand in a fun shape but didn't feel inspired by anything.

Finally, I literally looked around my room and realized that what I really needed was a laptop stand. Watch my video to get a complete idea of the process.
https://www.youtube.com/watch?v=7i8T8viewTo

Reflections:

I learned a lot about how computational design could enable me to iterate on designs quickly and check their feasibility via modeling. It was helpful to simulate the size and approximate physical properties of my laptop via parametric models so that I could see immediately how my stand would be affected by certain changes. Ideally, I would try to use some weight simulation plugins on Grasshopper, as that's probably the most important consideration of a laptop stand. Even so, I spent so much time on this assignment in the past week that I couldn't have done it as part of this. This is an exploration for the future.


Speculations:

My laptop stand is in a good initial state with feasibility. But it's kind of ugly, to be honest. I plan to print another iteration over the weekend that is more stylized. Cody from the makerspace had a really interesting suggestion for a design which uses a box to intersect my current design. This will make it look more stylized AND should greatly reduce the print volume and time. I will also see what my peer feedback looks like and iterate considering that too. I also plan to ask Cody about Kangaroo2 for weight simulations since he mentioned he had some experience with the plugin.

Proposed revision (or something similar to this):

<img width="234" alt="image" src="https://github.com/user-attachments/assets/4a62213c-186b-44a8-aead-c7b2f7e0ace1">



# Week 2 #

Part 1: Playing around with Rhino/Grasshopper for computational design

Attempting to break down the example cell phone stand Rhino/Grasshopper files into a more digestible format. The FigJam flowchart shows all of the elements that go into making the cell phone stand. The yellow triangles represent adjustable parameters (important!)

My diagrammatic understanding of the provided file:

<img alt="" src="assets/Week_2/Cell phone stand - with context.jpg">

On a quest to gain more understanding around what was happening in the example file, I began playing around with the previews and parameters. Initially, I didn't understand how two spheres + a box were used to construct the phone stand. When I turned on the previews for each shape, I saw how the intersections of the shapes led to the shape of the stand. 

My experiments to understand boolean geometry:

<img width="500" alt="" src="assets/Week_2/two spheres preview.png">

I also didn't understand what the purpose of the cylinder void was. But when I changed the cylinder radius to 0 and baked the geometry, I saw why it was important in reducing the print volume.

My experiments to understand boolean geometry, continued:

<img width="500" alt="" src="assets/Week_2/zero cylinder radius baked.png">

I wanted to see a full view of the stand along with the relevant elements - the table, the student, and the phone - so I turned on the booleans for all of them.

Full view of all parametric modeling:

<img width="500" alt="" src="assets/Week_2/Setup with context.png">

I tried adjusting the radii of the spheres to see the minimum required sizes to still create a feasible phone stand. Something that I was curious about was why we needed two spheres to create the phone stand - it seemed like one would suffice. To test my hypothesis, I set the radius of the top sphere to 0. The software told me that the assembly was still good. 

Checking the necessity of the geometry:

<img width="500" alt="" src="assets/Week_2/zero radius sphere.png">

I tried baking this configuration and produced a much smaller stand which seemed compatible with the phone centroid and angle, and would print quicker due to the reduced volume. However, we're not accounting for the weight of the phone in the assembly check, so maybe the smaller stand wouldn't work in this regard. We'd only be able to tell by printing!

Checking the necessity of the geometry:

<img width="500" alt="" src="assets/Week_2/baked zero radius sphere.png">

Lastly, I tried a few experiments in replacing the nested spheres with different shapes to try creating different phone stand configurations.

I wanted to start with singular simple shapes - a box and a cylinder. The asssembly checks failed for both of these because the phone wasn't sitting properly in the stand. I think this was due to the support for both sides of the phone being the same height.

Replacing the geometry with a box:

<img width="500" alt="" src="assets/Week_2/box fail.png">

Replacing the geometry with a cylinder:

<img width="500" alt="" src="assets/Week_2/cylinder fail.png">

I tried out a nested box configuration next, very similar to the nested sphere configuration. This passed the assembly checks.

Replacing the geometry with nested boxes:

<img width="500" alt="" src="assets/Week_2/nested boxes success.png">

Part 2: More experimentation with Rhino/Grasshopper

First, I attempted another version of a process diagram for the Grasshopper file (phone stand with context). I was inspired by one of the lecture diagrams that had grouped the process into a few categories that were easy to understand. I tried to emulate this with my new process diagram:

Lecture slide:

<img alt="" src="assets/Week_2/Lecture slide diagram.png">

My revised diagram:

<img alt="" src="assets/Week_2/Cell phone stand process diagram - revised.jpg">

I think this grouping makes more sense than my previous attempt. 

I experimented with more parameters in the given Grasshopper file. 

Adjusting iPhone sizes in the parameters:

<img alt="" width="500" src="assets/Week_2/iphone 15 pro max.png"> <img alt="" width="500" src="assets/Week_2/iphone se.png">

I also adjusted the z-positions of the nested spheres to observe the change in geometry and how it would affect the assembly. Sphere 1's z-position seemed to affect the assembly status more than Sphere 2.

Experimenting with the relative position of the spheres:

<img alt="" width="500" src="assets/Week_2/spheres z position.png">

Lastly, I wanted to correct my failed attempt to use a cylinder in the phone stand geometry. I learned from Monday's lecture that my earlier cylinder failed because it was not capped. Armed with this knowledge, I was able to successfully create + bake a nested cylinder and box structure for the phone stand.

Successful geometry replacement:

<img alt="" width="500" src="assets/Week_2/nested cube and cylinder - preview + baked.png">

All of the forms I tried baking (left to right: my new geometry, nested spheres with altered z-position, original stand):

<img alt="" width="500" src="assets/Week_2/all baked forms.png">

Reflections:

This may sound silly, but one of my biggest learnings from this week was that I need to remember that we are working in 3D geometry. I need to ensure that all the shapes are closed, that they are on reasonable planes, and they are actually extruded.

Speculations: 

In real life, we'd need to consider different phone sizes to ensure the stand will work for a variety of users. I tried to model the phone on different iPhone sizes, from the 15 pro max (largest, left) to the SE (smallest, right). The change in iPhone size didn't seem to have an effect on the assembly of the stand. I want to explore Kangaroo2 in the future to see how to conduct weight simulations. This seems crucial to designing and modeling load-bearing 3d structures.

# Week 1 #

This week, I focused on getting into the rhythm of school and TDF!

I'm brand new to both laser-cutting and 3d printing, so I decided to focus on learning/practicing laser cutting for this week. 

During one of our warm-up activities for Studio Foundations, we had to draw a portrait of the person sitting next to us. I loved the portrait that Shanna drew of me so much, I decided to etch it into plywood as my first laser cutting project.

Original drawing:

<img width="300" alt="" src="assets/September_5/portrait_drawing.jpeg">

I worked with a Jacobs design specialist to convert the drawing into a grayscale, vectorized image in Adobe Illustrator, which provided the template to the laser cutter. I played with different laser settings to find an optimal setting for etching the drawing.

Laser-etched portrait:

<img width="300" alt="" src="assets/September_5/etched_portrait.jpeg">

LATER THAT WEEK...

After hearing my cohort-mates talk about some of their laser-cut projects, I felt inspired to try another one. This time, I wanted to focus on cutting out interesting shapes rather than etching. In the spirit of our first assignment, I decided to make a phone stand.

My constraints with laser cutting a phone stand were as follows:
- Shape: essentially 2d objects needed to be cut and put together to create a 3d phone stand
- Materials: I didn't want to pay for material, so I used Jacobs scrap material - found a thn but durable black acrylic sheet.

Keeping these constraints in mind, I decided to make a phone stand that looked like a mini easel (example below - source: Instacart.com). I knew that my design and laser cut shapes would need to have slots to fit together since I didn't want to use hinges or other joinery.

<img width="300" alt="image" src="https://github.com/user-attachments/assets/075d1a9d-2a86-4eca-8698-e1a4bb270e82">

I found a laser cut template online ([link](https://community.glowforge.com/t/picture-stand/10458)), which I converted into something cut-able in Adobe Illustrator.

<img width="300" alt="" src="assets/September_5/first_phone_stand_illustrator_file.png">

I experimented with cutting out a bunch of different sizes of the template before landing on a size that supported my own phone well.

Laser cutter trial and error:

<img width="300" alt="" src="assets/September_5/phone_stand_different_sizes.jpeg">

A decent-sized phone stand:

<img width="300" alt="" src="assets/September_5/first_phone_stand.jpeg">

I even tested it with Lauryn's phone (kind of a fail):

<img width="300" alt="" src="assets/September_5/phone_stand_trial.jpeg">

There was room for improvement. For one, due to the lack of back support, the stand was front-heavy. It also didn't support different sizes of phones very well. Cody (design specialist) suggested adding some back support to my design and showed me an example of a laptop stand he had cut for himself which informed my second iteration.

<img width="300" alt="" src="assets/September_5/laptop_stand_inspo.jpeg">

I decided to modify the original template to better suit these needs. I extended the design to make it symmetrial (adding back support), and adjusted the size of the slots (adding wiggleroom to make the stand narrower or wider) I also made the curved ends a little longer so that the phone wouldn't slide out as easily. The result was the following:

<img width="300" alt="" src="assets/September_5/final_phone_stand.jpeg">

Side by side of prototype stages:

<img width="300" alt="" src="assets/September_5/prototype_stages.jpeg">

Flat:

<img width="300" alt="" src="assets/September_5/prototype_stages_flat.jpeg">

Much improved! 

Reflections:
Overall, I was able to practice iteration and prototyping through this exercise. I really enjoyed it. I think something I could improve on is prototyping a little more rapidly and giving myself a timebox (I could iterate on this design forever). 

I still need to find more users to test this version with. 

I also got started with some Rhino tutorials, but I have a lot more to go through before I start to feel comfortable (I probably could have redirected some of the laser cutting time to learning Rhino). 

Speculations:
For future versions, I want to try 3d-printing a similar design with a material that grips the phone better, like rubber. One of my goals before the weekend is to 3d print something simple!








