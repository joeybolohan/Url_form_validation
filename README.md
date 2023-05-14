# URL Validation Form

This project provides a simple HTML form that validates if the input is a properly formatted URL. It uses JavaScript for the validation.

## How It Works

The URL validation form contains a text box where you can input a string. By clicking the "Validate URL" button, the application will check if the input string is a valid URL.

The validation is performed using JavaScript's built-in URL constructor. This constructor is designed to parse and manipulate URLs, and it will throw an error if you attempt to create a new URL object with an invalid URL string.

Here's the main function of the script:

``` function validateURL() {
    var urlInput = document.getElementById('url').value;
    try {
        new URL(urlInput);
        alert("Valid URL");
    } catch (_) {
        alert("Invalid URL");
    }
}
```
When you click the "Validate URL" button, this function gets the value of the text box and attempts to construct a new URL object from that string. If the URL constructor can successfully create a URL object, the function alerts that the URL is valid. If the URL constructor throws an error (indicating that the URL is invalid), the function catches that error and alerts that the URL is invalid.

## How to Use

Open the HTML file in a web browser.
Input a string into the text box.
Click the "Validate URL" button to check if the string is a valid URL.
Note: This validator will accept any string that can be successfully parsed into a URL object by JavaScript's URL constructor, which covers a wide range of valid URLs. However, it will not provide detailed error messages about what part of the URL is incorrect, as the URL constructor does not provide such information when it throws an error.
