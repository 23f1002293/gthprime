# Nth Prime Number Generator

## Summary

A minimal, single-page web application that calculates the nth prime number. The user can provide the integer 'n' either through an input field on the page or directly as a URL query parameter.

## Setup

No server or dependencies are required. This is a pure HTML/JavaScript application.

1.  Save the `index.html` file to your local machine.
2.  Open the `index.html` file in any modern web browser (e.g., Chrome, Firefox, Safari).

## Usage

There are two ways to use the application:

1.  **Via the Web Interface**:
    *   Open `index.html`.
    *   Enter a positive integer into the input field labeled "Enter n:".
    *   Click the "Generate" button.
    *   The result will be displayed below the button.

2.  **Via URL Parameter**:
    *   Append `?n=<value>` to the file path in your browser's address bar, where `<value>` is the positive integer you want to find the prime for.
    *   Example: `file:///path/to/your/index.html?n=100`
    *   The page will load and automatically calculate and display the result for the given 'n'.

## Code Explanation

*   **`index.html`**: The single file containing all the code.
*   **HTML Structure**: A basic HTML5 document with a `main` section. It includes a `form` with a number input and a submit button. A `div` with the ID `result` is used to display the output.
*   **JavaScript Logic** (embedded in a `<script>` tag):
    *   **`isPrime(num)`**: A helper function that determines if a number is prime using trial division up to its square root. This is an efficient check for individual numbers.
    *   **`findNthPrime(n)`**: The core function. It iterates through integers, using `isPrime()` to check each one. It maintains a count of primes found and returns the number that corresponds to the nth prime.
    *   **Event Listeners**:
        *   An event listener for `DOMContentLoaded` is used to initialize the application once the page is fully loaded. It checks the URL for an 'n' parameter and, if found, triggers the calculation.
        *   An event listener on the form's `submit` event prevents the default page reload, retrieves the value from the input field, and calls the calculation function.
    *   **DOM Manipulation**: The script updates the `textContent` of the `#result` div to show the calculated prime number or any error messages.

## Version Update Information

*   **v1.0.0 (2023-10-27)**
    *   Initial release.
    *   Core functionality for calculating the nth prime number.
    *   Support for input via form and URL parameter.

## License

This project is licensed under the MIT License.