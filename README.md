# Cruise Ships 🛳️
Cruise Ships OOP/TDD exercise as part of CommandShift Bootcamp Syllabus

The project had the aim of taking some requirements, and translating them into object-oriented code. 

This involved developing the requirements into a domain model, which could then be used to form classes for objects which could interact with eachother.

## Requirements / User Stories

* As a cruise ship captain, So I can get passengers aboard a ship, I want a ship to have a starting port.
* As a cruise ship captain, So I can get passengers started on their journey, I want a ship to be able to set sail from a port.
* As a cruise ship captain, So I can get passengers to a new destination, I want a ship to be able to dock at a different port.
* As a tour representative, So I can decide which destinations passengers visit, I want a ship to take an itinerary which determines at which port it next docks.
* As a port operations manager, So I can best utilise a port, I want a port to keep track of the ships currently docked.

## Project Structure
.
├── __tests__
│   ├── itineary.test.js
│   ├── port.test.js
│   └── ship.test.js
├── package-lock.json
├── package.json
└── src
    ├── Itinerary.js
    ├── Port.js
    └── Ship.js

The ``__tests__`` directory contains the test suites for each of the 3 classes contained within the ``src`` directory

## Classes
### Port 🌊

The port object is instantiated with a name and an empty array of ships

**Methods:**

An ``addShip()`` method to add a ship object to the array of ships (called when a ship docks at a particular port)

A ``removeShip()`` method to remove a ship object from the array of ships (called when a ship sets sail from a particular port)

### Itinerary 📜

On instantiation, this object is passed an array of Port objects which make up the itinerary

### Ship 🛳️
The ship object is instantiated with an itinerary, a current port (the port in the itinerary which exists at index 0), a previous port (set to null), and the current port has the instantiated ship instance added to it.

**Methods:**

A ``setSail()`` method which sets previous port property equal to the current port, and then sets the current port property equal to null

A ``dock()`` method which sets the current port property equal to the next port in the itinerary, and adds the ship to that port

## Testing

This project was developed using a test-driven development approach, and Jest was used as the testing framework, with each class having its own test suite devoted to it.

Test doubles were used, to ensure each test suite was testing the functionality and behaviour specific to each particular class. 

The types of test doubles used were: 

* Mocks
* Spies
* Stubs
