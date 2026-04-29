# WIP Area

This folder is a **completely separate Quarto project** that serves as one's
personal development sandbox. It is invisible to the main site's render process.

## How it works

- Running `quarto render` from the main project root will never touch this folder
- Running `quarto render` or `quarto preview` from inside `wip/` renders
  only your WIP projects
- Output goes to `wip/_site/`, completely separate from the main `_site/`

## Adding a new WIP project

1. Create a new subfolder: `wip/project-x/`
2. Add a `index.qmd` inside it
3. Add it to `wip/_quarto.yml` navbar
4. Run `quarto render` from inside `wip/`

## Promoting a project to the main site

When a project is ready:

1. Move the entire folder (e.g. `wip/my-new-project/`) to the root of the
   main project
2. Add a link to it in the main `_quarto.yml` navbar
3. Run `quarto render` from the main project root
