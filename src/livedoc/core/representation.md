Live documents are represented as JSON.  
The JSON is created in the frontend and sent to the backend via WebSockets.  

The backend evaluates the JSON and produces a new JSON which is the updated state of the document.  

This new JSON is sent back to the frontend to be displayed.  

### Questions

- Should the whole JSON be sent back and forth between each end ?
- If not, should the global state be stored on the back or the front end ?
  - For this one, I think it should be stored on the back. Here I'm thinking about collaborative editing.

### Tools

-  Edition : Two editors 
    - monaco for code
    - a promise mirror based editor like TipTap for example (with promise-mirror-math or custom pro tiptap math extension) for text/math/markdown. 
   I can embed monaco into a TipTap custom node for code.

- Collaboration :  
Yjs integrates well with both monaco and promise-mirror.
