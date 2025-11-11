# frontend-only

This repo contains a frontend-only React app that uses the
same conventions as the other ucsb-cs156 code bases.

This repo will deploy itself on Github Pages.

You will need to configure Github Pages to use the gh-pages branch 
for the site.

You will also need to do a global search/replace on 

* `frontend-only` to `name-of-repo` 

Specifically:

1.  In vite.config.js, you need this inside the `export default defineConfig({` object:

    ```
    base: `/name-of-repo`
    ```

2.  In `main.jsx`, you need this on the `<BrowserRouter>` open tag:

    ```
        <BrowserRouter basename="/name-of-repo">
    ```