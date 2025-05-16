# Folder Structure

- **/app**: Contains all the routes, components, and logic for your application, this is where you'll be mostly working from.

- **/app/lib**: Contains functions used in your application, such as reusable utility functions and data fetching functions.

- **/app/ui**: Contains all the UI components for your application, such as cards, tables, and forms. To save time, we've pre-styled these components for you.

- **/public**: Contains all the static assets for your application, such as images.

- **Config Files**: You'll also notice config files such as next.config.ts at the root of your application. Most of these files are created and pre-configured when you start a new project using create-next-app. You will not need to modify them in this course.

# Next.js files

- layout.tsx
- page.tsx
- loading.tsx
- route.ts (exports async functions like GET, POST, etc..)



## Chapter 9: Streaming

#### Steps:
1. Fetching data on server
2. Rendering HTML on server
  
    Rendering here stands for generating raw HTML strings.
    
    HTML server-side rendering is different from browser rendering that "paints" the viewport.

    These HTML strings are sent to the browser as-is and with streaming, this HTML can be sent in chunks, so parts of the page appear faster.

3. Loading code on the client

    After sending the HTML, the browser still needs to load CSS and JavaScript. 

    JS bundle can come afterwards — you can see the page before it's fully interactive.

4. Hydrating

    Hydration means "taking over" the static HTML from the server and making it interactive using JavaScript.

    It's like pouring water (JS logic) onto a dry sponge (static HTML) so it comes alive.


With streaming, we can send these process these steps through chunks in parallel. A chunk with the header, a chunk with section A, etc..