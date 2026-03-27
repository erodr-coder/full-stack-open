```mermaid
sequenceDiagram
    participant browser
    participant server

    Note right of browser: JavaScript prevents default form submission and renders the new note submission immediately to the page

    browser ->> server: POST /new_note_spa
    server -->> browser: 201 Created {"message":"note created"}
```