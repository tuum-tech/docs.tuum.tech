## How to build locally

1. **Pull the docker image for 'slate'**
   ```
   docker pull slatedocs/slate
   ```
2. **Build the site**
   ```
   docker container rm -f slate;
   docker run --rm --name slate -v $(pwd)/build:/srv/slate/build -v $(pwd)/source:/srv/slate/source slatedocs/slate
   ```
3. **Run the development server for Slate to aid in working on the site**
   ```
   docker run --rm --name slate -p 4567:4567 -v $(pwd)/source:/srv/slate/source slatedocs/slate serve
   ```

## Guides

- [Learn how the Markdown Syntax works](https://github.com/slatedocs/slate/wiki/Markdown-Syntax)
- [Learn how to deploy the site](https://github.com/slatedocs/slate/wiki/Deploying-Slate)
- [General Wiki on how Slate works](https://github.com/slatedocs/slate/wiki#getting-started)
