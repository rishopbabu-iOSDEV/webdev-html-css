# HTML & CSS — Flexbox, Grid & Layout Practice

---

## Overview

This file gives you three sets of starter exercises — one for Flexbox, one for CSS Grid, and one comparing both. Each exercise has the HTML already written. Your job is to fill in the missing CSS marked with `/* TODO */`.

Every exercise uses real HTML tags and real CSS properties from the playground. By the end, you will have used every major layout property covered in class.

---

## How to Use This File

1. Create a new folder called `layout-practice/`
2. Inside it, create three files:
   - `flexbox-starter.html`
   - `grid-starter.html`
   - flex-vs-grid-starter.html`
3. Copy each starter block below into its file
4. Open the file in your browser
5. Fill in every `/* TODO */` comment with the correct CSS value
6. Reload the browser after each change to see the result

---

## Part 1 — Flexbox Starter

Copy this into `flexbox-starter.html`.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Flexbox Practice</title>
  <style>

    /* ── RESET ── */
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: 'Segoe UI', Arial, sans-serif;
      background: #f0f4f8;
      color: #0f172a;
      padding: 32px;
    }

    /* ── SHARED CELL STYLES ── */
    .cell {
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: 800;
      font-size: 0.9rem;
      color: #fff;
      border-radius: 8px;
      width: 60px;
      height: 60px;
    }
    .c1 { background: #4f46e5; }
    .c2 { background: #7c3aed; }
    .c3 { background: #0891b2; }
    .c4 { background: #059669; }
    .c5 { background: #d97706; }
    .c6 { background: #dc2626; }

    /* ── EXERCISE CONTAINER ── */
    .exercise {
      background: #fff;
      border: 1px solid #e2e8f0;
      border-radius: 12px;
      padding: 24px;
      margin-bottom: 36px;
    }
    .exercise h2 {
      font-size: 1rem;
      font-weight: 700;
      margin-bottom: 4px;
    }
    .exercise p {
      font-size: 0.85rem;
      color: #64748b;
      margin-bottom: 16px;
      line-height: 1.6;
    }
    .exercise code {
      background: #f1f5f9;
      padding: 2px 6px;
      border-radius: 4px;
      font-size: 0.8rem;
      font-family: monospace;
      color: #4f46e5;
    }
    hr {
      border: none;
      border-top: 1px solid #e2e8f0;
      margin: 36px 0;
    }

    /* ══════════════════════════════════════════
       EXERCISE 1 — display: flex
       Goal: make the items sit in a row
    ══════════════════════════════════════════ */
    #ex1-box {
      display: /* TODO: turn this into a flex container */;
      background: #f8fafc;
      border: 1px dashed #c7d2fe;
      border-radius: 8px;
      padding: 16px;
      gap: 10px;
    }

    /* ══════════════════════════════════════════
       EXERCISE 2 — flex-direction
       Goal: stack A B C D vertically (column)
    ══════════════════════════════════════════ */
    #ex2-box {
      display: flex;
      flex-direction: /* TODO: column or row? */;
      background: #f8fafc;
      border: 1px dashed #c7d2fe;
      border-radius: 8px;
      padding: 16px;
      gap: 10px;
    }

    /* ══════════════════════════════════════════
       EXERCISE 3 — justify-content
       Goal: push items to the END of the row
    ══════════════════════════════════════════ */
    #ex3-box {
      display: flex;
      justify-content: /* TODO: flex-end / center / space-between / space-around / space-evenly */;
      background: #f8fafc;
      border: 1px dashed #c7d2fe;
      border-radius: 8px;
      padding: 16px;
      gap: 10px;
    }

    /* ══════════════════════════════════════════
       EXERCISE 4 — align-items
       Goal: center items on the cross axis
             (the box is taller than the cells)
    ══════════════════════════════════════════ */
    #ex4-box {
      display: flex;
      height: 160px;
      align-items: /* TODO: center / flex-start / flex-end / stretch / baseline */;
      background: #f8fafc;
      border: 1px dashed #c7d2fe;
      border-radius: 8px;
      padding: 16px;
      gap: 10px;
    }

    /* ══════════════════════════════════════════
       EXERCISE 5 — flex-wrap
       Goal: let items wrap to the next line
             instead of overflowing
    ══════════════════════════════════════════ */
    #ex5-box {
      display: flex;
      flex-wrap: /* TODO: wrap or nowrap? */;
      background: #f8fafc;
      border: 1px dashed #c7d2fe;
      border-radius: 8px;
      padding: 16px;
      gap: 10px;
      width: 220px;   /* intentionally narrow */
    }

    /* ══════════════════════════════════════════
       EXERCISE 6 — gap
       Goal: add 24px space between all items
    ══════════════════════════════════════════ */
    #ex6-box {
      display: flex;
      gap: /* TODO: a px value */;
      background: #f8fafc;
      border: 1px dashed #c7d2fe;
      border-radius: 8px;
      padding: 16px;
    }

    /* ══════════════════════════════════════════
       EXERCISE 7 — flex-grow
       Goal: make item B fill all leftover space
    ══════════════════════════════════════════ */
    #ex7-box {
      display: flex;
      gap: 10px;
      background: #f8fafc;
      border: 1px dashed #c7d2fe;
      border-radius: 8px;
      padding: 16px;
    }
    #ex7-b {
      flex-grow: /* TODO: 0 or 1? */;
      width: auto;
    }

    /* ══════════════════════════════════════════
       EXERCISE 8 — align-self
       Goal: push item C alone to the bottom
             while A and B stay at the top
    ══════════════════════════════════════════ */
    #ex8-box {
      display: flex;
      align-items: flex-start;
      height: 140px;
      gap: 10px;
      background: #f8fafc;
      border: 1px dashed #c7d2fe;
      border-radius: 8px;
      padding: 16px;
    }
    #ex8-c {
      align-self: /* TODO: flex-end / center / stretch */;
    }

    /* ══════════════════════════════════════════
       EXERCISE 9 — order
       Goal: visually reorder so C appears first,
             then A, then B — without touching HTML
    ══════════════════════════════════════════ */
    #ex9-box {
      display: flex;
      gap: 10px;
      background: #f8fafc;
      border: 1px dashed #c7d2fe;
      border-radius: 8px;
      padding: 16px;
    }
    #ex9-a { order: /* TODO */; }
    #ex9-b { order: /* TODO */; }
    #ex9-c { order: /* TODO */; }

    /* ══════════════════════════════════════════
       EXERCISE 10 — CHALLENGE
       Build a nav bar: logo on the left,
       links centered, a button on the right.
       Do not change the HTML.
    ══════════════════════════════════════════ */
    #ex10-nav {
      display: flex;
      align-items: center;
      /* TODO: distribute space so logo is left,
               links are center, button is right */
      background: #0f172a;
      padding: 14px 24px;
      border-radius: 10px;
    }
    #ex10-logo {
      color: #fff;
      font-weight: 800;
      font-size: 1.1rem;
    }
    #ex10-links {
      display: flex;
      gap: 24px;
      /* TODO: grow to fill remaining space so
               links naturally center */
      justify-content: center;
    }
    #ex10-links a {
      color: #94a3b8;
      text-decoration: none;
      font-size: 0.88rem;
    }
    #ex10-btn {
      background: #4f46e5;
      color: #fff;
      border: none;
      padding: 8px 18px;
      border-radius: 8px;
      font-size: 0.85rem;
      font-weight: 700;
      cursor: pointer;
      white-space: nowrap;
    }

  </style>
</head>
<body>

  <h1 style="font-size:1.4rem;font-weight:800;margin-bottom:6px;">⚡ Flexbox Practice</h1>
  <p style="color:#64748b;font-size:.88rem;margin-bottom:32px;">Fill in every <code style="background:#f1f5f9;padding:2px 6px;border-radius:4px;font-family:monospace;color:#4f46e5;">/* TODO */</code> in the CSS. Do not change the HTML.</p>

  <!-- Exercise 1 -->
  <section class="exercise">
    <h2>Exercise 1 — display: flex</h2>
    <p><strong>What to do:</strong> Add <code>display: flex</code> to <code>#ex1-box</code> so A B C sit in a row.</p>
    <div id="ex1-box">
      <div class="cell c1">A</div>
      <div class="cell c2">B</div>
      <div class="cell c3">C</div>
    </div>
  </section>

  <!-- Exercise 2 -->
  <section class="exercise">
    <h2>Exercise 2 — flex-direction</h2>
    <p><strong>What to do:</strong> Change <code>flex-direction</code> so A B C D stack vertically.</p>
    <div id="ex2-box">
      <div class="cell c1">A</div>
      <div class="cell c2">B</div>
      <div class="cell c3">C</div>
      <div class="cell c4">D</div>
    </div>
  </section>

  <!-- Exercise 3 -->
  <section class="exercise">
    <h2>Exercise 3 — justify-content</h2>
    <p><strong>What to do:</strong> Set <code>justify-content</code> so A B C are pushed to the right end of the box.</p>
    <div id="ex3-box">
      <div class="cell c1">A</div>
      <div class="cell c2">B</div>
      <div class="cell c3">C</div>
    </div>
  </section>

  <!-- Exercise 4 -->
  <section class="exercise">
    <h2>Exercise 4 — align-items</h2>
    <p><strong>What to do:</strong> Center A B C vertically inside the tall box using <code>align-items</code>.</p>
    <div id="ex4-box">
      <div class="cell c1">A</div>
      <div class="cell c2">B</div>
      <div class="cell c3">C</div>
    </div>
  </section>

  <!-- Exercise 5 -->
  <section class="exercise">
    <h2>Exercise 5 — flex-wrap</h2>
    <p><strong>What to do:</strong> The box is only 220px wide. Add <code>flex-wrap</code> so items wrap to the next row instead of overflowing.</p>
    <div id="ex5-box">
      <div class="cell c1">A</div>
      <div class="cell c2">B</div>
      <div class="cell c3">C</div>
      <div class="cell c4">D</div>
      <div class="cell c5">E</div>
    </div>
  </section>

  <!-- Exercise 6 -->
  <section class="exercise">
    <h2>Exercise 6 — gap</h2>
    <p><strong>What to do:</strong> Add a <code>gap</code> of 24px between the items.</p>
    <div id="ex6-box">
      <div class="cell c1">A</div>
      <div class="cell c2">B</div>
      <div class="cell c3">C</div>
      <div class="cell c4">D</div>
    </div>
  </section>

  <!-- Exercise 7 -->
  <section class="exercise">
    <h2>Exercise 7 — flex-grow</h2>
    <p><strong>What to do:</strong> Make item B stretch to fill all the leftover horizontal space.</p>
    <div id="ex7-box">
      <div class="cell c1">A</div>
      <div class="cell c2" id="ex7-b">B</div>
      <div class="cell c3">C</div>
    </div>
  </section>

  <!-- Exercise 8 -->
  <section class="exercise">
    <h2>Exercise 8 — align-self</h2>
    <p><strong>What to do:</strong> Use <code>align-self</code> on item C so it drops to the bottom of the box while A and B stay at the top.</p>
    <div id="ex8-box">
      <div class="cell c1">A</div>
      <div class="cell c2">B</div>
      <div class="cell c3" id="ex8-c">C</div>
    </div>
  </section>

  <!-- Exercise 9 -->
  <section class="exercise">
    <h2>Exercise 9 — order</h2>
    <p><strong>What to do:</strong> The HTML order is A → B → C. Use <code>order</code> to display them as C → A → B without touching the HTML.</p>
    <div id="ex9-box">
      <div class="cell c1" id="ex9-a">A</div>
      <div class="cell c2" id="ex9-b">B</div>
      <div class="cell c3" id="ex9-c">C</div>
    </div>
  </section>

  <!-- Exercise 10 -->
  <section class="exercise">
    <h2>Exercise 10 — Challenge: Nav Bar</h2>
    <p><strong>What to do:</strong> Complete the CSS so the nav shows: logo on the left · links centered · button on the right. Hint: <code>flex-grow: 1</code> on <code>#ex10-links</code>.</p>
    <nav id="ex10-nav">
      <span id="ex10-logo">MyApp</span>
      <div id="ex10-links">
        <a href="#">Home</a>
        <a href="#">About</a>
        <a href="#">Contact</a>
      </div>
      <button id="ex10-btn">Sign Up</button>
    </nav>
  </section>

</body>
</html>
```

