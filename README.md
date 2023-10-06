# Input Domain Modeling

## Function: `calculateMono(MonoOperatorModes newMode, Double num)`

### Information

- Parameters: `MonoOperatorModes`, `Double`
- Return Type: `Double`
- Return Value: Calculation result depends on operator mode.
- Exceptional Behavior: `throw new Error();` if mode is invalid. 

### Testing Goal

The testing goal for the calculateMono function is to verify that it correctly performs various mathematical operations based on the provided `MonoOperatorModes` and input number `num`, ensuring accuracy, error handling, and edge case coverage.

### Functionality-Based IDM

| Characteristics                                      | B1               | B2                    | B3                         | B4            | B5            | B6            | B7            | B8           | B9             | B10                |
|------------------------------------------------------|------------------|-----------------------|----------------------------|---------------|---------------|---------------|---------------|--------------|----------------|--------------------|
| C1: Calculation Result Based On Different Operations | Result of Square | Result of Square Root | Result of Reciprocal (1/n) | Result of Cos | Result of Sin | Result of Tan | Result of Log | Result of Ln | Result of Rate | Result of Absolute |

### Interface-Based IDM

| Characteristics          | B1                      | B2    | B3                      |
|--------------------------|-------------------------|-------|-------------------------|
| C1: Mode is null         | True                    | False |                         |
| C2: Refinement of Number | Positive Decimal Number | Zero  | Negative Decimal Number |

### Combine Partitions

*TO DO*

### Derived Test Values

*TO DO*

---

## Function: `calculateBI(BiOperatorModes newMode, Double num)`

### Information

- Parameters: `BiOperatorModes`, `Double`
- Return Type: `Double`
- Return Value: Calculation result depends on operator mode.
- Exceptional Behavior: `throw new Error();` if mode is invalid.

### Testing Goal

The testing goal for the calculateBi function is to ensure that it accurately performs mathematical operations based on the provided `BiOperatorModes`, input numbers `num1` and `num2`, and updates the object's internal state accordingly.

### Functionality-Based IDM

| Characteristics                                      | B1                 | B2                    | B3                       | B4                 | B5                     |
|------------------------------------------------------|--------------------|-----------------------|--------------------------|--------------------|------------------------|
| C1: Calculation Result Based On Different Operations | Result of Addition | Result of Subtraction | Result of Multiplication | Result of Division | Result of X Power of Y |

### Interface-Based IDM

| Characteristics          | B1                      | B2    | B3                      |
|--------------------------|-------------------------|-------|-------------------------|
| C1: Mode is null         | True                    | False |                         |
| C2: Refinement of Number | Positive Decimal Number | Zero  | Negative Decimal Number |

### Combine Partitions

*TO DO*

### Derived Test Values

*TO DO*