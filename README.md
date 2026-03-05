# Personal Site (Static, ERB-Rendered)

A hand-built personal website powered by a lightweight Ruby rendering pipeline.

Templates are written in ERB, composed using partials, and compiled into static HTML via a custom build script. Source templates are kept separate from generated output, enabling reusable layout components and a simple, maintainable workflow.

This project serves as:
- A home for my “Today I Learned” technical notes
- An experimentation space for templating and workflow design
- A deliberately framework-free exercise in structure and maintainability

## Live Site

Deployed to both Aavalam and GitHub Pages:

- https://www.aavalam.org/~kellyky/
- https://kellyky.github.io/website/

## Local Setup

```sh
git clone git@github.com:kellyky/erb-static-website.git
cd erb-static-website
chmod +x bin/render
```

To view locally, open `index.html` directly in your browser:

```sh
open index.html
```

Alternatively, open the file using its absolute path — either with open from the command line or by pasting the path into your browser’s address bar:

```sh
file:///Users/me/path/to/erb-static-website/index.html
```

## Development Workflow

HTML files are generated artifacts and should not be edited directly.

To make changes:

1. Update the appropriate .erb template or asset file.
2. Run the render script from the project root.

```sh
bin/render
```

This regenerates the corresponding HTML file(s).

## Project Structure

```plaintext
├── README.md
├── assets/
│   ├── css/
│   └── images/
├── bin/
│   └── render                  # Static rendering script
├── index.html                  # Generated output
└── views/
    ├── index.erb               # Page structure template
    └── partials/               # Reusable ERB partials (header, footer)
        ├── _footer.erb
        ├── _header.erb
        └── _main.erb
```

