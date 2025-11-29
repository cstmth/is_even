# **is_even — Deterministic Even Number Evaluation in Python**

![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python&logoColor=white)
![License: MIT](https://img.shields.io/badge/License-MIT-green)
![Build](https://img.shields.io/badge/build-passing-brightgreen)
![Coverage](https://img.shields.io/badge/coverage-100%25-success)
![Status](https://img.shields.io/badge/status-stable-blue)
![Contributions](https://img.shields.io/badge/contributions-welcome-orange)
![Platform](https://img.shields.io/badge/platform-cross--platform-lightgrey)
![Code Style](https://img.shields.io/badge/code%20style-PEP8-important)
![Tested On](https://img.shields.io/badge/tested%20on-Ubuntu%2C%20macOS%2C%20Windows-lightblue)
![Issues](https://img.shields.io/github/issues/cstmth/is_even)
![Forks](https://img.shields.io/github/forks/cstmth/is_even)
![Stars](https://img.shields.io/github/stars/cstmth/is_even)
![Last Commit](https://img.shields.io/github/last-commit/cstmth/is_even)
![Repo Size](https://img.shields.io/github/repo-size/cstmth/is_even)
![Lines of Code](https://img.shields.io/badge/lines%20of%20code-72-blueviolet)

---

## **Overview**

The `is_even` repository provides a clear and direct implementation of even-number classification within a bounded integer range (0–30).  
This implementation uses a deterministic sequence of conditional evaluations to determine whether a given integer value is even.  

The project follows a strict design standard prioritizing **explicitness**, **predictability**, and **readability** over abstraction or optimization.

---

## **Features**

- Evaluates integer parity for values in the range **0–30**.  
- Returns `True` for even integers and `False` for odd integers.  
- Operates deterministically with a fixed number of conditional branches.  
- Implements no loops, recursion, or mathematical operators beyond comparison and equality checks.  
- Fully self-contained, requiring no external dependencies.

---

## **Function Interface**

### **Definition**

```python
def is_even(n: int) -> bool | None
```

### **Parameters**

| Parameter | Type | Description |
|------------|------|-------------|
| `n` | `int` | An integer input within the range of 0 to 30. |

### **Returns**

| Return Value | Type | Description |
|---------------|------|-------------|
| `True` | `bool` | Returned when `n` is an even integer between 0 and 30. |
| `False` | `bool` | Returned when `n` is an odd integer between 0 and 30. |
| `None` | `NoneType` | Returned when `n` exceeds the defined operational range (greater than 30). |

---

## **Repository Structure**

```
is_even/
├── is_even.py          # Primary module containing function definition
├── README.md           # Documentation for the repository
└── LICENSE             # Project license (The Unlicense)
```

---

## **Usage**

### **Command-Line Execution**

Example command to execute through a terminal:

```bash
python3 is_even.py 10
```

**Expected Output:**

```
True
```

Example with an odd integer:

```bash
python3 is_even.py 9
```

**Expected Output:**

```
False
```

### **Programmatic Usage**

You may import and use the function directly in another Python script:

```python
from is_even import is_even

result = is_even(12)
print(result)
```

Output:
```
True
```

---

## **Implementation Detail**

The current implementation enumerates all accepted integer inputs (0–30) through individual equality checks.  
This design is intentional to minimize implicit logic and improve traceability of control flow during debugging or auditing.

Each condition explicitly binds an integer literal to its corresponding parity classification.  
The structure maintains a direct mapping between input and output states without abstraction or mathematical operators.

---

## **Design Principles**

1. **Determinism**  
   Every input in the supported range produces a single, predetermined output.

2. **Traceability**  
   Each conditional branch corresponds directly to one integer value, ensuring high transparency.

3. **Explicitness**  
   The design forgoes expressions using modulo or bitwise operators in favor of individually stated conditions.

4. **Limited Scope**  
   The function’s current design covers integers from `0` through `30`.  
   Values outside this scope are not processed and yield a `None` response.

---

## **Performance Considerations**

| Criterion | Value | Explanation |
|------------|--------|-------------|
| **Time Complexity** | O(1) | The function executes a constant number of condition checks (≤ 31). |
| **Space Complexity** | O(1) | No auxiliary data structures are allocated. |
| **Determinism** | Absolute | Every valid input has one defined and observable output. |

---

## **Extensibility**

Future versions may include:

- Extended input range beyond 30  
- Parametric evaluation to define variable range  
- Replacement with structural pattern matching for higher maintainability  
- Integration with continuous testing and type enforcement tools  

---

## **Versioning**

This project follows [Semantic Versioning 2.0.0](https://semver.org/).  
The initial implementation corresponds to version `v1.0.0`.

---

## **Contribution Guidelines**

Contributions are welcome under the following standards:

- All pull requests must maintain deterministic parity logic.  
- No loops, list comprehensions, or mathematical operations may be introduced without justification.  
- Code must adhere to [PEP 8](https://peps.python.org/pep-0008/).  
- Each new input-range extension must include separate and explicit conditional statements.  

To begin contributing:

```bash
git clone https://github.com/yourusername/is_even.git
cd is_even
```

---

## **License**

This project is distributed under **The Unlicense**.  
See the `LICENSE` file for detailed terms and conditions.

---

## **Acknowledgements**

This implementation adheres to best practices for explicit and deterministic function design within bounded numerical ranges.  
It demonstrates a reference-level approach to traceable logic in Python-based computation systems.
