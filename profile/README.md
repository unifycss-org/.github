<div align="center">

# @unifycss/unifycss

**The complete, zero-runtime CSS framework for modern web applications.**

Build anything — from UI components to full application layouts — using **semantic class names**, **standalone button variants**, and a rich **1,989-class utility system** with comprehensive design tokens.

[![npm version](https://img.shields.io/npm/v/@unifycss/unifycss.svg?style=flat-square)](https://npmjs.com/package/@unifycss/unifycss)
[![npm downloads](https://img.shields.io/npm/dw/@unifycss/unifycss.svg?style=flat-square)](https://npmjs.com/package/@unifycss/unifycss)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://opensource.org/licenses/MIT)

</div>

---

## Table of Contents

- [Installation](#installation)
- [Quick Start](#quick-start)
- [Design Tokens](#design-tokens)
- [Button System](#button-system)
- [Component Library](#component-library)
  - [Layout & Application Shell](#layout--application-shell)
  - [Typography System](#typography-system)
  - [Badges & Tags](#badges--tags)
  - [Cards](#cards)
  - [Forms](#forms)
  - [Alerts & Feedback](#alerts--feedback)
  - [Navigation](#navigation)
  - [Modals & Overlays](#modals--overlays)
  - [Data Tables](#data-tables)
  - [Loading & Skeleton](#loading--skeleton)
  - [Tabs & Pills](#tabs--pills)
  - [Glassmorphism Effects](#glassmorphism-effects)
  - [Kanban & Dashboard](#kanban--dashboard)
  - [Media & Camera Views](#media--camera-views)
  - [AI & Chat Interfaces](#ai--chat-interfaces)
- [Utility Reference](#utility-reference)
  - [Spacing & Sizing](#spacing--sizing)
  - [Colors & Backgrounds](#colors--backgrounds)
  - [Borders & Radius](#borders--radius)
  - [Flexbox & Grid](#flexbox--grid)
  - [Transitions & Animations](#transitions--animations)
  - [Dark Mode](#dark-mode)
  - [Responsive Breakpoints](#responsive-breakpoints)
  - [Hover, Focus & State Variants](#hover-focus--state-variants)
  - [Accessibility Utilities](#accessibility-utilities)
  - [Print Utilities](#print-utilities)
- [Customization](#customization)
- [Framework Integrations](#framework-integrations)
- [License](#license)

---

## Installation

```bash
npm install @unifycss/unifycss
# or
pnpm add @unifycss/unifycss
# or
yarn add @unifycss/unifycss
```

---

## Quick Start

### Import in JavaScript / TypeScript / React / Next.js

```js
// In your entry file (e.g. app/layout.tsx, main.ts, App.js)
import '@unifycss/unifycss/unifycss.css';
```

### HTML Link Tag

```html
<link rel="stylesheet" href="node_modules/@unifycss/unifycss/unifycss.css" />
```

### CDN

```html
<!-- From unpkg -->
<link rel="stylesheet" href="https://unpkg.com/@unifycss/unifycss/unifycss.css" />
```

---

## Design Tokens

UnifyCSS is built on a comprehensive design token system powered by CSS custom properties. Override any token globally:

```css
:root {
  /* Brand Colors */
  --brand-primary:        #3b82f6;
  --brand-primary-light:  #60a5fa;
  --brand-primary-dark:   #2563eb;

  /* Gold System (signature UnifyCSS accent) */
  --gold:                 #e8c9a0;
  --gold-dark:            #c9a97d;
  --gold-light:           #f4dfc0;
  --gold-text:            #0a0a0a;

  /* Semantic Colors */
  --success:              #10b981;
  --warning:              #f59e0b;
  --danger:               #ef4444;
  --info:                 #3b82f6;

  /* Dark Surface System */
  --dark-base:            #07070a;
  --dark-100:             #0f0f14;
  --dark-200:             #16161d;
  --dark-300:             #1d1d27;
  --dark-400:             #252533;

  /* Typography */
  --font-sans:            'Inter', system-ui, -apple-system, sans-serif;
  --font-mono:            'Fira Code', 'Cascadia Code', monospace;
  --font-serif:           'Playfair Display', Georgia, serif;

  /* Border Radius */
  --radius-sm:            0.25rem;
  --radius-md:            0.5rem;
  --radius-lg:            0.75rem;
  --radius-xl:            1rem;
  --radius-2xl:           1.5rem;
  --radius-full:          9999px;

  /* Shadows */
  --shadow-sm:            0 1px 3px rgba(0,0,0,0.12);
  --shadow-md:            0 4px 16px rgba(0,0,0,0.25);
  --shadow-lg:            0 8px 32px rgba(0,0,0,0.35);
  --shadow-gold:          0 0 24px rgba(232,201,160,0.3);
}
```

---

## Button System

UnifyCSS features a **standalone button system** — every variant class carries its own base structural properties (padding, border-radius, display, font, cursor) and works without needing an additional `.btn` base class.

### Gold Button Family (signature dark-surface system)

```html
<!-- Filled -->
<button class="btn-gold">Get Started</button>

<!-- Outline -->
<button class="btn-gold-outline">View Details</button>

<!-- Ghost -->
<button class="btn-gold-ghost">Cancel</button>

<!-- Sizes -->
<button class="btn-gold btn-gold-sm">Small</button>
<button class="btn-gold btn-gold-lg">Large</button>
```

### Semantic Color Buttons

```html
<button class="btn-primary">Primary Action</button>
<button class="btn-secondary">Secondary</button>
<button class="btn-success">Save</button>
<button class="btn-warning">Caution</button>
<button class="btn-danger">Delete</button>
<button class="btn-info">Learn More</button>
<button class="btn-neutral">Default</button>
```

### Premium Accent Buttons

```html
<button class="btn-emerald">Confirm</button>
<button class="btn-rose">Remove</button>
<button class="btn-sapphire">Connect</button>
```

### Outline Variants

```html
<button class="btn-outline">Default Outline</button>
<button class="btn-outline-primary">Primary Outline</button>
<button class="btn-outline-secondary">Secondary Outline</button>
<button class="btn-outline-success">Success Outline</button>
<button class="btn-outline-warning">Warning Outline</button>
<button class="btn-outline-danger">Danger Outline</button>
<button class="btn-outline-info">Info Outline</button>
<button class="btn-emerald-outline">Emerald Outline</button>
```

### Ghost Variants

```html
<button class="btn-ghost">Ghost</button>
<button class="btn-ghost-danger">Danger Ghost</button>
<button class="btn-ghost-success">Success Ghost</button>
```

### Composed Usage (optional base class)

```html
<!-- With explicit base class if preferred -->
<button class="btn btn-primary">Primary</button>
<button class="btn btn-sm btn-outline-danger">Small Danger Outline</button>
```

---

## Component Library

### Layout & Application Shell

```html
<!-- Full application shell -->
<div class="app-shell">
  <header class="app-bar">
    <nav class="top-nav">...</nav>
  </header>
  <aside class="side-nav">...</aside>
  <main class="page-container">
    <div class="content-container">
      <section class="section-container">...</section>
    </div>
  </main>
</div>

<!-- Dashboard grid layout -->
<div class="dashboard-layout">
  <div class="dashboard-grid">
    <div class="dashboard-panel">...</div>
  </div>
</div>

<!-- Viewport & Canvas -->
<div class="viewport-canvas">...</div>
<div class="workspace-canvas">...</div>

<!-- Fluid containers -->
<div class="fluid-container">...</div>   <!-- full-width, responsive padding -->
<div class="fixed-container">...</div>  <!-- max-width constrained -->

<!-- Sticky header -->
<header class="sticky-header">...</header>

<!-- Page States -->
<div class="loading-view">Loading...</div>
<div class="empty-view">No data found</div>
<div class="error-view">Something went wrong</div>
<div class="forbidden-view">403 — Access denied</div>
<div class="not-found-view">404 — Page not found</div>
<div class="offline-view">No internet connection</div>
<div class="success-view">Done!</div>

<!-- Next.js specific page states -->
<div class="nextjs-not-found">Not Found Page</div>
<div class="nextjs-error">Error Page</div>
<div class="nextjs-loading">Loading Page</div>
```

### Typography System

```html
<!-- Headings -->
<h1 class="heading-1">Display Heading</h1>
<h2 class="heading-2">Section Heading</h2>
<h3 class="heading-3">Subsection</h3>
<h4 class="heading-4">Group Heading</h4>

<!-- Text sizes -->
<p class="text-xs">Extra small</p>
<p class="text-sm">Small</p>
<p class="text-base">Base</p>
<p class="text-lg">Large</p>
<p class="text-xl">Extra large</p>
<p class="text-2xl">2XL</p>
<p class="text-4xl">4XL</p>
<p class="text-6xl">6XL</p>

<!-- Fluid font sizes (viewport-responsive) -->
<h1 class="text-fluid-xl">Fluid Headline</h1>
<p class="text-fluid-base">Fluid paragraph</p>

<!-- Font weights -->
<p class="font-thin">Thin 100</p>
<p class="font-normal">Normal 400</p>
<p class="font-semibold">Semibold 600</p>
<p class="font-bold">Bold 700</p>
<p class="font-black">Black 900</p>

<!-- Font families -->
<p class="font-sans">Sans-serif (default)</p>
<p class="font-mono">Monospace</p>
<p class="font-serif">Serif / display</p>

<!-- Text colors -->
<p class="text-primary">Primary text</p>
<p class="text-secondary">Secondary text</p>
<p class="text-muted">Muted text</p>
<p class="text-gold">Gold accent</p>
<p class="text-success">Success green</p>
<p class="text-danger">Danger red</p>

<!-- Text transforms -->
<p class="uppercase tracking-widest">EYEBROW LABEL</p>
<p class="capitalize">Capitalized Text</p>

<!-- Special text effects -->
<p class="watermark-text">Watermark Background</p>
<span class="letter-spacing-wide">Wide Letter Spacing</span>

<!-- Star rating display -->
<span class="star-gold">★★★★★</span>
```

### Badges & Tags

```html
<!-- Standard badges -->
<span class="badge">Default</span>
<span class="badge badge-success">Success</span>
<span class="badge badge-warning">Warning</span>
<span class="badge badge-danger">Danger</span>
<span class="badge badge-info">Info</span>

<!-- Neon glow badges -->
<span class="badge-neon-cyan">Cyan Neon</span>
<span class="badge-neon-purple">Purple Neon</span>
<span class="badge-neon-gold">Gold Neon</span>

<!-- Live status dot badge -->
<span class="live-dot-badge">LIVE</span>

<!-- User status chips -->
<span class="status-chip-online">Online</span>
<span class="status-chip-away">Away</span>
<span class="status-chip-busy">Busy</span>

<!-- Floating badge chip -->
<div class="floating-badge-chip">New Feature</div>

<!-- Tags & chips -->
<div class="tags-group">
  <span class="tag">React</span>
  <span class="tag">TypeScript</span>
  <span class="tag tag-removable">CSS <button class="tag-remove-btn">×</button></span>
</div>

<!-- Cart badge pulse animation -->
<span class="cart-badge-pulse">3</span>

<!-- Section eyebrow label -->
<span class="section-eyebrow">FEATURED</span>
```

### Cards

```html
<!-- Base card -->
<div class="card">
  <div class="card-header">Title</div>
  <div class="card-body">Content here</div>
  <div class="card-footer">Footer</div>
</div>

<!-- Card variants -->
<div class="card card-dark">Dark surface card</div>
<div class="card card-bordered">Bordered card</div>
<div class="card card-elevated">Elevated shadow card</div>
<div class="card card-glass">Glassmorphism card</div>
<div class="card card-compact">Compact padding</div>

<!-- Feature card dark (ecommerce/marketing) -->
<div class="feature-card-dark">
  <div class="card-header">Premium</div>
  <div class="card-body">...</div>
</div>

<!-- Interactive card with ambient glow on hover -->
<div class="card-interactive">Hover me</div>

<!-- Pricing card (highlighted/popular) -->
<div class="pricing-card-featured">
  <span class="popular-badge">Most Popular</span>
  ...
</div>

<!-- Stat/Metric card -->
<div class="metric-stat-card">
  <div class="stat-value">12,430</div>
  <div class="stat-label">Total Users</div>
  <div class="stat-delta stat-delta-up">+8.2%</div>
</div>
```

### Forms

```html
<!-- Form layout -->
<form class="form">
  <div class="form-group">
    <label class="form-label">Email Address</label>
    <input class="form-input" type="email" placeholder="you@example.com" />
    <span class="form-hint">We'll never share your email.</span>
  </div>

  <div class="form-group">
    <label class="form-label">Password</label>
    <input class="form-input form-input-password" type="password" />
  </div>

  <!-- Textarea -->
  <div class="form-group">
    <label class="form-label">Message</label>
    <textarea class="form-textarea">...</textarea>
  </div>

  <!-- Select -->
  <div class="form-group">
    <label class="form-label">Country</label>
    <select class="form-select">
      <option>United States</option>
    </select>
  </div>

  <!-- Checkbox -->
  <div class="form-check">
    <input class="form-checkbox" type="checkbox" id="agree" />
    <label class="form-check-label" for="agree">I agree to the terms</label>
  </div>

  <!-- Radio -->
  <div class="form-check">
    <input class="form-radio" type="radio" name="plan" />
    <label class="form-check-label">Pro Plan</label>
  </div>

  <!-- Toggle switch -->
  <div class="toggle-switch">
    <input class="toggle-switch-input" type="checkbox" />
    <span class="toggle-switch-track"></span>
    <span class="toggle-switch-thumb"></span>
  </div>
</form>

<!-- Search input -->
<div class="search-bar">
  <input class="search-input" type="search" placeholder="Search anything..." />
</div>

<!-- Prompt / AI input bar -->
<div class="prompt-input-bar">
  <input class="prompt-input" type="text" placeholder="Ask anything..." />
  <div class="prompt-suggestions">
    <button class="prompt-suggestion-chip">Summarize</button>
  </div>
</div>

<!-- Color picker & time picker -->
<input class="color-picker" type="color" />
<input class="time-picker" type="time" />

<!-- Multi-select / combobox -->
<div class="multi-select">
  <div class="multi-select-value">Selected items</div>
  <div class="multi-select-dropdown">...</div>
</div>
```

### Alerts & Feedback

```html
<!-- Standard alerts -->
<div class="alert alert-success">✅ Profile updated successfully!</div>
<div class="alert alert-warning">⚠️ Your plan expires in 3 days.</div>
<div class="alert alert-danger">❌ Failed to save changes. Please retry.</div>
<div class="alert alert-info">ℹ️ New version 2.0 is now available.</div>

<!-- Snackbar / Toast notifications -->
<div class="snackbar snackbar-success">Saved to cloud</div>
<div class="snackbar snackbar-error">Upload failed</div>
<div class="snackbar snackbar-warning">Low disk space</div>
<div class="snackbar snackbar-info">Sync complete</div>

<!-- Success/Error message cards -->
<div class="message-success">
  <strong>Payment complete!</strong> Your order has been placed.
</div>
<div class="message-error">
  <strong>Error 500:</strong> Internal server error.
</div>

<!-- Progress bars -->
<div class="progress">
  <div class="progress-bar" style="width: 65%"></div>
</div>
<div class="progress progress-success">
  <div class="progress-bar" style="width: 100%"></div>
</div>
```

### Navigation

```html
<!-- App bar / top nav -->
<header class="app-bar">
  <div class="nav-brand">UnifyCSS</div>
  <nav class="nav-links">
    <a class="nav-link" href="/">Home</a>
    <a class="nav-link nav-link-active" href="/docs">Docs</a>
    <a class="nav-link nav-link-fancy" href="/pricing">Pricing</a>
  </nav>
</header>

<!-- Side navigation (sidebar) -->
<aside class="side-nav">
  <div class="side-nav-group">
    <div class="side-nav-label">GETTING STARTED</div>
    <a class="side-nav-link">Introduction</a>
    <a class="side-nav-link side-nav-link-active">Quick Start</a>
  </div>
</aside>

<!-- Bottom navigation (mobile) -->
<nav class="bottom-nav">
  <button class="bottom-nav-item">Home</button>
  <button class="bottom-nav-item bottom-nav-active">Explore</button>
  <button class="bottom-nav-item">Profile</button>
</nav>

<!-- Floating bottom bar -->
<div class="mobile-bottom-bar">
  <button class="mobile-bottom-bar-item">
    <span class="icon">🏠</span>
    <span class="label">Home</span>
  </button>
</div>

<!-- macOS-style floating dock -->
<div class="dock">
  <button class="dock-item">📁</button>
  <button class="dock-item">🌐</button>
  <button class="dock-item">⚙️</button>
</div>

<!-- Menubar -->
<div class="menubar">
  <button class="menubar-item">File</button>
  <button class="menubar-item">Edit</button>
  <button class="menubar-item">View</button>
</div>

<!-- Pagination -->
<div class="pagination">
  <button class="page-btn page-btn-prev">←</button>
  <button class="page-btn">1</button>
  <button class="page-btn page-btn-active">2</button>
  <button class="page-btn">3</button>
  <button class="page-btn page-btn-next">→</button>
</div>
```

### Modals & Overlays

```html
<!-- Modal -->
<div class="modal-backdrop">
  <div class="modal">
    <div class="modal-header">Confirm Action</div>
    <div class="modal-body">Are you sure you want to delete this?</div>
    <div class="modal-footer">
      <button class="btn-ghost">Cancel</button>
      <button class="btn-danger">Delete</button>
    </div>
  </div>
</div>

<!-- Glass modal -->
<div class="glass-modal-container">
  <div class="glass-modal-popup">...</div>
</div>

<!-- Backdrop dim overlay -->
<div class="backdrop-dim">...</div>

<!-- Mobile bottom sheet -->
<div class="bottom-sheet">
  <div class="bottom-sheet-handle"></div>
  <div class="bottom-sheet-content">...</div>
</div>

<!-- Command palette (⌘K spotlight) -->
<div class="command-palette">
  <input class="command-palette-input" type="text" placeholder="Type a command..." />
  <div class="command-palette-list">
    <div class="command-palette-item">New File</div>
    <div class="command-palette-item command-palette-item-active">Open Terminal</div>
  </div>
</div>

<!-- Notification center -->
<div class="notifications-center">
  <div class="notification-item notification-unread">
    <span class="notification-icon">🔔</span>
    <p class="notification-text">New comment on your post</p>
  </div>
</div>

<!-- Full-screen loading overlay -->
<div class="loading-overlay">
  <div class="loading-spinner"></div>
</div>
```

### Data Tables

```html
<!-- Standard data table -->
<div class="data-table-container">
  <table class="data-table">
    <thead class="data-table-head">
      <tr>
        <th class="data-table-th">Name</th>
        <th class="data-table-th">Status</th>
        <th class="data-table-th">Actions</th>
      </tr>
    </thead>
    <tbody>
      <tr class="data-table-row">
        <td class="data-table-cell">John Doe</td>
        <td class="data-table-cell"><span class="badge badge-success">Active</span></td>
        <td class="data-table-cell">
          <button class="btn-ghost btn-sm">Edit</button>
          <button class="btn-ghost-danger btn-sm">Delete</button>
        </td>
      </tr>
    </tbody>
  </table>
</div>

<!-- Data grid with control bar -->
<div class="data-grid">
  <div class="data-grid-controls">
    <input class="search-input" placeholder="Filter rows..." />
    <button class="btn-primary btn-sm">Export</button>
  </div>
  <div class="data-grid-body">...</div>
</div>
```

### Loading & Skeleton

```html
<!-- Loading spinners -->
<div class="loading-spinner"></div>
<div class="loading-spinner-lg"></div>

<!-- Pulsing 3-dot spinner -->
<div class="dots-spinner">
  <span></span><span></span><span></span>
</div>

<!-- Skeleton placeholder blocks -->
<div class="skeleton-pulse"></div>
<div class="skeleton-text"></div>
<div class="skeleton-avatar"></div>
<div class="skeleton-card"></div>

<!-- Shimmer wave (card loading state) -->
<div class="shimmer-wave">
  <div class="shimmer-line"></div>
  <div class="shimmer-line shimmer-line-short"></div>
</div>

<!-- Circular progress arcs (e.g. storage/upload) -->
<div class="progress-circular">
  <svg class="progress-circular-ring">...</svg>
  <span class="progress-circular-label">72%</span>
</div>

<!-- Suspense boundary fallback -->
<div class="suspense-boundary">
  <div class="suspense-spinner"></div>
</div>

<!-- Lazy loader display -->
<div class="lazy-loader">
  <div class="skeleton-pulse"></div>
</div>
```

### Tabs & Pills

```html
<!-- Standard tabs -->
<div class="tabs-container">
  <button class="tab-btn">Overview</button>
  <button class="tab-btn tab-btn-active">Analytics</button>
  <button class="tab-btn">Settings</button>
</div>
<div class="tab-panel">Tab content here</div>

<!-- Pill tabs -->
<div class="pill-tabs">
  <button class="pill-tab">Day</button>
  <button class="pill-tab pill-tab-active">Week</button>
  <button class="pill-tab">Month</button>
</div>
```

### Glassmorphism Effects

```html
<!-- Frosted glass panel -->
<div class="glass-panel">Content inside glass panel</div>

<!-- Glass panel with inner highlight border -->
<div class="glass-frosted">...</div>

<!-- Gradient border container -->
<div class="gradient-border">
  <div class="gradient-border-inner">Content</div>
</div>

<!-- Frosted glass button -->
<button class="btn-glass">Glass Button</button>

<!-- Ambient glow aura (marketing hero sections) -->
<div class="glow-aura glow-aura-brand">...</div>
<div class="glow-aura glow-aura-gold">...</div>

<!-- Hero radiant glow background -->
<section class="hero-radiant">
  <div class="hero-content">...</div>
</section>

<!-- Pill glow action button -->
<button class="pill-glow-btn">Explore Now</button>
```

### Kanban & Dashboard

```html
<!-- Kanban board -->
<div class="kanban-board">
  <div class="kanban-column">
    <div class="kanban-column-header">To Do</div>
    <div class="kanban-card">Task 1</div>
    <div class="kanban-card">Task 2</div>
  </div>
  <div class="kanban-column">
    <div class="kanban-column-header">In Progress</div>
    <div class="kanban-card kanban-card-active">Task 3</div>
  </div>
  <div class="kanban-column">
    <div class="kanban-column-header">Done</div>
    <div class="kanban-card kanban-card-done">Task 4</div>
  </div>
</div>

<!-- Bento dashboard grids -->
<div class="bento-grid">
  <div class="bento-cell bento-wide">Wide cell (analytics)</div>
  <div class="bento-cell">Small cell</div>
  <div class="bento-cell">Small cell</div>
  <div class="bento-cell bento-tall">Tall cell (chart)</div>
</div>

<!-- Filter panel with chips -->
<div class="filter-panel">
  <span class="filter-chip">All</span>
  <span class="filter-chip filter-chip-active">Active</span>
  <span class="filter-chip">Archived</span>
</div>
```

### Media & Camera Views

```html
<!-- Webcam / camera frame -->
<div class="webcam-view">
  <video class="webcam-feed" autoplay muted></video>
  <div class="webcam-overlay">
    <span class="live-rec-badge">● REC</span>
  </div>
</div>

<!-- Image cropper -->
<div class="cropper-container">
  <div class="cropper-overlay"></div>
  <div class="cropper-handles"></div>
</div>

<!-- Audio recorder with waveform -->
<div class="audio-recorder">
  <button class="audio-rec-btn">⏺ Record</button>
  <div class="audio-waveform">
    <span class="waveform-bar"></span>
  </div>
</div>

<!-- Screen recorder -->
<div class="screen-recorder-box">
  <span class="live-rec-badge">● LIVE</span>
</div>

<!-- File upload dropzone -->
<div class="upload-dropzone">
  <p>Drag & drop files here or <span class="upload-link">browse</span></p>
</div>

<!-- Upload queue -->
<div class="upload-queue">
  <div class="upload-item">
    <span class="upload-filename">design.figma</span>
    <div class="progress"><div class="progress-bar" style="width: 60%"></div></div>
    <span class="upload-size">4.2 MB</span>
  </div>
</div>
```

### AI & Chat Interfaces

```html
<!-- AI chat container -->
<div class="ai-chat-container">
  <div class="chat-message chat-message-user">
    <div class="chat-bubble chat-bubble-user">Hello!</div>
  </div>
  <div class="chat-message chat-message-ai">
    <div class="chat-bubble chat-bubble-ai">Hi! How can I help?</div>
  </div>
</div>

<!-- Streaming text cursor (typing animation) -->
<span class="streaming-cursor"></span>

<!-- AI citation badge -->
<span class="ai-citation-badge">[1]</span>

<!-- Regenerate response button -->
<button class="ai-regen-btn">↻ Regenerate</button>

<!-- Mention popup (@user suggestions) -->
<div class="mention-popup">
  <div class="mention-item">@johndoe</div>
  <div class="mention-item mention-item-active">@janedoe</div>
</div>
```

---

## Utility Reference

### Spacing & Sizing

```html
<!-- Margin -->
<div class="m-4">All sides margin (1rem)</div>
<div class="mx-auto">Auto horizontal margin</div>
<div class="mt-8">Top margin (2rem)</div>
<div class="mb-2">Bottom margin (0.5rem)</div>

<!-- Padding -->
<div class="p-6">All sides padding (1.5rem)</div>
<div class="px-4 py-2">Horizontal + vertical padding</div>

<!-- Gap (flex/grid) -->
<div class="flex gap-4">Items with gap</div>
<div class="grid gap-6">Grid with gap</div>

<!-- Sizing -->
<div class="w-full">Full width</div>
<div class="w-1/2">50% width</div>
<div class="h-screen">Full viewport height</div>
<div class="min-h-screen">Min full viewport height</div>
<div class="max-w-3xl mx-auto">Max-width centered</div>
```

### Colors & Backgrounds

```html
<!-- Background colors -->
<div class="bg-dark-base">Deep dark background</div>
<div class="bg-dark-100">Surface background</div>
<div class="bg-brand-primary">Brand primary</div>
<div class="bg-success">Success green</div>
<div class="bg-danger">Danger red</div>

<!-- Gold backgrounds -->
<div class="bg-gold">Gold fill</div>
<div class="bg-gold-subtle">Subtle gold tint</div>

<!-- Gradient backgrounds -->
<div class="bg-gradient-to-r from-brand to-dark">Brand gradient →</div>
<div class="bg-gradient-to-b from-dark-base to-dark-300">Dark gradient ↓</div>
<div class="bg-dark-gold-gradient">Dark-to-gold marketing gradient</div>
<div class="bg-dark-radial">Radial dark glow background</div>

<!-- Opacity -->
<div class="opacity-50">50% opacity</div>
<div class="opacity-0">Fully transparent</div>
```

### Borders & Radius

```html
<div class="border">1px border</div>
<div class="border-2">2px border</div>
<div class="border-brand">Brand color border</div>
<div class="border-gold">Gold border</div>
<div class="border-transparent">Transparent border</div>

<div class="rounded">Default radius</div>
<div class="rounded-md">Medium radius</div>
<div class="rounded-xl">Extra-large radius</div>
<div class="rounded-full">Pill/circle radius</div>
<div class="rounded-2xl">2XL radius</div>
```

### Flexbox & Grid

```html
<!-- Flexbox -->
<div class="flex items-center justify-between">Space between</div>
<div class="flex items-center gap-4">Items with gap</div>
<div class="flex flex-col gap-6">Vertical stack</div>
<div class="flex flex-wrap gap-2">Wrapping flex</div>
<div class="inline-flex items-center">Inline flex</div>

<!-- Grid -->
<div class="grid grid-cols-3 gap-6">3-column grid</div>
<div class="grid grid-cols-2 md:grid-cols-4">Responsive grid</div>

<!-- Horizontal/vertical stacks (semantic) -->
<div class="stack-h gap-4">Horizontal stack</div>
<div class="stack-v gap-6">Vertical stack</div>
```

### Transitions & Animations

```html
<!-- Transitions -->
<div class="transition">Default transition</div>
<div class="transition-all duration-200 ease-in-out">Smooth transition</div>
<div class="transition-colors duration-150">Color transition</div>
<div class="transition-transform">Transform transition</div>

<!-- Animations -->
<div class="animate-fade-in">Fade in on mount</div>
<div class="animate-slide-up">Slide up entrance</div>
<div class="animate-spin">Rotating spinner</div>
<div class="animate-pulse">Pulse (skeleton loading)</div>
<div class="animate-bounce">Bounce</div>

<!-- Hover effects -->
<div class="lift-hover">Lifts on hover</div>
<div class="fade-up">Fades up on scroll</div>
<div class="tilt-3d">3D tilt on hover</div>
```

### Dark Mode

```html
<!-- Dark mode is automatic via CSS custom properties.
     Override by toggling the .dark class on <html> or <body>: -->
<html class="dark">
  <body>
    <!-- All UnifyCSS tokens automatically shift to dark palette -->
  </body>
</html>

<!-- Dark-mode-specific utilities -->
<p class="dark:text-white">White text in dark mode</p>
<div class="dark:bg-dark-200">Dark surface in dark mode</div>
```

### Responsive Breakpoints

```html
<!-- Breakpoints: sm (640px), md (768px), lg (1024px), xl (1280px), 2xl (1536px) -->

<div class="hidden md:block">Visible on medium+ screens</div>
<div class="block md:hidden">Visible on mobile only</div>
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3">Responsive grid</div>
<div class="text-sm md:text-base lg:text-lg">Responsive text size</div>
<p class="p-4 md:p-8">Responsive padding</p>
```

### Hover, Focus & State Variants

```html
<div class="hover:opacity-80">Dim on hover</div>
<div class="hover:scale-105">Scale up on hover</div>
<div class="hover:shadow-xl">Shadow on hover</div>
<div class="hover:-translate-y-1">Float on hover</div>
<div class="hover:text-gold">Gold on hover</div>
<div class="hover:bg-brand-primary">Fill on hover</div>

<input class="focus:outline-none focus:ring-2" />
<button class="active:scale-95">Shrink on press</button>
<button class="disabled:cursor-not-allowed disabled:opacity-50" disabled>Disabled</button>
<input class="focus-visible:ring" />
```

### Accessibility Utilities

```html
<!-- Screen reader only (visually hidden, accessible to screen readers) -->
<span class="sr-only">Loading...</span>

<!-- Undo sr-only -->
<span class="not-sr-only">Visible again</span>

<!-- Focus management -->
<div class="focus-trap">
  <!-- Traps keyboard focus inside modals -->
</div>
```

### Print Utilities

```html
<div class="print:hidden">Hidden when printing</div>
<div class="print:block">Only visible when printing</div>
<div class="print:text-black">Force black text for print</div>
```

---

## Customization

All design tokens can be customized by overriding CSS variables:

```css
/* my-theme.css */
@import '@unifycss/unifycss/unifycss.css';

:root {
  /* Change brand color system */
  --brand-primary:      #7c3aed;
  --brand-primary-dark: #5b21b6;

  /* Change gold accent */
  --gold:               #fbbf24;
  --gold-dark:          #d97706;

  /* Change radius scale */
  --radius-md:          0.75rem;
  --radius-lg:          1rem;

  /* Change typography */
  --font-sans:          'Outfit', system-ui, sans-serif;
  --font-mono:          'JetBrains Mono', monospace;

  /* Change dark surfaces */
  --dark-base:          #080810;
  --dark-200:           #12121a;
}
```

---

## Framework Integrations

| Package | Description |
|---|---|
| [`@unifycss/nextjs`](https://npmjs.com/package/@unifycss/nextjs) | Next.js 16+ with Turbopack |
| [`@unifycss/react`](https://npmjs.com/package/@unifycss/react) | React ThemeProvider & hooks |
| [`@unifycss/vite`](https://npmjs.com/package/@unifycss/vite) | Vite plugin with HMR |
| [`@unifycss/webpack`](https://npmjs.com/package/@unifycss/webpack) | Webpack 5+ plugin & loader |
| [`@unifycss/postcss`](https://npmjs.com/package/@unifycss/postcss) | PostCSS plugin |
| [`@unifycss/cli`](https://npmjs.com/package/@unifycss/cli) | Command-line interface |

---

## License

MIT © [UnifyCSS Team](https://unifycss.dev) — Crafted with 🖤 for modern web developers.