---

## Part 2 — CSS Grid Starter

Copy this into `grid-starter.html`.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>CSS Grid Practice</title>
  <style>

    /* ── RESET ── */
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: 'Segoe UI', Arial, sans-serif;
      background: #f0f4f8;
      color: #0f172a;
      padding: 32px;
    }

    /* ── SHARED CELL STYLES ── */
    .cell {
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: 800;
      font-size: 0.9rem;
      color: #fff;
      border-radius: 8px;
      min-height: 56px;
    }
    .c1 { background: #4f46e5; }
    .c2 { background: #7c3aed; }
    .c3 { background: #0891b2; }
    .c4 { background: #059669; }
    .c5 { background: #d97706; }
    .c6 { background: #dc2626; }
    .c7 { background: #db2777; }
    .c8 { background: #65a30d; }

    /* ── EXERCISE CONTAINER ── */
    .exercise {
      background: #fff;
      border: 1px solid #e2e8f0;
      border-radius: 12px;
      padding: 24px;
      margin-bottom: 36px;
    }
    .exercise h2 {
      font-size: 1rem;
      font-weight: 700;
      margin-bottom: 4px;
    }
    .exercise p {
      font-size: 0.85rem;
      color: #64748b;
      margin-bottom: 16px;
      line-height: 1.6;
    }
    .exercise code {
      background: #f1f5f9;
      padding: 2px 6px;
      border-radius: 4px;
      font-size: 0.8rem;
      font-family: monospace;
      color: #6d28d9;
    }

    /* ══════════════════════════════════════════
       EXERCISE 1 — display: grid
       Goal: turn the box into a grid container
    ══════════════════════════════════════════ */
    #ex1-grid {
      display: /* TODO */;
      grid-template-columns: /* TODO: 3 equal columns */;
      gap: 10px;
      background: #f8fafc;
      border: 1px dashed #ddd6fe;
      border-radius: 8px;
      padding: 16px;
    }

    /* ══════════════════════════════════════════
       EXERCISE 2 — fr unit
       Goal: 3-column layout: 1fr 2fr 1fr
             (middle column is twice as wide)
    ══════════════════════════════════════════ */
    #ex2-grid {
      display: grid;
      grid-template-columns: /* TODO: 1fr 2fr 1fr */;
      gap: 10px;
      background: #f8fafc;
      border: 1px dashed #ddd6fe;
      border-radius: 8px;
      padding: 16px;
    }

    /* ══════════════════════════════════════════
       EXERCISE 3 — repeat()
       Goal: create 4 equal columns using repeat()
    ══════════════════════════════════════════ */
    #ex3-grid {
      display: grid;
      grid-template-columns: /* TODO: repeat(4, 1fr) */;
      gap: 10px;
      background: #f8fafc;
      border: 1px dashed #ddd6fe;
      border-radius: 8px;
      padding: 16px;
    }

    /* ══════════════════════════════════════════
       EXERCISE 4 — grid-template-rows
       Goal: first row 80px tall, second row 40px
    ══════════════════════════════════════════ */
    #ex4-grid {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      grid-template-rows: /* TODO: 80px 40px */;
      gap: 10px;
      background: #f8fafc;
      border: 1px dashed #ddd6fe;
      border-radius: 8px;
      padding: 16px;
    }

    /* ══════════════════════════════════════════
       EXERCISE 5 — gap (row and column separately)
       Goal: row-gap 20px, column-gap 8px
    ══════════════════════════════════════════ */
    #ex5-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      row-gap: /* TODO */;
      column-gap: /* TODO */;
      background: #f8fafc;
      border: 1px dashed #ddd6fe;
      border-radius: 8px;
      padding: 16px;
    }

    /* ══════════════════════════════════════════
       EXERCISE 6 — grid-column: span
       Goal: make item A span across 2 columns
    ══════════════════════════════════════════ */
    #ex6-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 10px;
      background: #f8fafc;
      border: 1px dashed #ddd6fe;
      border-radius: 8px;
      padding: 16px;
    }
    #ex6-a {
      grid-column: /* TODO: span 2 */;
    }

    /* ══════════════════════════════════════════
       EXERCISE 7 — grid-row: span
       Goal: make item A span 2 rows tall
    ══════════════════════════════════════════ */
    #ex7-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      grid-template-rows: repeat(2, 70px);
      gap: 10px;
      background: #f8fafc;
      border: 1px dashed #ddd6fe;
      border-radius: 8px;
      padding: 16px;
    }
    #ex7-a {
      grid-row: /* TODO: span 2 */;
    }

    /* ══════════════════════════════════════════
       EXERCISE 8 — grid-template-areas
       Goal: named layout:
         header header header
         sidebar  main  main
         footer  footer footer
    ══════════════════════════════════════════ */
    #ex8-grid {
      display: grid;
      grid-template-columns: 160px 1fr 1fr;
      grid-template-rows: 56px 120px 48px;
      gap: 10px;
      grid-template-areas:
        /* TODO: fill in the 3 rows as strings */
        "..."
        "..."
        "...";
      background: #f8fafc;
      border: 1px dashed #ddd6fe;
      border-radius: 8px;
      padding: 16px;
    }
    #ex8-header  { grid-area: /* TODO */; }
    #ex8-sidebar { grid-area: /* TODO */; }
    #ex8-main    { grid-area: /* TODO */; }
    #ex8-footer  { grid-area: /* TODO */; }

    /* ══════════════════════════════════════════
       EXERCISE 9 — auto rows
       Goal: every auto-created row is 60px tall
    ══════════════════════════════════════════ */
    #ex9-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      grid-auto-rows: /* TODO: 60px */;
      gap: 10px;
      background: #f8fafc;
      border: 1px dashed #ddd6fe;
      border-radius: 8px;
      padding: 16px;
    }

    /* ══════════════════════════════════════════
       EXERCISE 10 — CHALLENGE: Magazine Layout
       Goal:
         - 3 columns
         - Item A spans all 3 columns (hero)
         - Items B, C, D fill one column each
         - Item E spans 2 columns (featured)
         - Item F fills one column
    ══════════════════════════════════════════ */
    #ex10-grid {
      display: grid;
      grid-template-columns: /* TODO */;
      gap: 12px;
      background: #f8fafc;
      border: 1px dashed #ddd6fe;
      border-radius: 8px;
      padding: 16px;
    }
    #ex10-a { grid-column: /* TODO */; min-height: 80px; }
    #ex10-e { grid-column: /* TODO */; }

  </style>
