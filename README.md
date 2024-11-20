# s21_math

## Chapter I: Introduction

In this project, we have developed our own version of the standard `math.h` library in the C programming language. This library implements a range of basic mathematical operations, which are integral to various algorithms. The project serves as a practical exercise to learn computational methods and reinforces the principles of structured programming.

---

## Chapter II: Information

### About `math.h`

C mathematical operations are a set of functions included in the standard library of the C programming language. These functions work primarily with floating-point numbers and are integral to many computational tasks. Functions that operate on angles use **radians** as the unit of measurement.

### Overview of Implemented Functions

| No. | Function                                   | Description                                                    |
|-----|-------------------------------------------|----------------------------------------------------------------|
| 1   | `int s21_abs(int x)`                      | Computes the absolute value of an integer value               |
| 2   | `long double s21_acos(double x)`          | Computes arc cosine                                           |
| 3   | `long double s21_asin(double x)`          | Computes arc sine                                             |
| 4   | `long double s21_atan(double x)`          | Computes arc tangent                                          |
| 5   | `long double s21_ceil(double x)`          | Returns the nearest integer not less than the given value     |
| 6   | `long double s21_cos(double x)`           | Computes cosine                                               |
| 7   | `long double s21_exp(double x)`           | Returns e raised to the given power                          |
| 8   | `long double s21_fabs(double x)`          | Computes absolute value of a floating-point value            |
| 9   | `long double s21_floor(double x)`         | Returns the nearest integer not greater than the given value  |
| 10  | `long double s21_fmod(double x, double y)`| Remainder of floating-point division operation               |
| 11  | `long double s21_log(double x)`           | Computes natural logarithm                                    |
| 12  | `long double s21_pow(double base, double exp)` | Raises a number to the given power                       |
| 13  | `long double s21_sin(double x)`           | Computes sine                                                 |
| 14  | `long double s21_sqrt(double x)`          | Computes square root                                          |
| 15  | `long double s21_tan(double x)`           | Computes tangent                                              |

---

## Chapter III: Implementation Details

### Part 1: Implementing `math.h` Functions

The following steps were followed to implement the `math.h` library functions:

#### Requirements
1. **Programming Language and Standards**:
   - The library is written in **C11** standard using the **gcc compiler**.
   - Only modern and POSIX.1-2017 compliant constructs and functions are used.

2. **Structure and Naming**:
   - The code is located in the `src/` folder on the `develop` branch.
   - Functions are prefixed with `s21_` to avoid conflicts.

3. **Coding Guidelines**:
   - The project follows **Google C style guidelines**.
   - Structured programming principles are strictly adhered to, avoiding code duplication.

4. **Library Type**:
   - The library is implemented as a **static library** with a `s21_math.h` header file.

5. **Testing**:
   - **Unit Testing**: Functions are tested using the **Check library**, comparing results with the standard `math.h`.
   - Tests cover at least **80% of each function** (verified using `gcov`).
   - **Accuracy**: Functions maintain **16 significant digits** overall and **6 decimal places** in the fractional part.

6. **Makefile**:
   - The project includes a `Makefile` with the following targets:
      - `all`: Builds the library and tests.
      - `clean`: Cleans all build files.
      - `test`: Runs the unit tests.
      - `s21_math.a`: Builds the static library.
      - `gcov_report`: Generates a code coverage report in **HTML format**.

7. **Prohibitions**:
   - The standard `math.h` library is not used in the implementation (except for comparisons in tests).

---

### Build and Run Instructions

1. **Clone Repository**:
   ```bash
   git clone git@github.com:le0ruslan/math-library.git
   cd <math-library/src>
   ```
2. **Build the Project**:
   ```bash
   make all
   ```


3. **Run Tests**:
   ```bash
   make test
   ```


4. **Generate Coverage Report**:
   ```bash
   make gcov_report
   ```


5. **Clean Build Files**:
   ```bash
   make clean
   ```


---

### Unit Test Coverage

* All functions are tested for accuracy and behavior in various edge cases.
* Coverage is ensured using gcov with a minimum threshold of 80% per function.