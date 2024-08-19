# SimpliStyle CSS Framework

## Package Contents

1. `src/simplistyle.css`: The main CSS file
2. `vite.config.js`: Vite configuration file
3. `package.json`: npm package configuration
4. `.npmignore`: Specifies files to exclude from the npm package

## Part 1: Main CSS File and Vite Configuration

### src/simplistyle.css

```css
/* SimpliStyle CSS Framework v1.0.0
 * https://github.com/yourusername/SimpliStyle
 * Licensed under MIT (https://github.com/yourusername/SimpliStyle/blob/main/LICENSE)
 */

/* Table of Contents:
 * 1. CSS Variables (Custom Properties)
 * 2. Base Styles
 * 3. Typography
 * 4. Layout
 * 5. Grid System
 * 6. Buttons
 * 7. Cards
 * 8. Navigation
 * 9. Forms
 * 10. Utility Classes
 * 11. Animations
 * 12. Advanced Features
 * 13. Dark Mode
 * 14. Responsive Design
 * 15. Accessibility
 */

/* 1. CSS Variables (Custom Properties) */
:root {
  /* Colors */
  --ss-primary-color: #0071e3;
  --ss-secondary-color: #5e5ce6;
  --ss-success-color: #34c759;
  --ss-warning-color: #ff9f0a;
  --ss-error-color: #ff3b30;
  --ss-background-color: #f2f2f7;
  --ss-text-color: #1c1c1e;
  --ss-light-text-color: #8e8e93;

  /* Typography */
  --ss-font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
  --ss-font-size-base: 16px;
  --ss-line-height-base: 1.5;

  /* Spacing */
  --ss-spacing-unit: 8px;

  /* Borders */
  --ss-border-radius: 8px;
  --ss-border-width: 1px;
  --ss-border-color: #c6c6c8;

  /* Shadows */
  --ss-shadow-sm: 0 1px 2px rgba(0, 0, 0, 0.05);
  --ss-shadow-md: 0 4px 6px rgba(0, 0, 0, 0.1);
  --ss-shadow-lg: 0 10px 15px rgba(0, 0, 0, 0.1);

  /* Transitions */
  --ss-transition-speed: 0.3s;
}

/* 2. Base Styles */
*, *::before, *::after {
  box-sizing: border-box;
}

html {
  font-size: var(--ss-font-size-base);
  line-height: var(--ss-line-height-base);
}

body {
  margin: 0;
  font-family: var(--ss-font-family);
  color: var(--ss-text-color);
  background-color: var(--ss-background-color);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

img {
  max-width: 100%;
  height: auto;
}

/* 3. Typography */
h1, h2, h3, h4, h5, h6 {
  margin-top: 0;
  margin-bottom: 0.5em;
  font-weight: 600;
  line-height: 1.2;
}

h1, .ss-h1 { font-size: 2.5rem; }
h2, .ss-h2 { font-size: 2rem; }
h3, .ss-h3 { font-size: 1.75rem; }
h4, .ss-h4 { font-size: 1.5rem; }
h5, .ss-h5 { font-size: 1.25rem; }
h6, .ss-h6 { font-size: 1rem; }

p {
  margin-top: 0;
  margin-bottom: 1rem;
}

.ss-text-small { font-size: 0.875em; }
.ss-text-large { font-size: 1.125em; }

/* 4. Layout */
.ss-container {
  width: 100%;
  padding-right: var(--ss-spacing-unit);
  padding-left: var(--ss-spacing-unit);
  margin-right: auto;
  margin-left: auto;
}

@media (min-width: 576px) {
  .ss-container {
    max-width: 540px;
  }
}

@media (min-width: 768px) {
  .ss-container {
    max-width: 720px;
  }
}

@media (min-width: 992px) {
  .ss-container {
    max-width: 960px;
  }
}

@media (min-width: 1200px) {
  .ss-container {
    max-width: 1140px;
  }
}

/* 5. Grid System */
.ss-row {
  display: flex;
  flex-wrap: wrap;
  margin-right: calc(var(--ss-spacing-unit) * -1);
  margin-left: calc(var(--ss-spacing-unit) * -1);
}

.ss-col {
  flex-basis: 0;
  flex-grow: 1;
  max-width: 100%;
  padding-right: var(--ss-spacing-unit);
  padding-left: var(--ss-spacing-unit);
}

.ss-col-auto {
  flex: 0 0 auto;
  width: auto;
  max-width: 100%;
}

.ss-col-1 { flex: 0 0 8.333333%; max-width: 8.333333%; }
.ss-col-2 { flex: 0 0 16.666667%; max-width: 16.666667%; }
.ss-col-3 { flex: 0 0 25%; max-width: 25%; }
.ss-col-4 { flex: 0 0 33.333333%; max-width: 33.333333%; }
.ss-col-5 { flex: 0 0 41.666667%; max-width: 41.666667%; }
.ss-col-6 { flex: 0 0 50%; max-width: 50%; }
.ss-col-7 { flex: 0 0 58.333333%; max-width: 58.333333%; }
.ss-col-8 { flex: 0 0 66.666667%; max-width: 66.666667%; }
.ss-col-9 { flex: 0 0 75%; max-width: 75%; }
.ss-col-10 { flex: 0 0 83.333333%; max-width: 83.333333%; }
.ss-col-11 { flex: 0 0 91.666667%; max-width: 91.666667%; }
.ss-col-12 { flex: 0 0 100%; max-width: 100%; }

/* Responsive grid classes */
@media (min-width: 576px) {
  .ss-col-sm-1 { flex: 0 0 8.333333%; max-width: 8.333333%; }
  .ss-col-sm-2 { flex: 0 0 16.666667%; max-width: 16.666667%; }
  .ss-col-sm-3 { flex: 0 0 25%; max-width: 25%; }
  .ss-col-sm-4 { flex: 0 0 33.333333%; max-width: 33.333333%; }
  .ss-col-sm-5 { flex: 0 0 41.666667%; max-width: 41.666667%; }
  .ss-col-sm-6 { flex: 0 0 50%; max-width: 50%; }
  .ss-col-sm-7 { flex: 0 0 58.333333%; max-width: 58.333333%; }
  .ss-col-sm-8 { flex: 0 0 66.666667%; max-width: 66.666667%; }
  .ss-col-sm-9 { flex: 0 0 75%; max-width: 75%; }
  .ss-col-sm-10 { flex: 0 0 83.333333%; max-width: 83.333333%; }
  .ss-col-sm-11 { flex: 0 0 91.666667%; max-width: 91.666667%; }
  .ss-col-sm-12 { flex: 0 0 100%; max-width: 100%; }
}

@media (min-width: 768px) {
  .ss-col-md-1 { flex: 0 0 8.333333%; max-width: 8.333333%; }
  .ss-col-md-2 { flex: 0 0 16.666667%; max-width: 16.666667%; }
  .ss-col-md-3 { flex: 0 0 25%; max-width: 25%; }
  .ss-col-md-4 { flex: 0 0 33.333333%; max-width: 33.333333%; }
  .ss-col-md-5 { flex: 0 0 41.666667%; max-width: 41.666667%; }
  .ss-col-md-6 { flex: 0 0 50%; max-width: 50%; }
  .ss-col-md-7 { flex: 0 0 58.333333%; max-width: 58.333333%; }
  .ss-col-md-8 { flex: 0 0 66.666667%; max-width: 66.666667%; }
  .ss-col-md-9 { flex: 0 0 75%; max-width: 75%; }
  .ss-col-md-10 { flex: 0 0 83.333333%; max-width: 83.333333%; }
  .ss-col-md-11 { flex: 0 0 91.666667%; max-width: 91.666667%; }
  .ss-col-md-12 { flex: 0 0 100%; max-width: 100%; }
}

@media (min-width: 992px) {
  .ss-col-lg-1 { flex: 0 0 8.333333%; max-width: 8.333333%; }
  .ss-col-lg-2 { flex: 0 0 16.666667%; max-width: 16.666667%; }
  .ss-col-lg-3 { flex: 0 0 25%; max-width: 25%; }
  .ss-col-lg-4 { flex: 0 0 33.333333%; max-width: 33.333333%; }
  .ss-col-lg-5 { flex: 0 0 41.666667%; max-width: 41.666667%; }
  .ss-col-lg-6 { flex: 0 0 50%; max-width: 50%; }
  .ss-col-lg-7 { flex: 0 0 58.333333%; max-width: 58.333333%; }
  .ss-col-lg-8 { flex: 0 0 66.666667%; max-width: 66.666667%; }
  .ss-col-lg-9 { flex: 0 0 75%; max-width: 75%; }
  .ss-col-lg-10 { flex: 0 0 83.333333%; max-width: 83.333333%; }
  .ss-col-lg-11 { flex: 0 0 91.666667%; max-width: 91.666667%; }
  .ss-col-lg-12 { flex: 0 0 100%; max-width: 100%; }
}

@media (min-width: 1200px) {
  .ss-col-xl-1 { flex: 0 0 8.333333%; max-width: 8.333333%; }
  .ss-col-xl-2 { flex: 0 0 16.666667%; max-width: 16.666667%; }
  .ss-col-xl-3 { flex: 0 0 25%; max-width: 25%; }
  .ss-col-xl-4 { flex: 0 0 33.333333%; max-width: 33.333333%; }
  .ss-col-xl-5 { flex: 0 0 41.666667%; max-width: 41.666667%; }
  .ss-col-xl-6 { flex: 0 0 50%; max-width: 50%; }
  .ss-col-xl-7 { flex: 0 0 58.333333%; max-width: 58.333333%; }
  .ss-col-xl-8 { flex: 0 0 66.666667%; max-width: 66.666667%; }
  .ss-col-xl-9 { flex: 0 0 75%; max-width: 75%; }
  .ss-col-xl-10 { flex: 0 0 83.333333%; max-width: 83.333333%; }
  .ss-col-xl-11 { flex: 0 0 91.666667%; max-width: 91.666667%; }
  .ss-col-xl-12 { flex: 0 0 100%; max-width: 100%; }
}

/* 6. Buttons */
.ss-button {
  display: inline-block;
  font-weight: 400;
  text-align: center;
  vertical-align: middle;
  user-select: none;
  border: var(--ss-border-width) solid transparent;
  padding: 0.375rem 0.75rem;
  font-size: 1rem;
  line-height: 1.5;
  border-radius: var(--ss-border-radius);
  transition: color var(--ss-transition-speed), background-color var(--ss-transition-speed), border-color var(--ss-transition-speed), box-shadow var(--ss-transition-speed);
  cursor: pointer;
}

.ss-button:hover {
  text-decoration: none;
}

.ss-button:focus {
  outline: 0;
  box-shadow: 0 0 0 0.2rem rgba(0, 123, 255, 0.25);
}

.ss-button--primary {
  color: #fff;
  background-color: var(--ss-primary-color);
  border-color: var(--ss-primary-color);
}

.ss-button--primary:hover {
  background-color: #0056b3;
  border-color: #004da6;
}

.ss-button--secondary {
  color: #fff;
  background-color: var(--ss-secondary-color);
  border-color: var(--ss-secondary-color);
}

.ss-button--secondary:hover {
  background-color: #4a47c9;
  border-color: #

/* 7. Cards */
.ss-card {
  position: relative;
  display: flex;
  flex-direction: column;
  min-width: 0;
  word-wrap: break-word;
  background-color: #fff;
  background-clip: border-box;
  border: var(--ss-border-width) solid var(--ss-border-color);
  border-radius: var(--ss-border-radius);
}

.ss-card__body {
  flex: 1 1 auto;
  min-height: 1px;
  padding: 1.25rem;
}

.ss-card__title {
  margin-bottom: 0.75rem;
}

.ss-card__text:last-child {
  margin-bottom: 0;
}

/* 8. Navigation */
.ss-nav {
  display: flex;
  flex-wrap: wrap;
  padding-left: 0;
  margin-bottom: 0;
  list-style: none;
}

.ss-nav__link {
  display: block;
  padding: 0.5rem 1rem;
  text-decoration: none;
  color: var(--ss-text-color);
  transition: color var(--ss-transition-speed);
}

.ss-nav__link:hover,
.ss-nav__link:focus {
  color: var(--ss-primary-color);
}

/* 9. Forms */
.ss-form-group {
  margin-bottom: 1rem;
}

.ss-form-label {
  display: inline-block;
  margin-bottom: 0.5rem;
}

.ss-form-control {
  display: block;
  width: 100%;
  padding: 0.375rem 0.75rem;
  font-size: 1rem;
  line-height: 1.5;
  color: var(--ss-text-color);
  background-color: #fff;
  background-clip: padding-box;
  border: var(--ss-border-width) solid var(--ss-border-color);
  border-radius: var(--ss-border-radius);
  transition: border-color var(--ss-transition-speed), box-shadow var(--ss-transition-speed);
}

.ss-form-control:focus {
  color: var(--ss-text-color);
  background-color: #fff;
  border-color: var(--ss-primary-color);
  outline: 0;
  box-shadow: 0 0 0 0.2rem rgba(0, 123, 255, 0.25);
}

/* 10. Utility Classes */
.ss-text-center { text-align: center; }
.ss-text-left { text-align: left; }
.ss-text-right { text-align: right; }

.ss-mt-1 { margin-top: calc(var(--ss-spacing-unit) * 1); }
.ss-mt-2 { margin-top: calc(var(--ss-spacing-unit) * 2); }
.ss-mt-3 { margin-top: calc(var(--ss-spacing-unit) * 3); }

.ss-mb-1 { margin-bottom: calc(var(--ss-spacing-unit) * 1); }
.ss-mb-2 { margin-bottom: calc(var(--ss-spacing-unit) * 2); }
.ss-mb-3 { margin-bottom: calc(var(--ss-spacing-unit) * 3); }

.ss-ml-1 { margin-left: calc(var(--ss-spacing-unit) * 1); }
.ss-ml-2 { margin-left: calc(var(--ss-spacing-unit) * 2); }
.ss-ml-3 { margin-left: calc(var(--ss-spacing-unit) * 3); }

.ss-mr-1 { margin-right: calc(var(--ss-spacing-unit) * 1); }
.ss-mr-2 { margin-right: calc(var(--ss-spacing-unit) * 2); }
.ss-mr-3 { margin-right: calc(var(--ss-spacing-unit) * 3); }

.ss-p-1 { padding: calc(var(--ss-spacing-unit) * 1); }
.ss-p-2 { padding: calc(var(--ss-spacing-unit) * 2); }
.ss-p-3 { padding: calc(var(--ss-spacing-unit) * 3); }

.ss-d-none { display: none; }
.ss-d-block { display: block; }
.ss-d-flex { display: flex; }

.ss-justify-content-start { justify-content: flex-start; }
.ss-justify-content-center { justify-content: center; }
.ss-justify-content-end { justify-content: flex-end; }
.ss-justify-content-between { justify-content: space-between; }

.ss-align-items-start { align-items: flex-start; }
.ss-align-items-center { align-items: center; }
.ss-align-items-end { align-items: flex-end; }

/* 11. Animations */
@keyframes ss-fade-in {
  from { opacity: 0; }
  to { opacity: 1; }
}

.ss-fade-in {
  animation: ss-fade-in var(--ss-transition-speed) ease-in;
}

.ss-scale-on-hover {
  transition: transform var(--ss-transition-speed);
}

.ss-scale-on-hover:hover {
  transform: scale(1.05);
}

/* 12. Advanced Features */
.ss-glass-morphism {
  background: rgba(255, 255, 255, 0.2);
  backdrop-filter: blur(10px);
  border-radius: var(--ss-border-radius);
  border: 1px solid rgba(255, 255, 255, 0.1);
}

.ss-gradient-text {
  background: linear-gradient(45deg, var(--ss-primary-color), var(--ss-secondary-color));
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
}

/* 13. Dark Mode */
@media (prefers-color-scheme: dark) {
  :root {
    --ss-background-color: #000000;
    --ss-text-color: #ffffff;
    --ss-light-text-color: #8e8e93;
    --ss-border-color: #38383a;
  }

  .ss-card {
    background-color: #1c1c1e;
  }

  .ss-form-control {
    background-color: #1c1c1e;
    color: #ffffff;
  }
}

/* 14. Responsive Design */
@media (max-width: 576px) {
  .ss-hidden-sm { display: none; }
}

@media (min-width: 577px) and (max-width: 768px) {
  .ss-hidden-md { display: none; }
}

@media (min-width: 769px) and (max-width: 992px) {
  .ss-hidden-lg { display: none; }
}

@media (min-width: 993px) {
  .ss-hidden-xl { display: none; }
}

/* 15. Accessibility */
.ss-visually-hidden {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border: 0;
}

.ss-focus-visible:focus:not(:focus-visible) {
  outline: none;
  box-shadow: none;
}

.ss-focus-visible:focus-visible {
  outline: 2px solid var(--ss-primary-color);
  outline-offset: 2px;
}

@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
}
```

