## Expected Behavior
Intellij IDEA highlights a line (or first symbol in a line), where **Indentation** issue is found.
Hoovering mouse over highlighted area shows tooltip with the issue description.

Below is screenshot with correct highlighting and issue description from **SpacingAroundParens** rule.
![Correct spacing around parens highlighting](docs/correct_spacing_highlighting.png)

## Observed Behavior
Whole file content is highlighted, making it impossible to find violation (including other types of rules).
Hoovering mouse over random place of file shows correct violation description, but its impossible to find its location.

Below is screenshot with the problem from testing project to reproduce the issue.
![Incorrect indentation highlighting](docs/incorrect_indentation_highlighting.png)

## Steps to Reproduce
- Download and build test project: https://github.com/godiale/detekt-indentation-highlighting-issue
- Install detekt IntelliJ plugin and configure it as below:
    - Enable Detekt = Y
    - Enable Formatting rules = Y
    - Build upon the default configuration = N
    - Enable all experimental rules = N
    - Treat detek findings as errors = N
    - Configuration file = https://github.com/godiale/detekt-indentation-highlighting-issue/blob/main/config/detekt.yml
    - Baseline File = <empty>
    - Plugin jars = <empty>



## Context
<!-- How has this issue affected you? What are you trying to accomplish? -->
<!-- Providing context helps us come up with a solution that is most useful in the real world -->

## Your Environment
<!-- Include as many relevant details about the environment you experienced the bug in -->
* Version of detekt used: 1.15.0
* Version of detekt IntelliJ plugin used: 1.6.1
* Version of Gradle used (if applicable): 6.7
* Operating System and version: Windows 10 Pro
* Version of IntelliJ IDEA: Community 2020.3.1 Build #IC-203.6682.168, built on December 29, 2020
* Runtime version: 11.0.9.1+11-b1145.63 amd64
* Link to your project (if it's a public repository): https://github.com/godiale/detekt-indentation-highlighting-issue
