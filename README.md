


<div align="center">
  <table border="0" cellpadding="0" cellspacing="0">
    <tr>
      <td align="center" style="background: #ffffff; border: 1px solid #d0d7de; border-radius: 12px; padding: 16px; box-shadow: 0 4px 12px rgba(0,0,0,0.05);">
        <img src="https://github.com/user-attachments/assets/02f9cc35-67cc-4b0f-b1e4-8fe01dd9a036" width="100%" max-width="800px" alt="Rough Layout For The PCB" style="border-radius: 6px;" />
        <div style="margin-top: 12px; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif; font-size: 13px; color: #57606a; font-weight: 500;">
      </td>
    </tr>
  </table>
</div>



|Title | CNC Router |
|:-- |:--|
|Author | Sadrita Neogi|




## Overview

It's an hobby grade CNC router made fully from scratch that uses linear rails , extrusion rods and much more..

### Why I chose this project?
Behind choosing this project was when I make any project, sometimes mostly, I get all the parts 3-D printed, but for some specific project 3-D printed parts are two week for them, and then I need to done it. CNC milling and the cost of CNC milling is too much, so I thought one day. Why not I just made one CNC router for myself that I can be used to build my projects, much more efficiently.
### How to use this project
Use case of this project can be many. The main thing that we can do with this CNC router is CNC milling making our custom parts for rockets for robotic arms that can be printed but if we make it out of metal, then the overall structure of the project will be more rigid, and that can be good for our long run.


## Features

* Fully Enclosed Frame Acrylic panels + wooden walls keep the working area good  and make it look cool.

* 775 Spindle Motor Cheap and capable for PCB milling.

* Linear Rails For smoother motion and better rigidity than ender 3d printer-style wheels.

* Limit Switches So the machine can actually zero itself instead of guessing.

* Electronics Bay Dedicated compartment for the controller, motor driver, and power supply.

* 700 x 500 + working are for the CNC milling

## Setup

Once the machine is assembled and wired, firmware needs to be installed so that it can move.

### Flashing GRBL onto the Arduino
GRBL is the firmware which is going to run on the Arduino and interpret the G-code commands. The installation is fairly simple.

1. **Download the Arduino IDE** from their site, a program which allows to flash the Arduino with firmware.
2. **Download GRBL source code** `.zip` file from the GitHub repository: https://github.com/gnea/grbl/releases and unzip the grbl file.  
**Note:** Before we proceed, we need to modify the `config.h` file inside grbl to account for the lack of the Z axis.
3. **Open Arduino IDE and import the grbl file** via: `Sketch` -> `Include Library` -> `Add .ZIP Library...` *(it says .ZIP but the uncompressed file should be chosen)*.
4. **Navigate to the grblUpload sketch** via: `File` -> `Examples` -> `grbl` -> `grblUpload`.
5. **Connect the Arduino to the PC via USB** *(make sure the correct board and port is selected)*.
6. **Flash the sketch** through `Sketch` -> `Upload`.

### For more about the CNC shield - [DOC Link](https://mikroshop.ch/pdf/CNC-Shield-Guide.pdf)
---

### Connecting the Arduino to LaserGRBL
Connecting the Arduino to LaserGRBL (through which I will control the laser) is fairly simple.

1. **Download LaserGRBL** from their website: https://lasergrbl.com and install it.
2. **Connect the Arduino to the computer via USB**.
3. **Choose the correct port** and select **"115200" baud rate**, then click **Connect**.  

If the console shows `Grbl 1.1h`, the chip is connected.

##  Now for sending the G- Code to the Arduino I will use universal Gcode Sender 

**https://github.com/winder/Universal-G-Code-Sender**

- official website - https://winder.github.io/ugs_website/

- It is an open source software, which is used to control CNC machines to send G code to them and to use it