### vite.config.js

```javascript
import { defineConfig } from 'vite'
import { resolve } from 'path'

export default defineConfig({
  build: {
    lib: {
      entry: resolve(__dirname, 'src/simplistyle.css'),
      name: 'SimpliStyle',
      fileName: (format) => `simplistyle.${format}.css`
    },
    rollupOptions: {
      output: {
        assetFileNames: (assetInfo) => {
          if (assetInfo.name === 'style.css') return 'simplistyle.css'
          return assetInfo.name
        }
      }
    },
    minify: true,
    sourcemap: true
  }
})
```

### package.json

```json
{
  "name": "simplistyle",
  "version": "1.0.0",
  "description": "A minimalist CSS framework inspired by Apple's design principles",
  "main": "dist/simplistyle.umd.css",
  "module": "dist/simplistyle.es.css",
  "style": "dist/simplistyle.css",
  "files": [
    "dist"
  ],
  "scripts": {
    "build": "vite build",
    "prepublishOnly": "npm run build"
  },
  "keywords": [
    "css",
    "framework",
    "minimalist",
    "apple-inspired"
  ],
  "author": "Your Name",
  "license": "MIT",
  "devDependencies": {
    "vite": "^2.9.9"
  }
}
```

### .npmignore

```
src/
vite.config.js
.gitignore
```

## Setup Instructions

1. Create a new directory for your project and navigate into it:
   ```
   mkdir simplistyle && cd simplistyle
   ```

2. Initialize a new npm package:
   ```
   npm init -y
   ```

3. Install Vite as a dev dependency:
   ```
   npm install --save-dev vite
   ```

4. Create the following file structure:
   ```
   simplistyle/
   ├── src/
   │   └── simplistyle.css
   ├── vite.config.js
   ├── package.json
   └── .npmignore
   ```

5. Copy the contents of `simplistyle.css`, `vite.config.js`, `package.json`, and `.npmignore` into their respective files.

6. Build the project:
   ```
   npm run build
   ```

7. Publish to npm:
   ```
   npm publish
   ```

## Using with jsDelivr

After publishing to npm, you can use jsDelivr as a CDN. Add the following link to your HTML file:

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/simplistyle@1.0.0/dist/simplistyle.css">
```

Replace `1.0.0` with the version you want to use, or use `latest` for the most recent version.

## Local Development

1. Install dependencies:
   ```
   npm install
   ```

2. Make changes to `src/simplistyle.css`

3. Build the project:
   ```
   npm run build
   ```

4. The built files will be in the `dist/` directory.

Remember to update the version in `package.json` before publishing a new version to npm.
