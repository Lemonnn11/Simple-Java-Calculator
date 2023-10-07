# Input Domain Modeling

## Function: `calculateMono(MonoOperatorModes newMode, Double num)`

### Information

- Parameters: `MonoOperatorModes`, `Double`
- Return Type: `Double`
- Return Value: Calculation result depends on operator mode.
- Exceptional Behavior: `throw new Error();` if mode is invalid. 

### Testing Goal

The testing goal for the calculateMono function is to verify that it correctly performs various mathematical operations based on the provided `MonoOperatorModes` and input number `num`, ensuring accuracy, error handling, and edge case coverage.

### Interface-Based IDM

| Characteristics          | B1                      | B2    | B3                      |
|--------------------------|-------------------------|-------|-------------------------|
| C1: Mode is null         | True                    | False |                         |
| C2: Refinement of Number | Positive Decimal Number | Zero  | Negative Decimal Number |

### Functionality-Based IDM

| Characteristics                                      | B1               | B2                    | B3                         | B4            | B5            | B6            | B7            | B8           | B9                     | B10                |
|------------------------------------------------------|------------------|-----------------------|----------------------------|---------------|---------------|---------------|---------------|--------------|------------------------|--------------------|
| C1: Calculation Result Based On Different Operations | Result of Square | Result of Square Root | Result of Reciprocal (1/n) | Result of Cos | Result of Sin | Result of Tan | Result of Log | Result of Ln | Result of Rate (n/100) | Result of Absolute |

### Merging Characteristics

| Characteristics                                      | B1                      | B2                    | B3                         | B4            | B5            | B6            | B7            | B8           | B9                     | B10                |
|------------------------------------------------------|-------------------------|-----------------------|----------------------------|---------------|---------------|---------------|---------------|--------------|------------------------|--------------------|
| C1: Mode is null                                     | True                    | False                 |
| C2: Refinement of Number                             | Positive Decimal Number | Zero                  | Negative Decimal Number    |
| C3: Calculation Result Based On Different Operations | Result of Square        | Result of Square Root | Result of Reciprocal (1/n) | Result of Cos | Result of Sin | Result of Tan | Result of Log | Result of Ln | Result of Rate (n/100) | Result of Absolute |

### Relabel The Blocks

| Characteristics | B1 | B2 | B3 | B4 | B5 | B6 | B7 | B8 | B9 | B10 |
|-----------------|----|----|----|----|----|----|----|----|----|-----|
| A               | A1 | A2 |
| B               | B1 | B2 | B3 |
| C               | C1 | C2 | C3 | C4 | C5 | C6 | C7 | C8 | C9 | C10 |

### Combine Partitions

#### ACoC (60 Test Cases)

|       | COL1     | COL2     | COL3     | COL4     | COL5      |
|-------|----------|----------|----------|----------|-----------|
| ROW1  | A1 B1 C1 | A1 B1 C2 | A1 B1 C3 | A1 B1 C4 | A1 B1 C5  |
| ROW2  | A1 B2 C1 | A1 B2 C2 | A1 B2 C3 | A1 B2 C4 | A1 B2 C5  |
| ROW3  | A1 B3 C1 | A1 B3 C2 | A1 B3 C3 | A1 B3 C4 | A1 B3 C5  |
| ROW4  | A2 B1 C1 | A2 B1 C2 | A2 B1 C3 | A2 B1 C4 | A2 B1 C5  |
| ROW5  | A2 B2 C1 | A2 B2 C2 | A2 B2 C3 | A2 B2 C4 | A2 B2 C5  |
| ROW6  | A2 B3 C1 | A2 B3 C2 | A2 B3 C3 | A2 B3 C4 | A2 B3 C5  |
| ROW7  | A1 B1 C6 | A1 B1 C7 | A1 B1 C8 | A1 B1 C9 | A1 B1 C10 |
| ROW8  | A1 B2 C6 | A1 B2 C7 | A1 B2 C8 | A1 B2 C9 | A1 B2 C10 |
| ROW9  | A1 B3 C6 | A1 B3 C7 | A1 B3 C8 | A1 B3 C9 | A1 B3 C10 |
| ROW10 | A2 B1 C6 | A2 B1 C7 | A2 B1 C8 | A2 B1 C9 | A2 B1 C10 |
| ROW11 | A2 B2 C6 | A2 B2 C7 | A2 B2 C8 | A2 B2 C9 | A2 B2 C10 |
| ROW12 | A2 B3 C6 | A2 B3 C7 | A2 B3 C8 | A2 B3 C9 | A2 B3 C10 |

