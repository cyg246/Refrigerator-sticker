# Fridge Magnet Admin Upload Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Add a lightweight admin upload panel to the current exhibition page so new works can be added directly in the browser and persist locally.

**Architecture:** Keep the current single-file static page and layer an admin management flow into it. Store uploaded works in `localStorage`, including image data URLs, then merge them with the built-in default works at render time.

**Tech Stack:** HTML, CSS, vanilla JavaScript, localStorage, FileReader

---

### Task 1: Add admin entry and panel shell

**Files:**
- Modify: `D:\冰箱贴活动\docs\superpowers\previews\space-travel-landing.html`

- [ ] Add a visible but tasteful admin trigger in the navbar or page chrome.
- [ ] Add an upload panel overlay/drawer with fields for title, concept, student ID, and image.
- [ ] Add close/cancel controls and visual consistency with the liquid-glass system.

### Task 2: Add client-side upload logic

**Files:**
- Modify: `D:\冰箱贴活动\docs\superpowers\previews\space-travel-landing.html`

- [ ] Add `localStorage` key management for uploaded works.
- [ ] Add image file reading via `FileReader` and preview rendering.
- [ ] Add form validation for required fields.
- [ ] Save new works into local storage and re-render both featured/archive sections.

### Task 3: Keep the page coherent after uploads

**Files:**
- Modify: `D:\冰箱贴活动\docs\superpowers\previews\space-travel-landing.html`

- [ ] Merge built-in works with uploaded works in one render path.
- [ ] Decide featured works from the first three items in the merged list.
- [ ] Ensure uploaded works appear in the archive wall and modal detail flow.

### Task 4: Verify the static preview still works

**Files:**
- Test: `D:\冰箱贴活动\docs\superpowers\previews\space-travel-landing.html`

- [ ] Confirm the page returns HTTP 200.
- [ ] Confirm the admin trigger is present in the HTML.
- [ ] Confirm the upload form fields are present in the HTML.
