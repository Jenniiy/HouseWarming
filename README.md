# Java Programming Exercise: Heating System for a House

## Objective:
You’ll build a system to manage heating in a house with multiple rooms. Each room can have its temperature adjusted, and the boiler should adapt its power based on the heating needs of the rooms.

## Key Concepts:

- **House**: Contains rooms and a boiler. Initially, the house has neither.
- **Room**: Has a name and size (m³). Each room has its own radiator.
- **Boiler**: Heats water to warm the rooms. It has limited power, which determines how much heat it can provide.
- **Radiator**: Each room’s radiator communicates with the boiler through a thermostat to regulate the room temperature.

- **Thermostat**: Connected to the boiler of the house.

## Tasks:

You should be able to:

1. Set the temperature of individual rooms using their names.
2. Change the temperature of all rooms at once.

## Boiler:

### Properties:
- Has a maximum power.
- Has current power needed to heat up rooms in house.

### Implementation:
- The boiler's power must follow this formula:
  ```java
    power = desired_temperature * roomSize
  ```

## House:

### Properties:
- `rooms` (this will be a list, therefore make use of `import java.util.ArrayList;`)
- `boiler`

### Implementation:
- A house starts without any rooms or boiler.
- When a room is added, the boiler should be given to the thermostat of the radiator of that room (see for-loop).
- When a boiler is added, all thermostats should be updated to use the new boiler (see for-loop).

## Room:

### Properties:
- `Name`
- `Size` (m³)
- `Radiator`

## Radiator:

### Properties:
- `Thermostat`
- `Temperature`

### Implementation:
- Communicates with the thermostat to set up the temperature.

## Thermostat:

### Properties:
- `Boiler`

### Implementation:
- Communicates with the boiler to adjust the room’s temperature.
- Initially, not connected to any boiler. Only once the room is given to the house, should the boiler be given to the thermostat.

## Unseen material needed

### IF-ELSE Statement:

```java
if (condition) {
    // code to be executed
} else {
    // code to be executed
}
```

### FOREACH- loop:

```java
for(className c : listName) {
  // code to be executed
}
```
### FOR-loop:
```java
for(int i = 0; i < list.size(); i++){
  // code to be executed
}
```

### Errors (EXTRA HARD):
#### NULLPointerException
you may encounter a NullPointerException if you try to change the 
temperature of a room with a house which has no boiler.
this can be handled by using a  `try-catch clause` such as;
```java
try
{
  /*
   * code that might throw a NullPointerException
   * if boiler is not initialized, then its value is NULL 
   * (which means it is not referencing any object in memory)
   */
  boiler.setTemp(roomSize,temp);
}
catch( NullPointerException e)
{
  System.out.println("No Boiler given to house");
}
```

## How to Start:

### Create Basic Classes:
- Start with classes that do not depend on others, such as `Boiler`.
- Define its constructor (e.g., to set `maxPower`), and add methods to calculate the required power based on the room’s size and temperature.

### Add Dependent Classes:
- After building independent classes, create the classes that depend on others (like `Room`, which contains a `Radiator` that uses a `Thermostat`).

### Progressively Build the System:
- Continue this process until all classes are implemented, managing the interactions between the house, rooms, and the boiler.

## This exercise will help you practice object-oriented programming, class dependencies, and handling constraints such as the boiler’s maximum power.