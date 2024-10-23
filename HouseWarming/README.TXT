Java Programming Exercise: Heating System for a House

Objective:

You’ll build a system to manage heating in a house with multiple rooms. 
Each room can have its temperature adjusted, and the boiler should adapt its power based on the heating needs of the rooms.

Key Concepts:

House: Contains rooms and a boiler. Initially, the house has neither.

Room: Has a name and size (m³). Each room has its own radiator.

Boiler: Heats water to warm the rooms. It has limited power, which determines how much heat it can provide.

Radiator: Each room’s radiator communicates with the boiler through a thermostat to regulate the room temperature.
(EXTRA) If a room has a higher temperature demanded than the other rooms, the Radiator should be turned off. 

Thermostat: Connected to the Boiler of the house.

Tasks:

You should be able to:
Set the temperature of individual rooms using their names.
Change the temperature of all rooms at once.

Boiler: 

Properties
    - Has a maximum power. 
    
Implementation  
  
    - The boiler's power must follow this formula:
      power = desired_temperature * roomSize

(EXTRA)  
    - If a room’s heating requirement exceeds the boiler’s capacity, 
      return the maximum achievable temperature for that room.
    
    - Ensure that the power value is not exceeded. (this can be achieved making use of an if-else statement)
      If the power needed exceeds the boiler's maximum power, 
      the system should limit the temperature based on the boiler’s capacity.

House:
Properties
    - rooms (this will be a list, therefor make use of import java.util.ArrayList; )
    - boiler

Implementation
    - A house starts without any rooms and boiler.
    - When a room is added, the boiler should be given to the thermostat
      of the radiator of that room. (see for-loop)
    - When a boiler is added, all thermostats should be updated to use the new boiler. (see for-loop)

Room:

Properties
    - Name.
    - Size (m³).

Radiator:

Properties:
    - Thermostat
    - Temperature

Implementation:

    - Communicates with Thermostat to set up temperature

Thermostat:
Properties
    - Boiler
Implementation
    - Communicates with the boiler to adjust the room’s temperature.
    - Initially, not connected to any Boiler, only once the room is given to the house 
      the Boiler should be given to the Thermostat

How to Start:
Create Basic Classes:
    - Start with classes that do not depend on others, such as Boiler.
    - Define its constructor (e.g., to set maxPower), and add methods to calculate the 
      required power based on the room’s size and temperature.

Add Dependent Classes:
    - After building independent classes, create the classes that depend on others 
      (like Room, which contains a Radiator that uses a Thermostat).

Progressively Build the System:
    - Continue this process until all classes are implemented, 
      managing the interactions between the house, rooms, and the boiler.


This exercise will help you practice object-oriented programming, class dependencies, 
and handling constraints such as the boiler’s maximum power.

IF-ELSE statement

if(condition){
    //code to be executed
}else{
    //code to be executed
}


FOREACH-loop

for(Object o : Objects){
    //code to be executed
}


If at any point you struggle with these concepts,
go to https://chat.openai.com/ create an account and ask for help.










 
