Overview：
A small, static mock of Penn’s “Search Classes” page built with plain HTML/CSS. It demonstrates a consistent header, a red title bar, a centered content column, and three content blocks: Search form, Suggestions, and Carts. The layout emphasizes simple, readable structure and accessibility-friendly labels.

What’s inside：
File structure：
index.html — Markup for the top bar (logo + welcome), red title bar, and the three sections.
styles.css — All styling for the layout, spacing, buttons, headings, and checkboxes. It defines the centered column via .container, the white cards via .card, and the navy buttons via .primary-btn.

Key layout ideas：
Centered page width via .container with max-width: 980px; margin: 0 auto; padding: 0 16px;. This keeps all content aligned under the red title bar while remaining responsive.
White “cards” for each block using .card { background:#fff; border-radius:6px; padding:8px 16px; margin:8px 0; } for clean separation from the gray page background. 
Section headers outside cards: the SUGGESTIONS and CARTS titles are headings placed above their respective cards so the labels sit on the light gray background rather than inside the white card. The heading look/spacing is controlled by .section-header (uppercase, small bold, tight margins).
Responsive title size using a tiny media query to bump the hero title on wider screens. 

Form and controls：
Inputs/selects share consistent size/spacing with the shared rule input[type="text"], select { height: 40px; padding: 10px 12px; margin: 10px 0; }.
The navy call-to-action buttons use .primary-btn (full width, bold, rounded). 
The red “Search Classes” bar is .title-bar, and the top navigation is .top-bar with a left‐aligned logo and right‐aligned “Welcome, Ruijia.”

Where I used AI (and why)：
I used AI to resolve alignment and layout issues after multiple revisions. I reviewed and understood the generated code and integrated it into the project.
1. Aligning checkboxes and text perfectly
I asked AI for a robust pattern to align a checkbox with multi-line label text. The suggestion was to wrap each pair in a <label class="checkbox">…</label> and use Flexbox to align and space them:
label.checkbox { display: flex; align-items: center; gap: 8px; margin: 8px 0; line-height: 1.4; font-size: 13px; }
label.checkbox input[type="checkbox"] { width: 18px; height: 18px; margin: 0; }
This solved vertical misalignment and kept spacing consistent across browsers.

2. Placing section headers outside the cards with tight spacing  
Visually, the SUGGESTIONS and CARTS labels should sit on the gray background above each white card. I asked AI for a minimal, semantic way to do this without extra wrappers. The solution: keep as a sibling before each card and tune margins in CSS:
.section-header {
  font-size: 14px;
  font-weight: 800;
  text-transform: uppercase;
  margin: 2px 0;
  color: #011f5b;
}
That produced the desired look and alignment with small CSS.

Customizing：
- Change the logo: replace `assets/upenn-logo.png`.
- Adjust width: modify `.container { max-width: … }`.
- Control spacing: adjust the margin/padding of `.card` or `.section-header`.

Summary：
Code authored by me (HTML/CSS).
AI assistance was used specifically for:
Checkbox/text alignment with a flex-based label wrapper.
Structure and spacing for section headers outside the cards.
I reviewed, understood, and adapted the AI-suggested snippets before integrating them.
