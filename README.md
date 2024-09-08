
# Intro

Hi! I'm an MDes student at Berkeley, learning how to make cool things and keeping track of my progress here!

[Week 1](README.md#week-1-example-report-1)


---

# Week 2: September 6-12, 2024 #

Part 1: Playing around with Rhino/Grasshopper

Attempting to break down the example cell phone stand Rhino/Grasshopper files into a more digestible format. The FigJam flowchart shows all of the elements that go into making the cell phone stand. The yellow triangles represent adjustable parameters (important!)

<img alt="" src="assets/Week_2/Cell phone stand - with context.jpg">

On a quest to gain more understanding around what was happening in the example file, I began playing around with the previews and parameters. Initially, I didn't understand how two spheres + a box were used to construct the phone stand. When I turned on the previews for each shape, I saw how the intersections of the shapes led to the shape of the stand. 

<img alt="" src="assets/Week_2/two spheres preview.png">

I also didn't understand what the purpose of the cylinder void was. But when I changed the cylinder radius to 0 and baked the geometry, I saw why it was important in reducing the print volume.

<img alt="" src="assets/Week_2/zero cylinder radius baked.png">

I wanted to see a full view of the stand along with the relevant elements - the table, the student, and the phone - so I turned on the booleans for all of them.

<img alt="" src="assets/Week_2/Setup with context.png">

I tried adjusting the radii of the spheres to see the minimum required sizes to still create a feasible phone stand. Something that I was curious about was why we needed two spheres to create the phone stand - it seemed like one would suffice. To test my hypothesis, I set the radius of the top sphere to 0. The software told me that the assembly was still good. 

<img alt="" src="assets/Week_2/zero radius sphere.png">

I tried baking this configuration and produced a much smaller stand which seemed compatible with the phone centroid and angle, and would print quicker due to the reduced volume. However, we're not accounting for the weight of the phone in the assembly check, so maybe the smaller stand wouldn't work in this regard. We'd only be able to tell by printing!

<img alt="" src="assets/Week_2/baked zero radius sphere.png">


# Week 1: August 30 - September 5, 2024 #

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

I still need to find more users to test this version with. 

For future versions, I want to try 3d-printing a similar design with a material that grips the phone better.

Overall, I was able to practice iteration and prototyping through this exercise. I really enjoyed it. I think something I could improve on is prototyping a little more rapidly and giving myself a timebox (I could iterate on this design forever).

I also got started with some Rhino tutorials, but I have a lot more to go through before I start to feel comfortable (I probably could have redirected some of the laser cutting time to learning Rhino). 

One of my goals before the weekend s to 3d print something simple!








