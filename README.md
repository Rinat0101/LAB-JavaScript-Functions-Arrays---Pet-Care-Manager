# LAB | JavaScript Functions & Arrays - Pet Care Manager

## Learning Goals
- Understand and apply Object-Oriented Programming principles in JavaScript.
- Utilize arrays to manage a collection of pet objects.
- Create dynamic HTML elements using DOM manipulation.
- Implement user interactivity with methods to feed, play, and care for pets.

## Introduction
Welcome to the Pet Care Manager lab! In this lab, you'll develop a web application that allows users to manage their virtual pets. You will learn to create classes, manipulate arrays, and use the DOM to enhance user interaction while having fun with pet care themes.

## Requirements
You will complete the following iterations, each focusing on specific programming skills.

### Iteration #1: Create a Pet Class
Implement a class called `Pet` that has:

**Properties:**
- `name`: The name of the pet.
- `happiness`: A number representing the pet's happiness level (0-100).
- `hunger`: A number representing how hungry the pet is (0-100).

**Methods:**
- `play()`: Increases happiness by a certain amount (e.g., 10).
- `feed()`: Decreases hunger by a certain amount (e.g., 10).

**Example:**
```javascript
class Pet {
    constructor(name) {
        this.name = name;
        this.happiness = 50; // Default happiness
        this.hunger = 50; // Default hunger
    }

    play() {
        this.happiness += 10;
    }

    feed() {
        this.hunger -= 10;
    }
}
```
## Iteration #2: Create a Pet Manager
Implement a class called `PetManager` that manages multiple pets:

### Properties:
- `pets`: An array of Pet objects.

### Methods:
- `addPet(pet)`: Adds a new pet to the array.
- `removePet(name)`: Removes a pet by name.
- `getPets()`: Returns the array of pets.

### Example:
```javascript
class PetManager {
    constructor() {
        this.pets = [];
    }

    addPet(pet) {
        this.pets.push(pet);
    }

    removePet(name) {
        this.pets = this.pets.filter(pet => pet.name !== name);
    }

    getPets() {
        return this.pets;
    }
}
```
## Iteration #3: Build the User Interface
Using the DOM, create a user interface that includes:
- Input fields for adding a new pet (name).
- Buttons to feed and play with pets.
- A display area to show all pets with their happiness and hunger levels.

## Iteration #4: Add Interactivity
Implement event listeners for:
- Adding a new pet and displaying it in the UI.
- Feeding or playing with a pet and updating the displayed values accordingly.

## Bonus #1: Persistent Data
Implement functionality to use `localStorage` to save the pet list so it persists even after refreshing the page.

## Bonus #2: Pet Status
Add a feature that shows the status of each pet based on happiness and hunger levels. If a pet's happiness drops below a threshold, display a warning message.

## Bonus #3: Custom Pet Types
Allow users to create different types of pets (e.g., Dog, Cat, Bird) that may have different starting happiness and hunger levels. Implement additional properties to differentiate them based on type.

## Submission
Upon completion, run the following commands in your terminal:
```bash
git add .
git commit -m "Completed Pet Care Manager Lab"
git push origin master
