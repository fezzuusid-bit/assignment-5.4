HTML
<!-- index.html -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Design Tokens & CSS Variables Showcase</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header class="site-header">
        <h1>Design System Showcase</h1>
        <p>Built using reusable CSS variables and design tokens.</p>
    </header>

    <main class="container">
        <section class="card">
            <h2>Primary Card Title</h2>
            <p>This card utilizes design tokens for background colors, text colors, spacing, and border radius.</p>
            <button class="btn btn-primary">Primary Action</button>
        </section>

        <section class="card">
            <h2>Secondary Card Title</h2>
            <p>Changing a single CSS variable in `:root` instantly updates the entire theme across all components.</p>
            <button class="btn btn-secondary">Secondary Action</button>
        </section>
    </main>

    <footer>
        <p>&copy; 2026 Atim Akhtar. All rights reserved.</p>
    </footer>
</body>
</html>
CSS
/* style.css */

/* 1. Define Design Tokens in :root */
:root {
    /* Color Palette */
    --color-primary: #3b82f6;
    --color-primary-hover: #2563eb;
    --color-secondary: #0f172a;
    --color-bg: #f8fafc;
    --color-surface: #ffffff;
    --color-text: #334155;
    --color-text-muted: #64748b;
    --color-border: #e2e8f0;

    /* Spacing Tokens */
    --space-sm: 8px;
    --space-md: 16px;
    --space-lg: 24px;
    --space-xl: 32px;

    /* Font Size Tokens */
    --font-size-sm: 0.875rem;
    --font-size-base: 1rem;
    --font-size-lg: 1.25rem;
    --font-size-xl: 1.75rem;

    /* Border Radius & Shadow Tokens */
    --radius-md: 8px;
    --shadow-sm: 0 2px 4px rgba(0, 0, 0, 0.05);
    --shadow-md: 0 4px 6px rgba(0, 0, 0, 0.08);
}

/* Base Styles Using Tokens */
body {
    font-family: Arial, sans-serif;
    background-color: var(--color-bg);
    color: var(--color-text);
    font-size: var(--font-size-base);
    line-height: 1.6;
    margin: 0;
    padding: 0;
}

.site-header {
    background-color: var(--color-secondary);
    color: var(--color-surface);
    padding: var(--space-xl) var(--space-md);
    text-align: center;
}

.site-header h1 {
    font-size: var(--font-size-xl);
    margin-bottom: var(--space-sm);
    color: var(--color-surface);
}

.site-header p {
    color: var(--color-text-muted);
    font-size: var(--font-size-lg);
    margin: 0;
}

.container {
    max-width: 800px;
    margin: var(--space-xl) auto;
    padding: 0 var(--space-md);
    display: flex;
    flex-direction: column;
    gap: var(--space-lg);
}

/* Component Styles Using Tokens */
.card {
    background-color: var(--color-surface);
    border: 1px solid var(--color-border);
    border-radius: var(--radius-md);
    padding: var(--space-lg);
    box-shadow: var(--shadow-sm);
    transition: box-shadow 0.3s ease;
}

.card:hover {
    box-shadow: var(--shadow-md);
}

.card h2 {
    color: var(--color-secondary);
    font-size: var(--font-size-lg);
    margin-top: 0;
    margin-bottom: var(--space-sm);
}

.card p {
    color: var(--color-text);
    margin-bottom: var(--space-md);
}

/* Buttons Using Tokens */
.btn {
    font-size: var(--font-size-base);
    font-weight: bold;
    padding: var(--space-sm) var(--space-md);
    border: none;
    border-radius: var(--radius-md);
    cursor: pointer;
    transition: background-color 0.2s ease;
}

.btn-primary {
    background-color: var(--color-primary);
    color: var(--color-surface);
}

.btn-primary:hover {
    background-color: var(--color-primary-hover);
}

.btn-secondary {
    background-color: var(--color-secondary);
    color: var(--color-surface);
}

.btn-secondary:hover {
    background-color: #1e293b;
}

footer {
    text-align: center;
    padding: var(--space-lg);
    color: var(--color-text-muted);
    font-size: var(--font-size-sm);
    border-top: 1px solid var(--color-border);
    margin-top: var(--space-xl);
}
Ready for Assignment 5.5? Let me know whenever you want me to send it over!

Yes