# cruise-ships
Cruise Ships OOP/TDD exercise as part of CommandShift Bootcamp Syllabus

The project had the aim of taking some requirements, and translating them into object-oriented code. 

This involved developing the requirements into a domain model, which could then form classes for objects which could interact with eachother.

# Classes
Port

The port object is instantiated with a name and an empty array of ships
Methods: 

An addShip() method to add a ship object to the array of ships (called when a ship docks at a particular port)
A removeShip() method to remove a ship object from the array of ships (called when a ship sets sail from a particular port)

Itinerary: On instantiation, this object is passed an array of Port objects which make up the itinerary

Ship: The ship object is instantiated with an itinerary, a current port (the port in the itinerary which exists at index 0), a previous port (set to null), and the current port has the instantiated ship instance added to it.
Ship Methods: 

A setSail() method which sets previous port property equal to the current port, and then sets the current port property equal to null
A dock() method which sets the current port property equal to the next port in the itinerary, and adds the ship to that port


