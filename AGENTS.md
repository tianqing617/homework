# Repository Guidelines

## Project Structure & Module Organization
This repository is currently minimal and centered on a single top-level document: [`math300.html`](/Users/tianqing/home/homework/math300.html). There is no `src/`, `tests/`, or asset pipeline yet. Keep new files at the repository root only when they are project entry points or primary deliverables. If the project expands, group code under `src/`, place reusable static assets under `assets/`, and mirror tests under `tests/`.

## Build, Test, and Development Commands
There is no formal build system configured today. Use lightweight local checks before committing:

- `open math300.html` to preview the page in a browser on macOS.
- `python3 -m http.server 8000` to serve the repository locally for manual testing.
- `git diff --check` to catch trailing whitespace and malformed patches.

If you add tooling later, document the exact commands here and keep them reproducible from a clean clone.

## Coding Style & Naming Conventions
Use 2 spaces for HTML, CSS, and JavaScript indentation inside this repository. Prefer semantic HTML and descriptive file names in lowercase with hyphens, for example `course-outline.html` or `site-styles.css`. Keep inline scripts and styles small; move repeated logic into separate files once the project has more than one page. Favor clear IDs and classes such as `assignment-list` over presentation-based names.

## Testing Guidelines
Testing is manual at the moment. Before opening a pull request, verify the page loads cleanly in a browser, links work, and layout remains readable on both desktop and mobile widths. If JavaScript is introduced, add a `tests/` directory and adopt a browser-facing test runner before shipping complex behavior.

## Commit & Pull Request Guidelines
Git history currently starts with a single `init` commit, so no detailed convention is established yet. Use short, imperative commit messages such as `Add syllabus table styling` or `Fix broken homework link`. Pull requests should include a concise description, a summary of visible changes, and screenshots for UI-affecting edits. Link any related issue or task when applicable.

## Security & Configuration Tips
Do not commit secrets, API keys, or personal data into HTML, JavaScript, or sample content. Keep third-party assets licensed and documented if they are added later.
