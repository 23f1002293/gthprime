# Nth Prime Number Generator

## Summary

This is a minimal, single-page web application that calculates the nth prime number. A user can input a positive integer 'n' into a form or provide it as a URL query parameter (`?n=...`) to find the corresponding prime number. The application's background is styled with a specific image.

## Setup

No installation or build process is required. Simply download the following files into the same directory:

1.  `index.html`
2.  `Login.png` (You will need to provide this image)

Then, open `index.html` in any modern web browser.

## Usage

There are two ways to use the application:

1.  **Interactive Form:**
    *   Open `index.html`.
    *   Enter a positive integer into the input field labeled "Enter a positive integer (n):".
    *   Click the "Find nth Prime" button.
    *   The result will be displayed below the button.

2.  **URL Parameter:**
    *   Append `?n=<number>` to the URL in your browser's address bar.
    *   For example: `file:///path/to/your/folder/index.html?n=100`
    *   The page will automatically calculate and display the result for the given 'n' on load.

## Code Explanation

### `index.html`

The entire application is contained within this single file.

*   **HTML Structure**: A standard HTML5 document containing a `main` element that centers a form on the page. The form includes a number input, a submit button, and a paragraph tag (`<p>`) to display the result.
*   **CSS**: Embedded within a `<style>` tag. It sets `Login.png` as the full-screen background image and provides basic styling for centering content, the input form, and the result text to ensure readability against the background.
*   **JavaScript**: Embedded within a `<script>` tag.
    *   `isPrime(num)`: An efficient function to check if a given number is prime. It handles small numbers and then uses an optimized loop (stepping by 6) to check for factors.
    *   `getNthPrime(n)`: The core logic function. It iterates through numbers, using `isPrime` to count primes until it finds the nth one.
    *   `handleFormSubmit(event)`: Prevents the default form submission, reads the input value, validates it, calls `getNthPrime`, and displays the result or an error message in the designated result paragraph.
    *   **Event Listeners**: 
        *   An event listener on the form's `submit` event triggers the calculation when the button is clicked.
        *   A `DOMContentLoaded` listener runs when the page first loads. It checks for an `n` parameter in the URL and, if found, automatically triggers the calculation.

## Version Update Information

*   **Date**: 2023-10-27
*   **Version**: 1.1.0
*   **Changes**: 
    *   Updated the application background to use `Login.png`.

## License

MIT License

Copyright (c) 2023

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
