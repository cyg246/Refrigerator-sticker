# Cinematic Space-Travel Landing Page Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build a CDN-only React single-page landing page with two cinematic video sections, liquid-glass UI, Framer Motion entrances, and custom requestAnimationFrame video crossfades.

**Architecture:** Deliver a single standalone HTML artifact that loads React, ReactDOM, Babel, Tailwind, and Framer Motion from CDNs, defines shared CSS and Tailwind config in the document head, and mounts a React app into `#root`. Split the page logic into Babel script blocks that export components onto `window`, then compose them in a final `App` block.

**Tech Stack:** HTML, Tailwind CDN, React 18 UMD, ReactDOM 18 UMD, Babel Standalone, Framer Motion UMD

---

### Task 1: Create the standalone landing page artifact

**Files:**
- Create: `D:\冰箱贴活动\docs\superpowers\previews\space-travel-landing.html`

- [ ] **Step 1: Define the document shell and CDN dependencies**

Create a full HTML document with:

- `#root` mount node
- Google Fonts import for `Instrument Serif` and `Barlow`
- exact CDN scripts from the prompt
- Tailwind config that registers `font-heading`, `font-body`, and `borderRadius.DEFAULT = "9999px"`
- global black body background

- [ ] **Step 2: Add the exact liquid-glass CSS system**

Embed a `<style>` block containing:

- `.liquid-glass`
- `.liquid-glass::before`
- `.liquid-glass-strong`
- `.liquid-glass-strong::before`

Use the exact blur, inset shadow, and gradient border-mask treatment from the prompt.

- [ ] **Step 3: Implement React component scripts**

Define the following in separate `<script type="text/babel">` blocks, each exported via `window.X = X`:

- `window.Icons`
- `window.FadingVideo`
- `window.BlurText`
- `window.HeroSection`
- `window.CapabilitiesSection`
- `window.App`

- [ ] **Step 4: Mount the React app**

Mount `window.App` into `#root` with `ReactDOM.createRoot(...).render(...)`.

### Task 2: Implement the shared motion and video behavior

**Files:**
- Modify: `D:\冰箱贴活动\docs\superpowers\previews\space-travel-landing.html`

- [ ] **Step 1: Build the `FadingVideo` component**

Implement:

- `FADE_MS = 500`
- `FADE_OUT_LEAD = 0.55`
- `requestAnimationFrame`-driven `fadeTo`
- manual `ended` loop reset
- no CSS transition-based fades
- listener cleanup and `cancelAnimationFrame` on unmount

- [ ] **Step 2: Build the `BlurText` component**

Implement:

- IntersectionObserver trigger at 10% visibility
- word splitting by spaces
- word-by-word Framer Motion blur and y-axis animation
- inline-block words with `marginRight: "0.28em"`
- flex wrapping parent line

- [ ] **Step 3: Add Framer Motion entrance choreography**

Apply consistent `initial: { filter: "blur(10px)", opacity: 0, y: 20 }` and eased reveals to hero badge, subheading, CTAs, stats, and partner cluster.

### Task 3: Build the Hero and Capabilities sections

**Files:**
- Modify: `D:\冰箱贴活动\docs\superpowers\previews\space-travel-landing.html`

- [ ] **Step 1: Build the fixed navbar and Hero section**

Implement:

- fixed top navbar
- left circular logo
- desktop-only center nav pill
- white `Claim a Spot` pill
- hero badge
- `BlurText` headline
- subheading
- primary and secondary CTAs
- two stat cards
- partner chip and partner names
- hero background video with 120% scale and `object-top`

- [ ] **Step 2: Build the Capabilities section**

Implement:

- full-screen second section
- full-bleed looping background video
- heading block
- three liquid-glass capability cards
- nested icon tiles
- top-right chip clusters
- serif card titles and body copy

- [ ] **Step 3: Keep the entire page white-on-black with no overlay**

Ensure contrast comes from layout, typography, and glass chrome rather than dark scrims.

### Task 4: Verify the local preview artifact

**Files:**
- Test: `D:\冰箱贴活动\docs\superpowers\previews\space-travel-landing.html`

- [ ] **Step 1: Request the page over the local preview server**

Use the current local static server to request the file and confirm HTTP 200.

- [ ] **Step 2: Verify key strings exist in the generated HTML**

Check for:

- hero headline text
- capabilities heading
- video URLs
- `window.Motion = window.FramerMotion`

- [ ] **Step 3: Confirm delivery path**

Report the preview URL and file path clearly for review.
