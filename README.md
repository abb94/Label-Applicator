# 🏷️ Automated Label Applicator

The goal for this project is to make a cheap and automated DIY Label Applicator for small bottles and flasks with adjustable size, relative to the bottle placed on the device. 


---

## 📚 Table of Contents

- [Introduction](#-introduction)
- [Requirements](#-requirements)
- [Features](#-features)
- [Hardware](#-hardware)
- [Software](#-software)
- [Installation](#-installation)
- [Design Files](#-design-files)
- [Roadmap](#-roadmap)
- [Log](#-log)
- [Learnings](#-learnings)

---

## 🔍 Introduction


This project was created for a friend who is passionate about honey farming. In 2024, his bee colonies produced nearly half a ton of honey. Since each bottle contains roughly half a kilo, that’s about 1,000 bottles to label by hand — a task that’s both time-consuming and far from the most enjoyable part of beekeeping. Commercial automatic label applicators are notoriously expensive, so this project aims to develop a more affordable alternative.


---

## ‼️: Requirements

- [ ] Easy to move around. 
- [ ] Apply labels on different dimensions of glass and label sizes. 
- [ ] Easy to maintain.
- [ ] Easy to use.
- [ ] Semi-automatic and manual to operate. 

---

## ✨ Features

<!-- List the features, for example: automatic feed, sensor detection, calibration, etc. -->

---

## 🔩 Hardware

- 2 x 20 mm x 20 mm x 60 mm I-type profiles
- 3 x 20 mm x 20 mm x 15 mm I-type profiles


---

## 🧠 Software

<!-- Describe the software architecture, languages, frameworks, and any libraries used. -->

---

## ⚙️ Installation

<!-- Step-by-step guide to installing and running the project. Include wiring diagrams or schematics if relevant. -->

---

## 🖼️ Design Files

Current socket design: <br>

<img width="621" height="361" alt="Uden titel" src="https://github.com/user-attachments/assets/888745ba-e3ab-4d5b-b5f9-75ab3cf6bcaf" />


---

## 🧭 Roadmap

<!--
List completed tasks and planned features with checkboxes. Example:
- [x] Basic motor control
- [ ] Add web configuration
-->

---

## 📗: Log

### 7th of August 2025 <br>
Initially, my goal was to design the components so they could be inserted into the profile and held in place by a tight fit. However, since the profile measures only 20 mm × 20 mm, fitting them inside the I-profile sockets proved difficult and led to tolerance issues.
Considering I’ll be using T-nuts, this approach didn’t make much sense. Instead, I decided to design the components to fit an M4×10 mm screw, which can be tightened directly onto the profile — meaning only the nut will go into the sockets.


### 8th of August 2025 <br>
I have started designing the most fundamental parts for the applicator. <br>
- I have created the main roller
- A model for a honey glass
- A section for adjustable size, depending on the honey glass
- A mounting socket for quick testing, to figure out size requirements.

<br>
<img width="673" height="530" alt="image" src="https://github.com/user-attachments/assets/a071257f-f5be-479f-b65d-7165690b0790" />
<br>

I initially ordered a cheap rubber-coated paint roller from AliExpress and disassembled it to keep only the roller cylinder. I then sanded the edges, mounted the bearing, and found a suitable bearing socket on Thingiverse. This allowed me to test whether the bearing and cylinder could function as a roller for the glass (see the red cylinder in the picture).

<br>
<img width="673" height="530" alt="image" src="https://github.com/user-attachments/assets/d94a9a55-70c0-45e3-b1c3-cfa88fbf8da7" />
<br>

The cylinder I bought provided excellent grip on the glass, but its surface was too uneven. An uneven surface could cause frequent errors during the label application process. To address this, I plan to design my own 3D-printed cylinder and add a surface coating or material that increases friction between the glass and the cylinder.

### 17th of August 2025 <br>
I have scraped the previous idea by using a paint roller as the base, for the rolling mechanism of the label applicator. 
The reasoning for this are the following: 
- Approximately needing 3 cylinders with 30 mm in diamater and a length of approximately 140 mm, and additionally needing 4 x 20 mm cylinder with equal length to guide the label spool, would take a long time 3d printing.
- Furthermore, the filament required, would likely be quite high.

Therefore, I have found some old aluminum cylinders in different sizes, from an old moveable wardrobe I could use, as a base to create the cylinders. 
![Billede 1](https://github.com/user-attachments/assets/ec957acc-0a6e-4244-8dcf-dd2fbd8886dc)
![Billede 2](https://github.com/user-attachments/assets/6450b3e9-897a-4e62-b066-ac5fee6ddc57)

Furthermore, I have found a a default socket concept I will be using for the cylinders, where the socket fits perfectly on the profile and allows a tight fit for the bearing, while the bearing can still easily move. 
![Billede 4](https://github.com/user-attachments/assets/14e7646c-762e-411f-ae51-1720ac6849da)

###  8th of September 2025 <br>
I have ended on the design below, for the large rollers on the label applicator. 

<img width="986" height="615" alt="current design" src="https://github.com/user-attachments/assets/9ff043d8-c484-47b4-a8a3-37aa3648bd9c" />

I have 3D printed the current design and constructed the main frame with the two large rollers upon. 
![printed design](https://github.com/user-attachments/assets/9c9398a5-125c-46e3-b484-f33258dd831a)
Furthermore, due to the low amount of friction between the aluminum cylinder and the glass, I have bought some shrinking tape for the large cylinders (I do not expect this to be required for the small ones), which needs to be heat-treated with boiling water, to fit perfectly. This should create the necessary friction for the honey glass to roll smoothly. 

I also tried to put on the gears and connect the conveyer belt to a slow 12v dc motor I had laying around. As seen in the GIF below, the rotation seems acceptable for the time being, with the honey glass upon the two cylinders. <br>
![d397c6f3-438f-473a-9a5c-cbf6a5bd7c35-ezgif com-resize](https://github.com/user-attachments/assets/77382139-40dd-4ef4-87bc-367bd01ee646)

### 20th of September 2025 <br>
I fucked up. Since having iterated over several sockets and fits, I finally tried for an early-stage alpha test. 

I had iterated over sockets and fits. Sockets (The once mounted on the frame), had to be small enough, for the cylinders to touch - But still be sturdy enough to carry the load. 
In regards to the fit, it was required for them not to extend over the heatshrink, so that the heat shrink between two cylinders, could create friction between one another and "drag" the label spool through that space. 
Having iterated this several times, I forgot that I had adjusted some depths, which resulted in a wasted 6-hour 3D print and not being able to conduct an early-stage alpha test. 
- Learning? Standardize as much as possible, so that you don't iterate over several parts that serves a niche purpose. I could have created a socket in the beginning (and fit), which covered all my needs.
  
<img width="932" height="536" alt="20th of september" src="https://github.com/user-attachments/assets/62c18564-ebf2-4dad-9bfa-be4a5f6a33a9" />



### 3rd of October 2026 <br>

I have not worked on this project for a while now. Had to remove everything from my office and make it into a kids' room. 

I have contemplated about this project for a while now, and I will be re-designing the entire machine. 

When I tried to demo my machine, which I have not written about in this log, I noticed several issues. <br>
- I noticed spikes in required torque to keep the machine running. Because I am using DC motors and not stepper motors, I cannot reduce the rotations to increase torque, and therefore I can end up stalling the motors if increased force is applied for some reason (Example here is a full honey glass compared to an empty glass.
- My chosen IR sensors are not a good suit. IR sensors emit light and detects the same emitted light. My IR sensors reflects light upon an object, the object reflects it and the sensor detects it. However, the required compact build of the machine creates a placement of the glass and the object, which increases the error rate of object detection, to the small gap of tolerance that I can allow the sensors to have.

#### I will therefore make two changes to the build:
- Use 2 x low amp stepper motors
- shift from a reflective IR sensor to a transmissive IR sensor. <br>

Both seems like obvious choices a year later...

---
### 📄: Learnings
- Create a component as the first thing in Fusion 360. Create the body, and the sketch creating that body, and keep it inside the component.
- Tolerances are difficult on a 3d Printer.
- Standardize as much as possible, and don't create several parts from one origin, that fits a niche purpose. It is easier to have the original modified so that it coveres all requirements. 



---

