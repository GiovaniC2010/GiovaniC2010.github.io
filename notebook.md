## Table of Contents

- [Blocks](#blocks)
- [Concepts](#concepts)
- [Vocabulary](#vocabulary)
- [Notebook Style Guide](#markdown-style-guide-for-coding-notebooks)
  - [Headings](#headings)
  - [Text Formatting](#text-formatting)

---

## Blocks

### Hat Block
- **Name:** Hat Block
- **Shape/Type:** Hat shape (rounded top, notch on the bottom)
- **What It Does:** Starts a script when a specific event triggers it. It always goes at the very top of a stack of blocks.
- **Example:** `when started`

### Stack / Command Block
- **Name:** Stack / Command Block
- **Shape/Type:** Rectangular with a notch on top and a bump on the bottom
- **What It Does:** Tells the robot to do a single action. It stacks top-to-bottom with other commands.
- **Example:** `drive [forward] for [200] mm`

### C-Block
- **Name:** C-Block (Control Block)
- **Shape/Type:** Shaped like the letter "C"
- **What It Does:** Holds other blocks inside its loop to repeat them or run them conditionally.
- **Example:** `repeat [4]` or `if < > then`

### Reporter / Oval Block
- **Name:** Reporter Block
- **Shape/Type:** Oval with rounded ends
- **What It Does:** Stores or measures a value (like numbers or sensor readings) and drops into inputs on other blocks.
- **Example:** `distance from [Distance Sensor] in mm`

### Boolean / Hexagonal Block
- **Name:** Boolean Block
- **Shape/Type:** Hexagonal with pointed sides
- **What It Does:** Checks a condition and returns either TRUE or FALSE. Fits inside hexagonal slots on control blocks.
- **Example:** `<Bumper Pressed?>`

### Repeat Block
- **Name:** Repeat Block
- **Shape/Type:** C-shaped control block
- **What It Does:** Runs any blocks placed inside it for a set number of times.
- **Example:** `repeat [4]` to draw a square or repeat a sequence.

### Wait Until Block
- **Name:** Wait Until Block
- **Shape/Type:** Stack block with a hexagonal input slot
- **What It Does:** Pauses the program on that exact line until its Boolean condition turns TRUE.
- **Example:** `wait until <Bumper Pressed?>`

### If Then Block
- **Name:** If Then Block
- **Shape/Type:** C-shaped control block (with a hexagonal slot for a condition)
- **What It Does:** Checks a condition. If it is TRUE, it runs the code inside. If FALSE, it skips right past it.
- **Example:** `if <Distance in mm < 200> then [turn right 90 deg]`

### Forever Block
- **Name:** Forever Block
- **Shape/Type:** C-shaped block without a bottom notch
- **What It Does:** Loops the code inside continuously until the project is manually stopped.
- **Example:** `forever` checking sensor inputs to keep from bumping walls.

---

## Concepts

### Sequence
- **What It Means:** The specific top-to-bottom order in which commands run.
- **In My Own Words:** If you change the order of your blocks, the robot will do steps out of order and miss its goal.
- **Example:** Driving forward then turning right gets you to a totally different spot than turning right first and then driving.

### Parameters
- **What It Means:** Values or settings passed into a block to change how it behaves.
- **In My Own Words:** The adjustable numbers or drop-down choices inside a block that control speed, distance, or angle.
- **Example:** Changing the number in `drive for [200] mm` to `500` changes how far the robot moves.

### Loops / Iteration
- **What It Means:** Repeating a block of code multiple times.
- **In My Own Words:** Running a set of instructions over and over without having to duplicate blocks in your workspace.
- **Example:** Wrapping a `drive` and `turn` block inside a `repeat [4]` loop instead of snapping eight blocks together.

### Sensors
- **What It Means:** Hardware that reads physical information from the environment.
- **In My Own Words:** The robot's eyes and touch tools that let it react to the world around it.
- **Example:** A Bumper Sensor detecting when the robot physically contacts a wall.

### Booleans & Conditions
- **What It Means:** A True/False evaluation used to make decisions in code.
- **In My Own Words:** Asking a basic yes-or-no question so the program knows what branch of code to execute.
- **Example:** Checking if `<Bumper Pressed?>` returns TRUE (pressed) or FALSE (not pressed).

### Sense → Think → Act
- **What It Means:** The standard robotics loop where a robot reads data, decides what to do, and executes a physical movement.
- **In My Own Words:** Read sensors (Sense), run code logic (Think), move motors (Act).
- **Example:** Eye sensor spots a wall (Sense) -> program evaluates distance < 50 mm (Think) -> motors stop driving (Act).

### Comparisons
- **What It Means:** Comparing two numerical values using math symbols like `<` or `>`.
- **In My Own Words:** Checking which number is larger or smaller to generate a TRUE or FALSE output.
- **Example:** `< (Distance in mm) < (100) >` outputs TRUE as soon as an obstacle gets closer than 100 mm.

### Coordinates
- **What It Means:** An X and Y grid system used to mark exact positions on a map.
- **In My Own Words:** X handles side-to-side positioning and Y handles up-and-down positioning on the playground field.
- **Example:** Driving the robot directly to position `(X: 0 mm, Y: 400 mm)`.

### Conditionals
- **What It Means:** Code structures (like `if-then`) that execute actions only when conditions are met.
- **In My Own Words:** Decision blocks—"If this sensor sees something, then perform this move."
- **Example:** `if <Eye Sensor sees Red> then [stop drivetrain]`.

### Patterns
- **What It Means:** Spotting repeated steps or behaviors to make code cleaner.
- **In My Own Words:** Finding actions that happen over and over so you can replace them with a loop.
- **Example:** Seeing that navigating a maze consists of repeating "drive, turn right" four times in a row.

---

## Vocabulary

<details>
<summary><strong>1. VR Robot + Playground</strong></summary>

**Definition:**  
A VR Robot is a virtual robot programmed in a simulation. A Playground is the 3D virtual field where the VR Robot runs.

**In My Own Words:**  
The VR Robot is the digital bot you program, and the Playground is the map or arena it moves around in.

**Example:**  
Opening the "Grid Map" Playground to test your robot's pathfinding code.

</details>

<details>
<summary><strong>2. Programming Language + Project</strong></summary>

**Definition:**  
A Programming Language is the syntax and rules used to give instructions to a computer. A Project is the saved file containing your organized code.

**In My Own Words:**  
The language is how you communicate with the robot (like VEXcode blocks), and the project is your saved code file.

**Example:**  
Saving your VEXcode Blocks project before running it in the simulator.

</details>

<details>
<summary><strong>3. Behavior + Command</strong></summary>

**Definition:**  
A Behavior is an overall action done by the robot. A Command is an individual instruction block that tells the robot what to do.

**In My Own Words:**  
A command is one single block, while a behavior is the bigger result you see when those commands run together.

**Example:**  
`turn right 90 degrees` is a command; weaving through an obstacle course is a behavior.

</details>

<details>
<summary><strong>4. Drivetrain</strong></summary>

**Definition:**  
The system of motors, wheels, and gears that allows a robot to drive and turn.

**In My Own Words:**  
The wheels and motors that control how the robot moves across the ground.

**Example:**  
Configuring the Drivetrain settings in VEXcode to match wheel size and width.

</details>

<details>
<summary><strong>5. Loop + Iteration</strong></summary>

**Definition:**  
A Loop is a structure that repeats code. An Iteration is one complete pass through that loop.

**In My Own Words:**  
The loop is the container block, and an iteration is counting each single turn through it.

**Example:**  
In a `repeat [4]` block, driving each side of a square counts as one iteration.

</details>

<details>
<summary><strong>6. Sensor + Bumper Sensor</strong></summary>

**Definition:**  
A Sensor gathers data from the environment. A Bumper Sensor is a physical switch that detects contact when bumped.

**In My Own Words:**  
A sensor reads surroundings, and a bumper sensor specifically detects physical crashes into objects.

**Example:**  
A Bumper Sensor signaling the robot to stop the instant it hits a wall.

</details>

<details>
<summary><strong>7. Boolean + Condition + TRUE/FALSE</strong></summary>

**Definition:**  
A Boolean is a data type with only two possible values: TRUE or FALSE. A Condition is a statement checked by code that outputs a Boolean.

**In My Own Words:**  
A condition asks a question, and the Boolean is the TRUE or FALSE answer that comes back.

**Example:**  
Checking `<Bumper Pressed?>`: if pressed it returns TRUE, otherwise FALSE.

</details>

<details>
<summary><strong>8. Distance Sensor + Threshold</strong></summary>

**Definition:**  
A Distance Sensor uses light/ultrasonic waves to report how far away an object is. A Threshold is a set target value used to trigger an action when crossed.

**In My Own Words:**  
The sensor measures distance, and the threshold is the specific cutoff distance where your robot reacts.

**Example:**  
Setting a threshold of 150 mm so the robot turns whenever the distance sensor reads less than 150 mm.

</details>

<details>
<summary><strong>9. Coordinate Plane + X/Y Coordinates</strong></summary>

**Definition:**  
A Coordinate Plane is a 2D grid mapping positions. X and Y coordinates pinpoint exact locations using horizontal (X) and vertical (Y) axes.

**In My Own Words:**  
A grid map where X tracks left/right movement and Y tracks up/down movement.

**Example:**  
The center of the VR playground grid sits at `(X: 0 mm, Y: 0 mm)`.

</details>

<details>
<summary><strong>10. Location Sensor</strong></summary>

**Definition:**  
A sensor that reads the robot's exact X and Y position and heading angle on the grid.

**In My Own Words:**  
The robot's built-in GPS that reports its exact spot on the map.

**Example:**  
Checking the Location Sensor to see if `X < 500 mm` before turning a corner.

</details>

<details>
<summary><strong>11. Comment</strong></summary>

**Definition:**  
A note added inside code to explain what sections do; it is completely ignored when the robot executes the program.

**In My Own Words:**  
Notes you leave in your project to remind yourself or partners how your code works.

**Example:**  
Placing a comment saying `// Search for green disk` above a search algorithm block.

</details>

<details>
<summary><strong>12. Eye Sensor</strong></summary>

**Definition:**  
An optical sensor that detects if an object is present and identifies colors like Red, Green, Blue, or Black.

**In My Own Words:**  
A color sensor that tells the robot what color object or line it is looking at.

**Example:**  
Using the Down Eye Sensor to stop driving when the robot sees a red line on the playground floor.

</details>

<details>
<summary><strong>13. Conditional Statement</strong></summary>

**Definition:**  
A programming structure (like `if-then` or `if-then-else`) that executes different actions depending on whether a condition is TRUE or FALSE.

**In My Own Words:**  
A block that lets your code make decisions based on changing conditions.

**Example:**  
Using an `if-then-else` statement to drive forward if the path is clear, or turn if an obstacle is in the way.

</details>

---

## Markdown Style Guide for Coding Notebooks
Follow this guide to keep your coding notebook **clear, consistent, and professional**.  
This ensures your notes are easy for you (and others) to read later.

---

## Headings
**When to use:** Organize your notebook into sections (like days, topics, or projects).  
- `#` for the notebook title (use once at the top).  
- `##` for each day or major topic.  
- `###` for subsections (like "Notes", "Practice", "Reflections").  

# Example:
# My Coding Notebook
## Day 1
### Notes
### Practice

# Text Formatting
When to use: Highlight important ideas or add emphasis.
Use bold for key terms or definitions.
Use italic for emphasis or side comments.
Use inline code for keywords, functions, or commands.

# Example:
**Class** = a blueprint for objects  
*Remember:* always test your code  
Use `System.out.println()` to print

# Code Blocks
When to use: Anytime you write multiple lines of code.
Inline code for short snippets.
Fenced code blocks with language for full examples.

# Example:
```java
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello World!");
    }
}