#### ECC (10 Test Cases)

|      | COL1     | COL2     | COL3     | COL4     | COL5      |
|------|----------|----------|----------|----------|-----------|
| ROW1 | A1 B1 C1 | A2 B2 C2 | A2 B3 C3 | A1 B1 C4 | A1 B1 C5  |
| ROW2 | A1 B1 C6 | A1 B1 C7 | A2 B2 C8 | A1 B1 C9 | A1 B1 C10 |

#### PWC (30 Test Cases)

|      | COL1     | COL2     | COL3      | COL4      | COL5      |
|------|----------|----------|-----------|-----------|-----------|
| ROW1 | A1 B1 C1 | A2 B2 C1 | A1 B3 C1  | A2 B1 C2  | A1 B2 C2  |
| ROW2 | A2 B3 C2 | A1 B1 C3 | A2 B2 C3  | A1 B3 C3  | A2 B1 C4  |
| ROW3 | A1 B2 C4 | A2 B3 C4 | A1 B1 C5  | A2 B2 C5  | A1 B3 C5  |
| ROW4 | A2 B1 C6 | A1 B2 C6 | A2 B3 C6  | A1 B1 C7  | A2 B2 C7  |
| ROW5 | A1 B3 C7 | A2 B1 C8 | A1 B2 C8  | A2 B3 C8  | A1 B1 C9  |
| ROW6 | A2 B2 C9 | A1 B3 C9 | A2 B1 C10 | A1 B2 C10 | A2 B3 C10 |

#### BCC (13 Test Cases)

Base Choice: A2 B1 C1

|      | COL1     | COL2     | COL3     | COL4      | COL5     |
|------|----------|----------|----------|-----------|----------|
| ROW1 | A2 B1 C2 | A2 B1 C3 | A2 B1 C4 | A2 B1 C5  | A2 B1 C6 |
| ROW2 | A2 B1 C7 | A2 B1 C8 | A2 B1 C9 | A2 B1 C10 | A2 B2 C1 |
| ROW3 | A2 B3 C1 | A1 B1 C1 |

#### MBCC (24 Test Cases)

Base Choice 1: A2 B1 C1

|      | COL1      | COL2     | COL3     | COL4     | COL5     |
|------|-----------|----------|----------|----------|----------|
| ROW1 | A1 B1 C1  | A2 B2 C1 | A2 B1 C2 | A2 B1 C3 | A2 B1 C4 |
| ROW2 | A2 B1 C5  | A2 B1 C6 | A2 B1 C7 | A2 B1 C8 | A2 B1 C9 |
| ROW3 | A2 B1 C10 |  

Base Choice 2: A2 B3 C1

|      | COL1      | COL2     | COL3     | COL4     | COL5     |
|------|-----------|----------|----------|----------|----------|
| ROW1 | A1 B3 C1  | A2 B2 C1 | A2 B3 C2 | A2 B3 C3 | A2 B3 C4 |
| ROW2 | A2 B3 C5  | A2 B3 C6 | A2 B3 C7 | A2 B3 C8 | A2 B3 C9 |
| ROW3 | A2 B3 C10 |

### Derived Test Values

#### Select Sample

- ACoC
    - Negative Square (A2 B3 C1)
    - Zero Cos (A2 B2 C4)
- ECC
    - Zero Ln (A2 B2 C8)
    - One Divide By Negative (A2 B3 C3)
- PWC
    - One Divide By Zero (A2 B2 C3)
    - Negative Ln (A2 B3 C8)
- BCC
    - Positive Tan (A2 B1 C6)
    - Positive Ln (A2 B1 C8)
- MBCC
    - Negative Rate (A2 B3 C9)
    - Negative Square Root (A2 B3 C2)

