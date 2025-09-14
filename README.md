# Mean-Variance-Standard Deviation Calculator

This project is a Python-based calculator that computes the mean, variance, standard deviation, max, min, and sum for a 3x3 matrix formed from a list of 9 numbers. It processes the data along rows (axis 1), columns (axis 0), and the entire flattened array. The project includes unit tests and is designed for development and testing.

## Project Structure

- `main.py`: Entry point for running the calculator and unit tests.
- `mean_var_std.py`: Core module containing the `calculate` function.
- `test_module.py`: Unit tests for the `calculate` function.
- `requirements.txt`: Dependencies (NumPy).

## Requirements

- Python 3.6+
- NumPy (version 1.18.5 as specified)

Install dependencies:
```
pip install -r requirements.txt
```

## Usage

### Running the Calculator

1. Ensure you have the required dependencies installed.
2. Run the entry point:
   ```
   python main.py
   ```
   This will:
   - Calculate statistics for the example list `[0,1,2,3,4,5,6,7,8]`.
   - Output the results as a dictionary.
   - Automatically run the unit tests.

Example output for `[0,1,2,3,4,5,6,7,8]`:
```
{
    'mean': [[3.0, 3.0, 3.0], [0.0, 3.0, 6.0], 3.0],
    'variance': [[3.0, 3.0, 3.0], [3.0, 3.0, 3.0], 3.0],
    'standard deviation': [[1.7320508075688772, 1.7320508075688772, 1.7320508075688772], [1.7320508075688772, 1.7320508075688772, 1.7320508075688772], 1.7320508075688772],
    'max': [[6, 7, 8], [2, 5, 8], 8],
    'min': [[0, 1, 2], [0, 3, 6], 0],
    'sum': [[9, 9, 9], [3, 9, 15], 27]
}
```

### Running Unit Tests Only

To run tests without the example calculation:
```
python -m unittest test_module
```

The tests validate the `calculate` function against expected outputs for sample inputs and handle edge cases (e.g., invalid list length).

## Function Details

The `calculate` function in `mean_var_std.py`:
- **Input**: A list of exactly 9 numbers.
- **Raises**: `ValueError` if the list doesn't have 9 elements.
- **Output**: A dictionary with keys `'mean'`, `'variance'`, `'standard deviation'`, `'max'`, `'min'`, and `'sum'`. Each value is a list of three lists: column stats, row stats, and overall stats.

It uses NumPy for efficient matrix operations.

## Development

- Start by reading this README.md.
- Modify `mean_var_std.py` for changes to the calculation logic.
- Add new tests in `test_module.py`.
- Run `python main.py` to test changes.

## Instructions

For building and extending this project, refer to the freeCodeCamp guide: [Mean-Variance-Standard Deviation Calculator](https://www.freecodecamp.org/learn/data-analysis-with-python/data-analysis-with-python-projects/mean-variance-standard-deviation-calculator).

## License

This project is part of the freeCodeCamp curriculum and is open for educational use.