</head>
<body>

  <h1 style="font-size:1.4rem;font-weight:800;margin-bottom:6px;">▦ CSS Grid Practice</h1>
  <p style="color:#64748b;font-size:.88rem;margin-bottom:32px;">Fill in every <code style="background:#f1f5f9;padding:2px 6px;border-radius:4px;font-family:monospace;color:#6d28d9;">/* TODO */</code> in the CSS. Do not change the HTML.</p>

  <!-- Exercise 1 -->
  <section class="exercise">
    <h2>Exercise 1 — display: grid + 3 equal columns</h2>
    <p><strong>What to do:</strong> Add <code>display: grid</code> and <code>grid-template-columns</code> so items sit in 3 equal columns.</p>
    <div id="ex1-grid">
      <div class="cell c1">A</div>
      <div class="cell c2">B</div>
      <div class="cell c3">C</div>
      <div class="cell c4">D</div>
      <div class="cell c5">E</div>
      <div class="cell c6">F</div>
    </div>
  </section>

  <!-- Exercise 2 -->
  <section class="exercise">
    <h2>Exercise 2 — fr unit</h2>
    <p><strong>What to do:</strong> Make a 3-column layout where the middle column is twice as wide as the sides: <code>1fr 2fr 1fr</code>.</p>
    <div id="ex2-grid">
      <div class="cell c1">A</div>
      <div class="cell c2">B — Wide</div>
      <div class="cell c3">C</div>
    </div>
  </section>

  <!-- Exercise 3 -->
  <section class="exercise">
    <h2>Exercise 3 — repeat()</h2>
    <p><strong>What to do:</strong> Use <code>repeat()</code> to create 4 equal columns without writing <code>1fr</code> four times.</p>
    <div id="ex3-grid">
      <div class="cell c1">A</div>
      <div class="cell c2">B</div>
      <div class="cell c3">C</div>
      <div class="cell c4">D</div>
      <div class="cell c5">E</div>
      <div class="cell c6">F</div>
      <div class="cell c7">G</div>
      <div class="cell c8">H</div>
    </div>
  </section>

  <!-- Exercise 4 -->
  <section class="exercise">
    <h2>Exercise 4 — grid-template-rows</h2>
    <p><strong>What to do:</strong> Set explicit row heights: first row <code>80px</code>, second row <code>40px</code>.</p>
    <div id="ex4-grid">
      <div class="cell c1">A</div>
      <div class="cell c2">B</div>
      <div class="cell c3">C</div>
      <div class="cell c4">D</div>
      <div class="cell c5">E</div>
      <div class="cell c6">F</div>
    </div>
  </section>

  <!-- Exercise 5 -->
  <section class="exercise">
    <h2>Exercise 5 — row-gap / column-gap</h2>
    <p><strong>What to do:</strong> Set <code>row-gap: 20px</code> and <code>column-gap: 8px</code> separately.</p>
    <div id="ex5-grid">
      <div class="cell c1">A</div>
      <div class="cell c2">B</div>
      <div class="cell c3">C</div>
      <div class="cell c4">D</div>
      <div class="cell c5">E</div>
      <div class="cell c6">F</div>
    </div>
  </section>

  <!-- Exercise 6 -->
  <section class="exercise">
    <h2>Exercise 6 — grid-column: span</h2>
    <p><strong>What to do:</strong> Make item A span 2 columns wide using <code>grid-column: span 2</code>.</p>
    <div id="ex6-grid">
      <div class="cell c1" id="ex6-a">A — Wide</div>
      <div class="cell c2">B</div>
      <div class="cell c3">C</div>
      <div class="cell c4">D</div>
      <div class="cell c5">E</div>
    </div>
  </section>

  <!-- Exercise 7 -->
  <section class="exercise">
    <h2>Exercise 7 — grid-row: span</h2>
    <p><strong>What to do:</strong> Make item A span 2 rows tall using <code>grid-row: span 2</code>.</p>
    <div id="ex7-grid">
      <div class="cell c1" id="ex7-a">A — Tall</div>
      <div class="cell c2">B</div>
      <div class="cell c3">C</div>
      <div class="cell c4">D</div>
      <div class="cell c5">E</div>
    </div>
  </section>

  <!-- Exercise 8 -->
  <section class="exercise">
    <h2>Exercise 8 — grid-template-areas</h2>
    <p><strong>What to do:</strong> Name the grid areas and assign each child its correct area. Layout: header top, sidebar left, main right, footer bottom.</p>
    <div id="ex8-grid">
      <div class="cell c1" id="ex8-header">Header</div>
      <div class="cell c5" id="ex8-sidebar">Sidebar</div>
      <div class="cell c3" id="ex8-main">Main</div>
      <div class="cell c6" id="ex8-footer">Footer</div>
    </div>
  </section>

  <!-- Exercise 9 -->
  <section class="exercise">
    <h2>Exercise 9 — grid-auto-rows</h2>
    <p><strong>What to do:</strong> Set <code>grid-auto-rows: 60px</code> so every auto-generated row is 60px tall, even as more items are added.</p>
    <div id="ex9-grid">
      <div class="cell c1">A</div>
      <div class="cell c2">B</div>
      <div class="cell c3">C</div>
      <div class="cell c4">D</div>
      <div class="cell c5">E</div>
      <div class="cell c6">F</div>
      <div class="cell c7">G</div>
      <div class="cell c8">H</div>
    </div>
  </section>

  <!-- Exercise 10 -->
  <section class="exercise">
    <h2>Exercise 10 — Challenge: Magazine Layout</h2>
    <p><strong>What to do:</strong> Build this layout — A is a hero spanning all 3 columns · B C D each get 1 column · E spans 2 columns · F gets 1 column.</p>
    <div id="ex10-grid">
      <div class="cell c1" id="ex10-a">A — Hero</div>
      <div class="cell c2">B</div>
      <div class="cell c3">C</div>
      <div class="cell c4">D</div>
      <div class="cell c5" id="ex10-e">E — Featured</div>
      <div class="cell c6">F</div>
    </div>
  </section>

