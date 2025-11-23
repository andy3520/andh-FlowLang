# ANDH-FlowLang Specification

Version: 0.1.0 (Draft)

## Overview

ANDH-FlowLang is a structured natural-language dialect that enables expressing computational logic in a human-readable format while maintaining machine interpretability.

## Design Principles

1. **Clarity Over Brevity**: Prefer explicit, clear expressions over terse syntax
2. **Natural Flow**: Follow natural language patterns where possible
3. **Structured Flexibility**: Allow both rigid and flexible expression styles
4. **AI-First Design**: Optimize for AI understanding and execution

## Core Language Elements

### 1. Statements

ANDH-FlowLang uses declarative statements to express computations and control flow:

```
Define variable X as 10
Set Y to X plus 5
```

### 2. Conditions

Conditional logic uses natural language expressions:

```
If X is greater than Y:
    Do action A
Otherwise:
    Do action B
```

### 3. Iterations

Loops and repetitions use clear, natural phrasing:

```
For each item in collection:
    Process item

Repeat while condition is true:
    Perform action
```

### 4. Functions

Functions are defined using natural language patterns:

```
Define function calculate_sum with parameters A and B:
    Return A plus B
```

### 5. Data Types

ANDH-FlowLang supports basic data types expressed naturally:

- **Numbers**: `10`, `3.14`, `negative 5`
- **Text**: `"hello world"`, `'single quotes'`
- **Boolean**: `true`, `false`, `yes`, `no`
- **Collections**: `list of [1, 2, 3]`, `set of items`, `dictionary of {key: value}`, `empty dictionary`

### 6. Operations

Operations use natural language operators:

- **Arithmetic**: `plus`, `minus`, `times`, `divided by`
- **Comparison**: `equals`, `is greater than`, `is less than`
- **Logical**: `and`, `or`, `not`

## Comments

Comments are denoted with `#` or can be natural language notes:

```
# This is a comment
Note: This section handles input validation
```

## Example Program

```flowlang
# Simple number guessing game

Define secret_number as random number between 1 and 100
Define attempts as 0
Define guessed as false

Repeat while not guessed and attempts less than 10:
    Prompt user for guess
    Increment attempts by 1
    
    If guess equals secret_number:
        Output "Congratulations! You guessed it!"
        Set guessed to true
    Otherwise if guess is less than secret_number:
        Output "Too low, try again"
    Otherwise:
        Output "Too high, try again"

If not guessed:
    Output "Game over! The number was" secret_number
```

## Language Evolution

This specification is a living document. ANDH-FlowLang is designed to evolve based on practical usage and community feedback.

## Implementation Notes

Interpreters and transpilers for ANDH-FlowLang should:

1. Be tolerant of minor syntax variations
2. Provide clear error messages in natural language
3. Support both strict and lenient parsing modes
4. Maintain source location information for debugging

## Future Considerations

- Module and import system
- Exception handling patterns
- Async/concurrent operations
- Type system refinements
- Standard library definition
