Exercise 4:

```mermaid
sequenceDiagram
    participant browser
    participant server

    browser-->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa
    activate server
    server-->>browser: return spa.html
    deactivate server
    browser-->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    activate server
    server-->>browser: return main.css
    deactivate server
    browser-->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
    activate server
    server-->>browser: return spa.js
    deactivate server
    note right of browser: Browser runs JavaScript code including an instruction to fetch JSON data from server
    browser-->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate server
    server-->>browser: return data.json
    deactivate server
    note right of browser: Browser runs JavaScript code that renders data.json as a list
```

Exercise 5:

```mermaid
sequenceDiagram
    participant browser
    participant server

    browser-->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa
    activate server
    server-->>browser: return spa.html
    deactivate server
    browser-->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    activate server
    server-->>browser: return main.css
    deactivate server
    browser-->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
    activate server
    server-->>browser: return spa.js
    deactivate server
    note right of browser: Browser runs JavaScript code including an instruction to fetch JSON data from server
    browser-->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate server
    server-->>browser: return data.json
    deactivate server
    note right of browser: Browser runs JavaScript code that renders data.json as a list
```

Exercise 6:

```mermaid
sequenceDiagram
    participant browser
    participant server

    browser-->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    note right of browser: Browser sends data in body of POST request
    activate server
    server-->>browser: return code 201 with message 'note created'
    deactivate server
    note right of browser: Browser executes JavaScript code that appends the new note to the previously-fetched notes data, then re-renders the list
```
