```mermaid
sequenceDiagram
    participant browser
    participant server

    browser ->> server: GET /spa
    server -->> browser: 200 HTML document

    browser ->> server: GET main.css
    server -->> browser: 200 CSS

    browser ->> server: GET spa.js
    server -->> browser: 200 JavaScript

    note right of browser: The browser executes the JavaScript code that fetches the JSON data from the server

    browser ->> server: GET data.json
    server -->> browser: 200 JSON

    note right of browser: The browser renders the notes to the page

```