### Sparse Matrix Operations Project

#### Project Overview

The Sparse Matrix Operations project is designed to provide a user-friendly command-line interface for performing basic matrix operations (addition, subtraction, and multiplication) on sparse matrices. Sparse matrices are matrices in which most elements are zero, and they are commonly used in scientific computing and various applications where memory efficiency is crucial.

This project includes the following functionalities:

1. **Reading Sparse Matrices from Files**:
   - The program reads two sparse matrices from user-specified files. The matrices are stored in a compressed format where only non-zero elements are saved, along with their row and column indices.
   
2. **Performing Matrix Operations**:
   - Users can select one of three operations to perform on the matrices:
     - **Addition**: Adds the corresponding elements of two matrices.
     - **Subtraction**: Subtracts the corresponding elements of the second matrix from the first matrix.
     - **Multiplication**: Multiplies two matrices using the dot product method, if the matrices are dimensionally compatible.
   
3. **Writing Results to Files**:
   - The results of the operations are written to predefined output files. The output includes the dimensions of the resulting matrix and the non-zero elements in a format similar to the input.

4. **User Interaction**:
   - The program provides a continuous loop for user interaction, allowing the user to:
     - Input new file paths for different matrices.
     - Perform multiple operations on the same matrices.
     - Choose whether to perform additional operations or input new matrices.

#### Detailed Functionality

1. **Reading Matrices**:
   - The program reads the matrix files which contain the dimensions (number of rows and columns) and the non-zero elements with their respective positions.
   - Example of input format:
     ```
     rows=4
     cols=5
     (0, 1, 3)
     (1, 0, 4)
     (2, 2, 5)
     ```

2. **Matrix Operations**:
   - **Addition and Subtraction**: These operations are straightforward element-wise operations. They require the matrices to have the same dimensions.
   - **Multiplication**: This operation requires the number of columns in the first matrix to match the number of rows in the second matrix. The result is a matrix where each element is computed as the dot product of the corresponding row from the first matrix and the column from the second matrix.

3. **Output Format**:
   - The results are written to output files in a similar format to the input files, ensuring consistency and easy readability.
   - Example of output format:
     ```
     rows=4
     cols=5
     (0, 1, 3)
     (1, 0, 4)
     (2, 2, 5)
     ```

4. **User Interaction Loop**:
   - The program interacts with the user through the command line, providing prompts to input file paths and select operations.
   - After performing an operation, the user is given the option to perform another operation on the same matrices or input new matrices.

#### Sample Interaction

```
Please enter the path to the first matrix file: C:\path\to\first\matrix.txt
Please enter the path to the second matrix file: C:\path\to\second\matrix.txt
Select the operation you want to perform:
1. Addition
2. Subtraction
3. Multiplication
Enter the number corresponding to the operation: 1
Matrix 1: 4x5
Matrix 2: 4x5
Addition result has been written to C:\path\to\output\Addition_result.txt
Do you want to perform another operation? (yes/no): yes
Select the operation you want to perform:
1. Addition
2. Subtraction
3. Multiplication
Enter the number corresponding to the operation: 2
Matrix 1: 4x5
Matrix 2: 4x5
Subtraction result has been written to C:\path\to\output\Subtraction_result.txt
Do you want to perform another operation? (yes/no): no
Do you want to input new files? (yes/no): yes
Please enter the path to the first matrix file: ...
```

#### Implementation Details

The project is implemented in Python, utilizing classes and methods to handle sparse matrix operations efficiently. The `SparseMatrix` class encapsulates the functionality for reading matrices from files, performing operations, and writing results to files. Static methods are used for reading files to maintain clarity and separation of concerns.

This project is suitable for users needing to perform operations on large, sparse matrices efficiently and provides a clear and simple interface for interacting with the program.