# AI Workflow Optimization

## Goal
Fix and refactor a broken pricing card using AI assistance.

---

## AI Prompt Used

### First Prompt
> Analyze this HTML and CSS pricing card and fix all layout and syntax bugs.  
> Explain what is broken and provide a corrected version of the code.

### AI Reply

I’ll first load the `broken-pricing.html` file to see the current markup and styles, then I’ll explain what’s broken and provide a fixed version.

#### What’s Broken

**HTML issues**

- The `h2` tag is not properly closed:  
  `<h2 class="title">Basic Plan<h2>` should end with `</h2>`.
- The HTML is all on one line. This isn’t a syntax error but makes it hard to read and maintain.

**CSS issues**

- `box-shdow` is misspelled. It should be `box-shadow`, so the card currently has no shadow.
- `margin: auto;` centers horizontally but not vertically. If vertical centering was expected, it’s missing.
- The button has no `cursor: pointer;`, so it doesn’t feel like a clickable element.

#### Corrected and Improved Version

A cleaned-up, fully working version with fixes and small layout/UX improvements was provided (kept simple with no major redesign).

---

### Second Prompt
> Refactor it into a reusable component (e.g., `Card(title, price, features)`).

### AI Reply

I’ll read `pricing-component.html` to see what you currently have, then I’ll refactor the pricing card into a reusable **Card-style component** you can use for multiple plans.

#### Idea

You can’t literally define a “component” in plain HTML, but you can get close with:

- Reusable **CSS classes** for layout and styling.
- A small **JavaScript factory function** `createCard(title, price, features)` that builds and inserts the card.

A complete `pricing-component.html` file was then created that defines this reusable component and demonstrates it with multiple plans.

---

```markdown
## Files

- `broken-pricing.html` — original broken code  
- `fixed-pricing.html` — corrected layout  
- `pricing-component.html` — reusable component version

---

## Result

- The pricing card now renders correctly.
- The layout and syntax bugs are fixed.
- The card can now be reused as a component for multiple pricing plans.