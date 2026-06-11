# Math Operations Parser

This is an old educational project that I built a long time ago at university, when I was practicing Java, string processing, recursion, and basic expression parsing. The repository remains as a small archival example of how I approached parsing and calculation tasks back then without using external libraries.

The repository contains two separate console programs:

- `MathOperationsParser.java` - a parser for mathematical expressions.
- `ResistanceOfElectricCircleParser.java` - a parser for calculating the equivalent resistance of an electric circuit.

## What The Project Does

### 1. `MathOperationsParser`

This program reads a mathematical expression from the console, removes spaces, performs basic input validation, and calculates the result.

Supported features:

- parentheses `(` `)`
- addition `+`
- subtraction `-`
- multiplication `*`
- division `/`
- decimal numbers using `.`

Example expression:

```text
(5+10*3.4)/10
```

Calculation approach:

1. The expression is split into tokens.
2. Parts inside parentheses are processed recursively.
3. Operations are executed in priority order:
   - `/`
   - `*`
   - `+`
   - `-`

### 2. `ResistanceOfElectricCircleParser`

This program is focused on simple electric circuit problems. It allows entering resistor values and calculating equivalent resistance for series and parallel connections.

Supported features:

- series connection with `+`
- parallel connection with `|`
- parentheses `(` `)`
- resistor notation using `R` or `r`

Example expression:

```text
(R10+R5)|R20|(R7+R3)
```

Calculation logic:

- `R10 + R5` means a series connection
- `R10 | R5` means a parallel connection
- parallel resistance is calculated using the formula:

```text
R = a*b/(a+b)
```

## How It Works

Both programs follow a simple idea:

- the user enters an expression in the console
- the string goes through basic validation
- the expression is split into parts
- nested expressions in parentheses are calculated recursively
- after that, operators are processed from left to right in the defined order

This is not a full mathematical engine or an industrial-grade parser. It is better described as a learning exercise in manual expression parsing.

## Repository Structure

```text
.
├── MathOperationsParser.java
└── ResistanceOfElectricCircleParser.java
```

## Running The Code

This is simple Java console code without a build system such as Maven or Gradle.

General launch idea:

```bash
javac Main.java
java Main
```

However, it is important to note that the repository preserves an old educational version of the code almost as-is. Because of that, before running it you may need to:

- align the `public class Main` name with the file name
- adjust package/import structure depending on your environment
- open the code in a simple Java IDE project and adapt it for modern execution

## Limitations

This project is educational in nature, so it has several intentional or historical limitations:

- very basic input validation
- no complete handling of all invalid input scenarios
- no tests
- no build, CI, or packaging
- the code reflects early learning-stage Java practice and is not intended to be production-quality

## Why This Repository Exists

This repository can be useful as:

- an example of early Java learning code
- a simple demonstration of recursive parenthesis handling
- an example of manual arithmetic expression parsing
- a small experiment for electric circuit resistance calculations

## Possible Improvements

If I ever return to this project, it could be improved by:

- extracting shared parsing logic into separate classes
- introducing a proper token model instead of working only with strings
- adding tests
- turning the project into a Maven or Gradle application
- adding support for unary minus, better validation, and clearer error messages

## Note

This README describes the repository as it exists now: an old university learning experiment, not a finished or actively maintained product.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
