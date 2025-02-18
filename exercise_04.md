##### User creates a new note on the page https://studies.cs.helsinki.fi/exampleapp/notes by writing something into the text field and clicking the Save button. 

```mermaid

sequenceDiagram
    participant browser
    participant server

    Note right of browser: User writes a note in the text field.
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note
    activate server
    server-->>browser: {"status": "success", "message": "Note saved!"}
    deactivate server

    Note right of browser: The browser updates the User Interface to show the new note.
```