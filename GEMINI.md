# Gemini Assistant Guidelines for `hirom.net`

This document provides guidelines for the Gemini assistant to ensure its contributions are aligned with the project's standards and conventions.

## 1. Project Overview

-   **Project Name:** `hirom.net` (based on `astro-chiri` theme)
-   **Description:** A personal blog built with the Astro framework.
-   **Package Manager:** pnpm

## 2. Core Technologies

-   **Framework:** Astro (`^5.12.0`)
-   **Language:** TypeScript (`^5.8.3`)
-   **UI Components:** Astro components (`.astro`)
-   **Content:** Markdown (`.md`) and MDX (`.mdx`)
-   **Deployment:** Netlify

## 3. Key Commands

When asked to perform common tasks, use the following `pnpm` scripts:

| Task | Command | Description |
| :--- | :--- | :--- |
| **Start Dev Server** | `pnpm dev` | Runs the local development server. |
| **Create Production Build** | `pnpm build` | Builds the static site for production. |
| **Preview Build** | `pnpm preview` | Previews the production build locally. |
| **Lint Files** | `pnpm lint` | Lints the codebase with ESLint. |
| **Fix Lint Errors** | `pnpm lint:fix` | Automatically fixes fixable ESLint errors. |
| **Format Code** | `pnpm format` | Formats code with Prettier. |
| **Check Formatting** | `pnpm format:check` | Checks for formatting issues without writing files. |
| **Create New Post** | `pnpm new` | Runs the interactive script to create a new blog post. |

**Note:** Always use `pnpm` to run these scripts.

## 4. Content Management

-   **Location:** All blog posts are located in `src/content/posts/`.
-   **Creating Posts:** To create a new post, always use the `pnpm new` command. Do not create files manually.
-   **File Format:** Posts should be in Markdown (`.md`).
-   **Frontmatter:** Ensure all posts have the following frontmatter fields:
    -   `title`: The title of the post.
    -   `pubDate`: The publication date in `YYYY-MM-DD` format.
    -   `description`: A brief summary of the post.
    -   `tags`: An array of relevant tags (e.g., `["Astro", "TypeScript"]`). **Note: Any article generated or appended by Gemini CLI must include the `Gemini_CLI` tag.**
-   **File Generation Location:** All generated or modified content files must be located exclusively within `src/content/posts/`.
-   **File Naming Convention:** Generated or modified post files must adhere to the `YYYY-MM-DD_記事名.md` format.

## 5. Code Style and Conventions

-   **Formatting:** All code must be formatted with Prettier. Before committing, always run `pnpm format`.
-   **Linting:** All code must pass ESLint checks. Run `pnpm lint` to check for issues.
-   **Component Structure:**
    -   UI-specific, reusable components go into `src/components/ui/`.
    -   Layout components go into `src/components/layout/`.
    -   Page-specific or single-use components can be co-located with the pages that use them.
-   **Styling:** Global styles are managed in `src/styles/global.css`. Component-specific styles should be scoped within the Astro component's `<style>` tag.

## 6. Dependencies

-   Use `pnpm add` to add new dependencies.
-   Use `pnpm add -D` to add new development dependencies.
-   Before adding a new dependency, consider if the desired functionality can be achieved with existing libraries.

## 7. Deployment

-   The site is hosted on Netlify.
-   Deployment is handled automatically by Netlify upon pushing to the `main` branch.
-   The build command executed by Netlify is `pnpm build`.

By following these guidelines, you can effectively assist with development, content creation, and maintenance tasks for this project.
