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
- **Shape/Type:** Hat shape (curved top, notch on the bottom)
- **What It Does:** Starts a script or program when a specific event happens (like pressing start or receiving a message). It always goes at the very top of a stack.
- **Example:** `when started`

### Stack / Command Block
- **Name:** Stack / Command Block
- **Shape/Type:** Rectangular with a notch on top and a bump on the bottom
- **What It Does:** Tells the robot to perform a specific action. It connects above and below other blocks to execute commands step-by-step.
- **Example:** `drive for [200] mm`

### C-Block
- **Name:** C-Block (Control Block)
- **Shape/Type:** Shaped like the letter "C"
- **What It Does:** Holds other command blocks inside its loop or frame to repeat or conditionally run them.
- **Example:** `repeat [4]` or `if < > then`

### Reporter / Oval Block
- **Name:** Reporter Block
- **Shape/Type:** Oval / Rounded ends
- **What It Does:** Reports or holds a value (like a number, text, or distance reading) and drops inside other blocks that accept inputs.
- **Example:** `distance from [Distance Sensor] in mm`

### Boolean / Hexagonal Block
- **Name:** Boolean Block
- **Shape/Type:** Hexagonal (pointed ends)
- **What It Does:** Reports a condition that can only be `TRUE` or `FALSE`. Fits into hexagonal slots inside control blocks like `if then` or `wait until`.
- **Example:** `<Bumper Pressed?>`

### Repeat Block
- **Name:** Repeat Block
- **Shape/Type:** C-shaped control block
- **What It Does:** Runs any commands placed inside its "C" body a set number of times.
- **Example:** `repeat [4]` to drive in a square.

### Wait Until Block
- **Name:** Wait Until Block
- **Shape/Type:** Stack block with a hexagonal input slot
- **What It Does:** Pauses the program's execution on that line until the Boolean condition in its slot becomes `TRUE`.
- **Example:** `wait until <Bumper Pressed?>`

### If Then Block
- **Name:** If Then Block
- **Shape/Type:** C-shaped control block (with a hexagonal slot for a condition)
- **What It Does:** Checks a Boolean condition; if it is `TRUE`, it runs the code inside the C-shape. If `FALSE`, it skips the inside code.
- **Example:** `if <Distance in mm < 200> then [turn right 90 deg]`

### Forever Block
- **Name:** Forever Block
- **Shape/Type:** C-shaped block without a bottom notch (it never ends)
- **What It Does:** Repeats the code inside it continuously for as long as the project runs.
- **Example:** `forever` checking sensor inputs to stop the robot from bumping into walls.

---

## Concepts

### Sequence
- **What It Means:** The specific order in which instructions are given to a computer or robot.
- **In My Own Words:** Code runs top-to-bottom. If you swap the steps, the robot does things out of order and fails the task.
- **Example:** Telling a robot to `drive forward` then `turn right` gets you to a different spot than `turn right` then `drive forward`.

### Parameters
- **What It Means:** Inputs or values passed into a command block to change how it executes.
- **In My Own Words:** The adjustable numbers or options inside a block that tweak what the robot actually does.
- **Example:** In `drive for [200] mm`, changing `200` to `500` changes the distance parameter.

### Loops / Iteration
- **What It Means:** Repeating a sequence of code multiple times or indefinitely.
- **In My Own Words:** Doing the same instructions again without having to write out the same blocks over and over.
- **Example:** Using a `repeat 4` block to draw a square instead of stacking 4 sets of drive and turn blocks.

### Sensors
- **What It Means:** Hardware devices that gather real-time data about the robot's surrounding environment.
- **In My Own Words:** The robot's eyes, ears, and sense of touch so it knows what's happening around it.
- **Example:** A Bumper Sensor detecting physical contact with a wall.

### Booleans & Conditions
- **What It Means:** A True/False evaluation used to control decision-making logic in code.
- **In My Own Words:** Asking a simple yes-or-no question so the robot can decide what step to take next.
- **Example:** Checking if `<Bumper Pressed?>` yields `TRUE` (pressed) or `FALSE` (not pressed).

### Sense → Think → Act
- **What It Means:** The fundamental robotics control loop where a robot reads sensors, processes data, and responds.
- **In My Own Words:** First gather info (Sense), figure out what it means using code (Think), then move or react (Act).
- **Example:** Distance sensor sees wall (Sense) -> code sees distance < 50 mm (Think) -> motors stop (Act).

### Comparisons
- **What It Means:** Evaluating two numerical values using math operators like `<` (less than) or `>` (greater than).
- **In My Own Words:** Comparing two numbers to see which is bigger, which outputs a `TRUE` or `FALSE` result.
- **Example:** `< (Distance in mm) < (100) >` evaluates to `TRUE` if an object gets closer than 100 mm.

### Coordinates
- **What It Means:** A numerical system using X and Y values to mark precise locations on a grid map.
- **In My Own Words:** X measures left/right and Y measures up/down so the robot knows its exact map position.
- **Example:** Moving the VR robot to location (X: 0 mm, Y: 400 mm).

### Conditionals
- **What It Means:** Programming structures (like `if-then`) that execute code blocks only when certain conditions are met.
- **In My Own Words:** Making a decision in code—"If this happens, then do that."
- **Example:** `If <Eye Sensor sees Red> then [Stop driving]`.

### Patterns
- **What It Means:** Identifying repeated sequences or behaviors to simplify code and design better algorithms.
- **In My Own Words:** Spotting identical steps in a challenge so you can use a loop or clean function instead of repeating blocks.
- **Example:** Realizing a maze involves "drive forward, turn right" four times in a row.