</body>
</html>
```

---

## Part 3 — Flex vs Grid Starter

Copy this into `flex-vs-grid-starter.html`.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Flex vs Grid Practice</title>
  <style>

    /* ── RESET ── */
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: 'Segoe UI', Arial, sans-serif;
      background: #f0f4f8;
      color: #0f172a;
      padding: 32px;
    }

    /* ── SHARED CELL STYLES ── */
    .cell {
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: 800;
      font-size: 0.85rem;
      color: #fff;
      border-radius: 7px;
      min-height: 52px;
    }
    .c1 { background: #4f46e5; }
    .c2 { background: #7c3aed; }
    .c3 { background: #0891b2; }
    .c4 { background: #059669; }
    .c5 { background: #d97706; }
    .c6 { background: #dc2626; }

    /* ── EXERCISE CONTAINER ── */
    .exercise {
      background: #fff;
      border: 1px solid #e2e8f0;
      border-radius: 12px;
      padding: 24px;
      margin-bottom: 40px;
    }
    .exercise h2 {
      font-size: 1rem;
      font-weight: 700;
      margin-bottom: 4px;
    }
    .exercise p {
      font-size: 0.85rem;
      color: #64748b;
      margin-bottom: 16px;
      line-height: 1.6;
    }
    .exercise code {
      background: #f1f5f9;
      padding: 2px 6px;
      border-radius: 4px;
      font-size: 0.8rem;
      font-family: monospace;
      color: #0f172a;
    }

    /* ── SIDE-BY-SIDE PANELS ── */
    .split {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 16px;
    }
    @media (max-width: 640px) {
      .split { grid-template-columns: 1fr; }
    }

    .panel {
      border-radius: 10px;
      overflow: hidden;
      border: 1px solid #e2e8f0;
    }
    .panel-head {
      padding: 8px 14px;
      font-size: 0.75rem;
      font-weight: 700;
      letter-spacing: 0.5px;
      text-transform: uppercase;
    }
    .panel-head.flex { background: #dcfce7; color: #14532d; }
    .panel-head.grid { background: #ede9fe; color: #4c1d95; }
    .panel-body {
      background: #f8fafc;
      padding: 14px;
    }
    .answer-note {
      margin-top: 12px;
      font-size: 0.78rem;
      color: #64748b;
      font-style: italic;
    }

    /* ══════════════════════════════════════════
       EXERCISE 1 — Basic Row of Items
       Solve the SAME problem two ways:
       left panel = Flexbox, right panel = Grid
    ══════════════════════════════════════════ */
    /* Flex solution */
    #ex1-flex {
      display: /* TODO */;
      gap: 8px;
    }
    /* Grid solution */
    #ex1-grid {
      display: /* TODO */;
      grid-template-columns: /* TODO: repeat(3, 1fr) */;
      gap: 8px;
    }

    /* ══════════════════════════════════════════
       EXERCISE 2 — Centered Single Item
       Center one box both horizontally
       and vertically inside a 160px tall parent
    ══════════════════════════════════════════ */
    /* Flex solution */
    #ex2-flex {
      display: flex;
      justify-content: /* TODO */;
      align-items: /* TODO */;
      height: 160px;
      background: #f8fafc;
      border-radius: 8px;
    }
    /* Grid solution */
    #ex2-grid {
      display: grid;
      place-items: /* TODO: center */;
      height: 160px;
      background: #f8fafc;
      border-radius: 8px;
    }

    /* ══════════════════════════════════════════
       EXERCISE 3 — Sidebar Layout
       Left sidebar 200px · right main fills rest
    ══════════════════════════════════════════ */
    /* Flex solution */
    #ex3-flex {
      display: flex;
      gap: 12px;
    }
    #ex3-flex .sidebar {
      flex-shrink: 0;
      width: /* TODO: 200px */;
    }
    #ex3-flex .main {
      flex-grow: /* TODO */;
    }
    /* Grid solution */
    #ex3-grid {
      display: grid;
      grid-template-columns: /* TODO: 200px 1fr */;
      gap: 12px;
    }

    /* ══════════════════════════════════════════
       EXERCISE 4 — 2×2 Card Grid
       4 cards, equal size, 2 columns
    ══════════════════════════════════════════ */
    /* Flex solution */
    #ex4-flex {
      display: flex;
      flex-wrap: /* TODO */;
      gap: 10px;
    }
    #ex4-flex .cell {
      width: /* TODO: calc(50% - 5px) — half minus half the gap */;
    }
    /* Grid solution */
    #ex4-grid {
      display: grid;
      grid-template-columns: /* TODO: repeat(2, 1fr) */;
      gap: 10px;
    }

    /* ══════════════════════════════════════════
       EXERCISE 5 — Holy Grail Layout
       header · (sidebar | main | aside) · footer
       Classic page layout — use Grid
    ══════════════════════════════════════════ */
    #ex5-grid {
      display: grid;
      grid-template-columns: /* TODO: 140px 1fr 140px */;
      grid-template-rows: /* TODO: 48px 1fr 40px */;
      grid-template-areas:
        /* TODO: 3 rows as strings */
        "..."
        "..."
        "...";
      gap: 10px;
      height: 260px;
    }
    #ex5-header  { grid-area: /* TODO */; }
    #ex5-sidebar { grid-area: /* TODO */; }
    #ex5-main    { grid-area: /* TODO */; }
    #ex5-aside   { grid-area: /* TODO */; }
    #ex5-footer  { grid-area: /* TODO */; }

    /* ══════════════════════════════════════════
       EXERCISE 6 — CHALLENGE: Nav + Hero + Cards
       Build a full mini-page layout:
       • Nav bar (Flexbox — logo left, links right)
       • Hero section (centered text, Flex or Grid)
       • 3-column card row (Grid)
    ══════════════════════════════════════════ */

    /* Nav */
    #ex6-nav {
      display: /* TODO */;
      align-items: /* TODO */;
      justify-content: /* TODO: space-between */;
      background: #0f172a;
      padding: 14px 24px;
      border-radius: 10px 10px 0 0;
    }
    #ex6-nav-logo { color: #fff; font-weight: 800; font-size: 1rem; }
    #ex6-nav-links { display: flex; gap: 20px; }
    #ex6-nav-links a { color: #94a3b8; text-decoration: none; font-size: 0.85rem; }

    /* Hero */
    #ex6-hero {
      display: /* TODO */;
      flex-direction: column;
      align-items: /* TODO */;
      justify-content: /* TODO */;
      background: #4f46e5;
      color: #fff;
      height: 140px;
      text-align: center;
      padding: 20px;
    }
    #ex6-hero h2 { font-size: 1.2rem; font-weight: 800; }
    #ex6-hero p  { font-size: 0.85rem; opacity: 0.8; margin-top: 6px; }

    /* Cards */
    #ex6-cards {
      display: /* TODO */;
      grid-template-columns: /* TODO: repeat(3, 1fr) */;
      gap: 12px;
      background: #f8fafc;
      padding: 16px;
      border-radius: 0 0 10px 10px;
      border: 1px solid #e2e8f0;
      border-top: none;
    }
    .card {
      background: #fff;
      border: 1px solid #e2e8f0;
      border-radius: 8px;
      padding: 16px;
    }
    .card h3 { font-size: 0.9rem; font-weight: 700; margin-bottom: 4px; }
    .card p  { font-size: 0.8rem; color: #64748b; line-height: 1.5; }

  </style>
</head>
<body>

  <h1 style="font-size:1.4rem;font-weight:800;margin-bottom:6px;">⚡▦ Flex vs Grid Practice</h1>
  <p style="color:#64748b;font-size:.88rem;margin-bottom:32px;">Each exercise solves the same layout problem two ways. Fill in both sides.</p>

  <!-- Exercise 1 -->
  <section class="exercise">
    <h2>Exercise 1 — Row of 3 Items</h2>
    <p><strong>What to do:</strong> Display A B C in a horizontal row — once using Flexbox, once using Grid.</p>
    <div class="split">
      <div class="panel">
        <div class="panel-head flex">⚡ Flexbox</div>
        <div class="panel-body">
          <div id="ex1-flex">
            <div class="cell c1">A</div>
            <div class="cell c2">B</div>
            <div class="cell c3">C</div>
          </div>
        </div>
      </div>
      <div class="panel">
        <div class="panel-head grid">▦ Grid</div>
        <div class="panel-body">
          <div id="ex1-grid">
            <div class="cell c1">A</div>
            <div class="cell c2">B</div>
            <div class="cell c3">C</div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Exercise 2 -->
  <section class="exercise">
    <h2>Exercise 2 — Perfect Center</h2>
    <p><strong>What to do:</strong> Center one item both horizontally and vertically. Flex uses <code>justify-content</code> + <code>align-items</code>. Grid uses <code>place-items</code>.</p>
    <div class="split">
      <div class="panel">
        <div class="panel-head flex">⚡ Flexbox</div>
        <div class="panel-body">
          <div id="ex2-flex">
            <div class="cell c1" style="width:80px;height:80px;">📌</div>
          </div>
        </div>
      </div>
      <div class="panel">
        <div class="panel-head grid">▦ Grid</div>
        <div class="panel-body">
          <div id="ex2-grid">
            <div class="cell c4" style="width:80px;height:80px;">📌</div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Exercise 3 -->
  <section class="exercise">
    <h2>Exercise 3 — Sidebar Layout</h2>
    <p><strong>What to do:</strong> Fixed 200px sidebar on the left, main content fills the rest. Flex uses <code>flex-grow</code>; Grid uses <code>200px 1fr</code>.</p>
    <div class="split">
      <div class="panel">
        <div class="panel-head flex">⚡ Flexbox</div>
        <div class="panel-body">
          <div id="ex3-flex">
            <div class="cell c5 sidebar" style="height:80px;">Side</div>
            <div class="cell c3 main" style="height:80px;">Main</div>
          </div>
        </div>
      </div>
      <div class="panel">
        <div class="panel-head grid">▦ Grid</div>
        <div class="panel-body">
          <div id="ex3-grid">
            <div class="cell c5" style="height:80px;">Side</div>
            <div class="cell c3" style="height:80px;">Main</div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Exercise 4 -->
  <section class="exercise">
    <h2>Exercise 4 — 2×2 Card Grid</h2>
    <p><strong>What to do:</strong> 4 equal cards in a 2-column layout. Flex uses <code>flex-wrap</code> + calculated width. Grid uses <code>repeat(2, 1fr)</code>.</p>
    <div class="split">
      <div class="panel">
        <div class="panel-head flex">⚡ Flexbox</div>
        <div class="panel-body">
          <div id="ex4-flex">
            <div class="cell c1">A</div>
            <div class="cell c2">B</div>
            <div class="cell c3">C</div>
            <div class="cell c4">D</div>
          </div>
        </div>
      </div>
      <div class="panel">
        <div class="panel-head grid">▦ Grid</div>
        <div class="panel-body">
          <div id="ex4-grid">
            <div class="cell c1">A</div>
            <div class="cell c2">B</div>
            <div class="cell c3">C</div>
            <div class="cell c4">D</div>
          </div>
        </div>
      </div>
    </div>
    <p class="answer-note">Notice: Grid version needs 3 lines of CSS. Flex version needs more math.</p>
  </section>

  <!-- Exercise 5 -->
  <section class="exercise">
    <h2>Exercise 5 — Holy Grail Layout (Grid only)</h2>
    <p><strong>What to do:</strong> Build the classic page layout using <code>grid-template-areas</code>. Header spans all 3 columns. Footer spans all 3. Middle row has sidebar · main · aside.</p>
    <div id="ex5-grid">
      <div class="cell c1" id="ex5-header">Header</div>
      <div class="cell c5" id="ex5-sidebar">Sidebar</div>
      <div class="cell c3" id="ex5-main">Main</div>
      <div class="cell c4" id="ex5-aside">Aside</div>
      <div class="cell c6" id="ex5-footer">Footer</div>
    </div>
    <p class="answer-note">Try building this same layout with Flexbox — it is much harder.</p>
  </section>

  <!-- Exercise 6 -->
  <section class="exercise">
    <h2>Exercise 6 — Challenge: Mini Page</h2>
    <p><strong>What to do:</strong> Complete the full mini-page. Use Flexbox for the nav and hero. Use Grid for the card row at the bottom.</p>
    <div>
      <nav id="ex6-nav">
        <span id="ex6-nav-logo">MyApp</span>
        <div id="ex6-nav-links">
          <a href="#">Home</a>
          <a href="#">About</a>
          <a href="#">Contact</a>
        </div>
      </nav>
      <div id="ex6-hero">
        <h2>Welcome to MyApp</h2>
        <p>Learn HTML &amp; CSS by building real things.</p>
      </div>
      <div id="ex6-cards">
        <div class="card">
          <h3>🎯 Flexbox</h3>
          <p>Great for rows and columns of content that flow naturally.</p>
        </div>
        <div class="card">
          <h3>▦ Grid</h3>
          <p>Best for two-dimensional page layouts with rows and columns.</p>
        </div>
        <div class="card">
          <h3>🔀 Combined</h3>
          <p>Use Grid for the page, Flexbox for the components inside it.</p>
        </div>
      </div>
    </div>
  </section>

</body>
</html>
```

