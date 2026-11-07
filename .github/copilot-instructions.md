# Copilot instructions

## Architecture

- This is a dependency-free, single-page static site. `index.html` contains the page structure, Portuguese copy, and inline vanilla JavaScript; `styles.css` contains the design system, layout, responsive rules, and animations.
- Section IDs in `index.html` are targets for the navigation and calls to action. Keep those links in sync when changing section IDs.
- The contact form currently prevents submission, displays a client-side confirmation, and resets. It does not send data to a backend; do not describe it as a working lead-delivery integration.

## Build, test, and lint

- No package manifest, build scripts, test suite, or lint configuration is present. There are no project build, test, lint, or single-test commands to run.
- For a manual visual check, open `index.html` in a browser.

## Conventions

- Keep user-facing copy in Brazilian Portuguese (`lang="pt-BR"`).
- Add or adjust shared colors and font stacks in the `:root` custom properties in `styles.css`. The current typography uses Manrope for display and Inter for body text, with system fallbacks.
- Preserve the lightweight HTML/CSS/vanilla-JavaScript approach; do not add a framework, build system, or animation dependency for routine page changes.
- Keep responsive behavior and reduced-motion support in `styles.css`. JavaScript reveals and count-up effects use `IntersectionObserver` and check `prefers-reduced-motion`; preserve a usable static presentation when motion is reduced.
- The form controls use accessible names and the confirmation uses `role="status"`. Follow these patterns when changing the form.
- For relevant UI work, the repository skills in `.agents/skills/web-design-reviewer/SKILL.md` and `.agents/skills/premium-frontend-ui/SKILL.md` provide additional guidance; apply them in a way that preserves this site's existing lightweight architecture.
