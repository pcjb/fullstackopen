Exercise 0.6: New note in single page app diagram

```mermaid
sequenceDiagram
    participant browser
    participant server

    Note right of browser: The browser adds the new note to the notes list
    Note right of browser: The browser re-renders the notes list
    
    browser-->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa<br/>{"content":"Yet another note","date":"2023-12-12T15:28:38.216Z"}
    activate server
    server-->>browser: {"message":"note created"}
    deactivate server

    Note right of browser: The browser prints the JSON received from the server to the console
```