---

## HTML Tags Used

| Tag | Where |
| ----- | ------- |
| `<!DOCTYPE html>` | Document declaration |
| `<html lang="en">` | Root element with language attribute |
| `<head>` | Document metadata |
| `<meta charset="UTF-8">` | Character encoding |
| `<meta name="viewport">` | Mobile-responsive viewport |
| `<title>` | Browser tab title |
| `<style>` | Embedded CSS |
| `<body>` | Page content |
| `<h1>` `<h2>` `<h3>` | Headings |
| `<p>` | Paragraph |
| `<div>` | Generic block container |
| `<section>` | Semantic section |
| `<nav>` | Navigation landmark |
| `<a href="#">` | Hyperlink |
| `<button>` | Interactive button |
| `<span>` | Inline element |
| `<code>` | Inline code snippet |
| `<hr>` | Horizontal rule / divider |

---

## CSS Properties Used

### Flexbox

| Property | Values practised |
| ---------- | ----------------- |
| `display` | `flex` |
| `flex-direction` | `row`, `column` |
| `justify-content` | `flex-start`, `center`, `flex-end`, `space-between`, `space-around`, `space-evenly` |
| `align-items` | `flex-start`, `center`, `flex-end`, `stretch`, `baseline` |
| `flex-wrap` | `wrap`, `nowrap` |
| `gap` | px values |
| `flex-grow` | `0`, `1` |
| `flex-shrink` | `0`, `1` |
| `align-self` | `flex-start`, `center`, `flex-end` |
| `order` | integer values |