---

## Vocabulary

<details>
<summary><strong>1. VR Robot + Playground</strong></summary>

**Definition:**  
A VR Robot is a virtual robot programmed inside a simulation environment. A Playground is the 3D virtual arena where the VR Robot drives and interacts.

**In My Own Words:**  
The VR Robot is the digital bot you code, and the Playground is the map or field it moves around in.

**Example:**  
Loading the "Grid Map" Playground to test your VR Robot's movement algorithms.

</details>

<details>
<summary><strong>2. Programming Language + Project</strong></summary>

**Definition:**  
A Programming Language is a set of rules and syntax used to give instructions to a computer. A Project is the file containing the organized code blocks for a specific task.

**In My Own Words:**  
The language is how you speak to the robot (like VEXcode blocks), and the project is your saved file.

**Example:**  
Opening your VEXcode Blocks project to program a maze-navigating robot.

</details>

<details>
<summary><strong>3. Behavior + Command</strong></summary>

**Definition:**  
A Behavior is an overall action performed by the robot (e.g., turning around). A Command is an individual instruction block that tells the robot to execute a step.

**In My Own Words:**  
A command is a single line of code, while a behavior is the bigger action created by running commands.

**Example:**  
`turn right 90 degrees` is a command; driving in a circle is a complex behavior.

</details>

<details>
<summary><strong>4. Drivetrain</strong></summary>

**Definition:**  
The system of motors, wheels, and gears that enables a robot to move around its environment.

**In My Own Words:**  
The wheels and motors that make the robot drive, turn, and back up.

**Example:**  
Configuring the Drivetrain in VEXcode to set wheel travel and track width.

</details>

<details>
<summary><strong>5. Loop + Iteration</strong></summary>

**Definition:**  
A Loop is a structure that repeats code. An Iteration is one single complete pass through that loop.

**In My Own Words:**  
The loop is the repeat block itself, and iteration is counting each cycle through the loop.

**Example:**  
In a `repeat 4` block, finishing the square requires 4 total iterations.

</details>

<details>
<summary><strong>6. Sensor + Bumper Sensor</strong></summary>

**Definition:**  
A Sensor detects environmental inputs. A Bumper Sensor is a physical switch that detects physical contact when bumped.

**In My Own Words:**  
A sensor collects info, and a bumper sensor specifically tells the robot when it hits an obstacle.

**Example:**  
A Bumper Sensor sends a signal to stop the drivetrain the instant the robot bumps a wall.

</details>

<details>
<summary><strong>7. Boolean + Condition + TRUE/FALSE</strong></summary>

**Definition:**  
A Boolean is a data type with only two states: TRUE or FALSE. A Condition is a statement checked by code that returns a Boolean value.

**In My Own Words:**  
A condition asks a question, and the Boolean result is the TRUE or FALSE answer.

**Example:**  
Checking if `<Bumper Pressed?>`: if pressed, the state is TRUE; otherwise, it is FALSE.

</details>

<details>
<summary><strong>8. Distance Sensor + Threshold</strong></summary>

**Definition:**  
A Distance Sensor uses light/ultrasonic waves to report the distance to an object. A Threshold is a set numerical value used to trigger an action when crossed.

**In My Own Words:**  
The sensor measures distance, and the threshold is the cutoff line for taking action.

**Example:**  
Setting a threshold of 150 mm so the robot turns whenever the distance sensor reads less than 150 mm.

</details>

<details>
<summary><strong>9. Coordinate Plane + X/Y Coordinates</strong></summary>

**Definition:**  
A Coordinate Plane is a 2D grid used for mapping position. X-axis and Y-axis are horizontal and vertical reference lines, while X/Y coordinates pinpoint exact locations.

**In My Own Words:**  
A grid map where X measures horizontal location and Y measures vertical location.

**Example:**  
The center of the VR playground grid plane sits at position (X: 0 mm, Y: 0 mm).

</details>

<details>
<summary><strong>10. Location Sensor</strong></summary>

**Definition:**  
A sensor that reads the robot’s current X and Y position and heading angle relative to the Playground grid.

**In My Own Words:**  
The robot's built-in GPS that tells it its exact spot on the map.

**Example:**  
Using the Location Sensor to check if X < 500 mm before making a turn.

</details>

<details>
<summary><strong>11. Comment</strong></summary>

**Definition:**  
A text note added inside the project code to explain what the program does; it is ignored by the robot during execution.

**In My Own Words:**  
Notes you leave in your code for yourself or teammates to explain how things work.

**Example:**  
Adding a comment block reading `// Drive to first obstacle` above a section of movement blocks.

</details>

<details>
<summary><strong>12. Eye Sensor</strong></summary>

**Definition:**  
An optical sensor that detects whether an object is present and can identify specific colors (such as Red, Green, Blue, or Black).

**In My Own Words:**  
A color-picker sensor that lets the robot see objects and detect what color they are.

**Example:**  
Using the Down Eye Sensor to detect when the robot reaches a red line on the floor.

</details>

<details>
<summary><strong>13. Conditional Statement</strong></summary>

**Definition:**  
A programming instruction (like `if-then` or `if-then-else`) that performs different actions depending on whether a condition evaluates to TRUE or FALSE.

**In My Own Words:**  
A block that lets your code make decisions on the fly depending on what's happening.

**Example:**  
Using an `if-then-else` statement to drive forward if the path is clear, or turn if an obstacle appears.

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
