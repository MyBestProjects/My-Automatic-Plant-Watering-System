# My-Automatic-Plant-Watering-System
This project took several months to complete. I encountered four major issues, each causing significant problems. Here, I explain each issue and how I resolved them:

The first issue I encountered was the inability to add a second relay due to the presence of a state function. This required transitioning from one state to another, but I was unsure how to implement this in the code. To resolve this, I created a state called "fork," which allowed the system to determine whether to direct the flow to one water plant or the other.

The second issue I encountered was that the state 'fork' caused additional problems, leading to a breakdown of the entire system. This resulted in the code being disabled and stopping in the middle of execution. To address this, I implemented an if-else statement. This conditional structure checks whether the second relay needs to activate; if so, it will proceed to pour. If not, it will check whether the first relay needs to activate and proceed accordingly.

The third issue I encountered was that the second relay would not cooperate. I attempted to resolve this by changing some pins, but this did not work. After conducting research without finding a solution, I sought assistance on the Arduino Forum. A member named "runaway_pancake" identified the error: I had missed a pinMode declaration. Once I included the necessary pinMode configuration, the relay functioned correctly.

The fourth and final issue I encountered was that when I transitioned the ESP32 and all the other hardware, both relays would turn on whenever the first moisture sensor detected dryness. This problem caused a delay of approximately three days. Eventually, I identified the issue in the code: I needed to add a variable to determine when each relay should turn on or off.

This project involved:
1 Esp32
2 plants
2 moisture sensors
2 relays
2 water motors
2 watering pipes
2 battery packs
1 power bank
Some normal jumper wires
Some female and male jumper wires

 