### Grid

| Property | Values practised |
| ---------- | ----------------- |
| `display` | `grid` |
| `grid-template-columns` | `1fr`, `repeat()`, px values, mixed |
| `grid-template-rows` | px values, `1fr` |
| `gap` / `row-gap` / `column-gap` | px values |
| `grid-column` | `span N` |
| `grid-row` | `span N` |
| `grid-template-areas` | named string layout |
| `grid-area` | named area |
| `grid-auto-rows` | px values |
| `place-items` | `center` |

### General CSS

| Property | Values practised |
| ---------- | ----------------- |
| `display` | `flex`, `grid` |
| `background` | hex colours |
| `color` | hex colours |
| `font-family` | system font stack |
| `font-size` | rem, px |
| `font-weight` | `700`, `800` |
| `border-radius` | px values |
| `border` | shorthand |
| `padding` | px values |
| `margin` | `0 auto`, px values |
| `width` / `height` | px, `calc()`, `%` |
| `min-height` | px values |
| `text-decoration` | `none` |
| `opacity` | `0–1` |
| `text-transform` | `uppercase` |
| `letter-spacing` | px values |
| `cursor` | `pointer` |
| `white-space` | `nowrap` |
| `overflow` | `hidden` |
| `line-height` | unitless ratio |
| `box-sizing` | `border-box` |
| `@media` | `max-width` breakpoint |

---

## Answer Key Reference

Use the playground files to check your answers:

- **Flexbox answers** → Flexbox Playground (the live demo shows the correct result for each property)
- **Grid answers** → CSS Grid Playground
- **Flex vs Grid answers** → Flex vs Grid Playground

If your output does not match the playground demo, re-read the property description in the playground and try again before looking up the answer.

Created by Rishop Babu.