|  |  | CAD WORK |  |  |
| :-: | :-: | :-: | :-: | :-: |
| <img src="https://github.com/user-attachments/assets/7860b64f-466d-40dc-8343-575fc86575a3" width="250" alt="CAD Work 4" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/ab023fcb-871d-4c58-a92f-3c4bc75a7769" width="250" alt="CAD Work 7" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/3037593c-aa03-492a-9dce-ab86404577b0" width="250" alt="CAD Work 9" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/522ee632-376f-4e40-97b7-edaea035a7e8" width="250" alt="CAD Work 11" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/c46c9228-7af2-4ab5-848b-ec6a5d0b74ea" width="250" alt="CAD Work 14" style="border-radius: 12px;" /> |
| <img src="https://github.com/user-attachments/assets/39e22ca8-7502-4e30-96eb-7e4e9b784800" width="250" alt="CAD Work 18" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/7fe63c1a-5bb6-4eb1-a07d-311874dae0aa" width="250" alt="CAD Work 21" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/2e0e50d0-d1e3-4181-bf7a-fc22fcf3a9b4" width="250" alt="CAD Work 25" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/ddbef16a-62c9-40f3-840b-48ac252a87be" width="250" alt="CAD Work 27" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/6facc3ee-d9e8-40ae-b736-ff80694b6178" width="250" alt="CAD Work 30" style="border-radius: 12px;" /> |
| <img src="https://github.com/user-attachments/assets/7f5e3594-4530-41ff-96ef-fea678031a81" width="250" alt="CAD Work 31" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/104b6725-ebd1-4f84-b1ba-b7d81ee0c4b8" width="250" alt="CAD Work 35" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/93804ce7-e02c-421a-b69f-76ff7b4b66cd" width="250" alt="CAD Work 36" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/827b152e-820c-4c61-8b1e-4b143521a237" width="250" alt="CAD Work 39" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/8c1b876c-f40f-4bbb-9829-841ee55361ed" width="250" alt="CAD Work 41" style="border-radius: 12px;" /> |
| <img src="https://github.com/user-attachments/assets/0ad9bd95-44cb-4450-9883-99b1fe69130e" width="250" alt="CAD Work 43" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/7d5426b0-1b20-45b6-a692-510eb064086d" width="250" alt="CAD Work 44" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/ecb0a888-b69d-4333-99c7-a7cc215e2f38" width="250" alt="CAD Work 46" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/347ecd9f-0895-47bd-8971-a99f66cbc8cf" width="250" alt="CAD Work 49" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/98d13908-f166-495b-8bcd-68cfbd393f96" width="250" alt="CAD Work 50" style="border-radius: 12px;" /> |
| <img src="https://github.com/user-attachments/assets/bb35e172-96c1-4ad4-9603-902117b0db14" width="250" alt="CAD Work 53" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/81b0107d-e182-467e-affb-784f417f3cf0" width="250" alt="CAD Work 54" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/f5c7c24b-c923-4a34-94b1-772594895a91" width="250" alt="CAD Work 57" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/011b314f-5d41-4d5c-9c44-e72ae4400088" width="250" alt="CAD Work 58" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/e657382f-18e5-4e5e-b4c9-2685d682a061" width="250" alt="CAD Work 60" style="border-radius: 12px;" /> |
| <img src="https://github.com/user-attachments/assets/2557fe90-84b0-4383-9e0e-c96fd82e4d24" width="250" alt="CAD Work 62" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/b64bac4b-1ba0-4c51-a72d-b2a06569a473" width="250" alt="CAD Work 64" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/19810d2a-b466-40bd-b543-d41262be8dc5" width="250" alt="CAD Work 65" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/98235f93-2d72-4228-8029-327abc5af8ec" width="250" alt="CAD Work 66" style="border-radius: 12px;" /> | <img src="https://github.com/user-attachments/assets/3f864b5a-8c7b-454e-b5d7-32727ca9c340" width="250" alt="CAD Work 68" style="border-radius: 12px;" /> |


## Fusion Renders 

<img width="2940" height="1272" alt="Render 1" src="https://github.com/user-attachments/assets/1ef3da53-ea16-4466-8b3b-5830f38c0289" />

<img width="2940" height="1272" alt="Render 2" src="https://github.com/user-attachments/assets/1c019c9f-1f8e-4d0a-8b9e-b107a7cfd616" />

<img width="2940" height="1272" alt="Render 3" src="https://github.com/user-attachments/assets/ecfb869e-7967-4c35-bf26-b499b521f1c6" />

<img width="2940" height="1272" alt="Render 4" src="https://github.com/user-attachments/assets/cd18caa0-eb5b-4ef6-b84e-7323e4185d5d" />
