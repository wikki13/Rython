# Rython

<img src="man/figures/Rython_logo.webp" alt="Rython" width="200" align="center" style="margin-right: 15px;"/>


**Rython** is an R library designed to convert Python code to R code. 
It simplifies the process of translating Python scripts into their R equivalents, 
making it easier for users familiar with R to adapt Python code to R. 
The package provides a set of functions that map common Python constructs (e.g., imports, variables, functions) to their R counterparts.

## Features

- **Python to R Code Translation**: The core functionality of the package is to translate basic Python syntax into R, including variables, imports, functions, and basic control structures.
- **Import Translation**: The package converts Python's `import` statements to the appropriate R `library()` calls, making it easy to switch between Python and R libraries.
- **Variable Conversion**: Automatically converts Python variable assignments (e.g., `x = [1, 2, 3]`) into their R equivalents (e.g., `x <- c(1, 2, 3)`).
- **Function Definitions**: Translates Python function definitions into R function syntax, making it easier to adapt Python code into R.
- **Boolean and None Translation**: Converts Python booleans (`True`, `False`) and `None` into R equivalents (`TRUE`, `FALSE`, `NULL`).

## Installation

You can install the **Rython** package from CRAN (once available) or directly from GitHub using the `devtools` package:

```r
# Install from GitHub (Development version)
devtools::install_github("wikki13/Rython")

Installation
You can install the Rython package from CRAN (once available) or directly from GitHub using the devtools package:

R
Copy code
# Install from GitHub (Development version)
devtools::install_github("wikki13/Rython")
Usage
To use the package, simply load it and call the translate_python_to_r() function, passing the Python code you want to translate as a string.


# Example usage
library(Rython)

python_code <- "import numpy as np\nx = np.array([1, 2, 3])"
translated_code <- translate_python_to_r(python_code)

# View the translated R code
print(translated_code)
This will translate Python code like:

# Example output
library(Matrix)
x <- array(c(1, 2, 3))
```
## **Comparison: Rython vs Reticulate**

| Feature                       | **Rython**                                                                                          | **Reticulate**                                                                                  |
|-------------------------------|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| **Purpose**                  | Translates Python code into equivalent R code.                                                     | Enables Python code to be directly executed and integrated within R.                          |
| **Workflow Integration**     | Provides translated R code for use in native R environments.                                        | Embeds Python within R scripts or workflows, allowing both languages to coexist.              |
| **User Base**                | Ideal for Python developers migrating to R or needing a full conversion of Python scripts to R.     | Designed for users comfortable with using both Python and R simultaneously.                   |
| **Code Conversion**          | Converts Python syntax, functions, and libraries into R equivalents.                              | No conversion; Python code is executed as-is using an embedded Python interpreter.            |
| **Dependency Management**    | Independent of Python runtime; focuses solely on generating R code.                                | Requires a Python environment to run embedded Python code.                                    |
| **Examples of Use**          | Migrating Python scripts to R for long-term use, teaching, or adapting to R-native workflows.       | Combining Python and R in a single workflow, leveraging libraries from both ecosystems.       |
| **Learning Curve**           | Simplifies the process for users transitioning from Python to R.                                    | Requires familiarity with both Python and R for seamless integration.                         |


### Future Developments
- **Enhanced Syntax Support**: We plan to extend the package to handle more advanced Python constructs, such as classes, loops, and exception handling.
- **Bi-directional Translation**: Future versions will explore the possibility of translating R code back to Python, enabling a more seamless integration between both languages.
- **Improved Libraries Handling**: There are plans to support more Python libraries and their R equivalents for smoother transitions in scientific computing and machine learning projects.
- **Code Optimization**: Enhancing the speed and efficiency of code translation, especially when dealing with large Python scripts.

## **Contributing**

We welcome contributions! Check out our [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

## **License**

This project is licensed under the MIT License. See the [LICENSE](LICENSE.md) file for details.

