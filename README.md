# Online Code Editor Website

A simple web-based code editor that allows users to write and preview HTML, CSS, and JavaScript code in real-time. This tool is ideal for experimenting with code snippets and learning web development.

## Features

- **Live Preview:** See the results of your HTML, CSS, and JavaScript code in real-time.
- **Multiple Editors:** Separate text areas for HTML, CSS, and JavaScript input.
- **Responsive Design:** The editor is designed to be responsive and user-friendly.

## Technologies Used

- **HTML:** Structure of the web page.
- **CSS:** Styling and layout of the editor.
- **JavaScript:** Functionality for live code preview and updating.

## Setup and Installation

To run this project locally, follow these steps:

1. **Clone the Repository:**
   ```sh
   git clone https://www.github.com/rvrakash17/Online-Code-Editor-Website.git
   cd Online-Code-Editor-Website
   ```

2. **Open the Project:**
   - Open the `index.html` file in a web browser to view and use the code editor.

3. **Dependencies:**
   - Ensure that you have an internet connection to load any external resources if required.

## Code Explanation

### HTML

- **Structure:** Defines the layout of the code editor, including text areas for HTML, CSS, and JavaScript, and an iframe for the live preview.

### CSS

- **Styling:** Provides styling for the text areas and iframe to ensure a clean and usable interface.

  ```css
  body {
    text-align: center;
  }

  textarea {
    width: 32%;
    float: top;
    min-height: 250px;
    overflow: scroll;
    margin: auto;
    display: inline-block;
    background: #F4F4F9;
    outline: none;
    font-family: Courier, sans-serif;
    font-size: 14px;
  }

  iframe {
    bottom: 0;
    position: relative;
    width: 100%;
    height: 35em;
  }
  ```

### JavaScript

- **Functionality:** Handles the live preview of the code by updating the iframe with the content from the HTML, CSS, and JavaScript text areas.

  ```javascript
  function compile() {
    var html = document.getElementById("html");
    var css = document.getElementById("css");
    var js = document.getElementById("js");
    var code = document.getElementById("code").contentWindow.document;
    
    document.body.onkeyup = function(){
      code.open();
      code.writeln(html.value + "<style>" + css.value + "</style>" + "<script>" + js.value + "<\/script>");
      code.close();
    };
  }

  compile();
  ```

## Usage

1. **Enter Code:**
   - Input your HTML code into the HTML text area.
   - Input your CSS code into the CSS text area.
   - Input your JavaScript code into the JavaScript text area.

2. **Live Preview:**
   - The iframe will automatically update and display the live preview of your code as you type.

## Author
- Akash R
