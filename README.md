# accessibility-by-default

AI skill that makes accessibility a non-negotiable baseline in web development.

---

## What This Does

Changes how AI agents approach web development by treating accessibility as a default requirement, not an afterthought.

When this skill is active, the agent:
- Writes accessible markup from the start
- Rejects common inaccessible patterns
- Prioritizes semantic HTML and native browser behavior
- Designs for keyboard, screen readers, and assistive technology
- Reviews code for accessibility gaps before considering work complete

This is not a linting tool. This changes decision-making.

---

## Why This Matters

Most web accessibility issues come from decisions made early — choosing a `<div>` instead of a `<button>`, forgetting labels on inputs, building modals that trap keyboard users.

These aren't complex problems. They're defaults.

This skill embeds accessibility knowledge directly into the agent's workflow so the right choice becomes the obvious choice.

---

## When to Use

Use this skill when working on:
- Web pages and web applications
- UI component libraries
- Forms, navigation, interactive widgets
- Design systems
- Frontend refactors
- Accessibility audits

Use it if you want code that works for:
- Keyboard users
- Screen reader users
- People with low vision
- People with cognitive differences
- People on slow connections or old devices
- People who've disabled animations

---

## When NOT to Use

This skill does not:
- Generate WCAG compliance reports or certifications
- Test accessibility automatically (you still need tools like axe, Lighthouse, manual testing)
- Cover mobile app accessibility (iOS/Android native)
- Replace human accessibility auditors
- Guarantee legal compliance
- Handle niche ARIA widgets without clear guidance

This is a development skill, not a compliance audit.

---

## What This Intentionally Does NOT Cover

- **WCAG AAA requirements** — Focuses on AA, which covers most practical needs
- **Legal compliance** — Compliance is contextual; this provides technical guidance, not legal advice
- **PDF accessibility** — Out of scope
- **Native mobile apps** — Focuses on web (HTML/CSS/JS)
- **Automated testing setup** — You still need axe-core, pa11y, or similar
- **Disability simulation** — Real users are not simulations; this teaches patterns, not empathy theater

---

## How It Works

The skill defines:
1. **Core principles** — Semantic HTML, keyboard navigation, screen reader compatibility
2. **Mandatory checks** — Structure, forms, focus, contrast, motion, ARIA
3. **Development rules** — Practical code patterns for accessible implementations
4. **Anti-patterns** — Explicit list of patterns to reject (div buttons, placeholder-only forms, etc.)
5. **Review workflow** — Step-by-step accessibility evaluation process

The agent applies these principles automatically. You don't need to prompt for accessibility — it's embedded.

---

## Philosophy

Accessibility is not a feature. It's part of doing the job correctly.

You wouldn't ship a button that doesn't click. You wouldn't ship a form that doesn't submit. Accessibility is the same category of requirement.

This skill makes that the default.

---

## Practical Impact

**Before:**
```html
<div class="button" onclick="handleSubmit()">Submit</div>
```

**After:**
```html
<button type="button" onclick="handleSubmit()">Submit</button>
```

**Before:**
```html
<input type="email" placeholder="Your email">
```

**After:**
```html
<label for="email">Your email</label>
<input type="email" id="email" name="email">
```

**Before:**
```css
.box {
  animation: bounce 1s infinite;
}
```

**After:**
```css
@media (prefers-reduced-motion: no-preference) {
  .box {
    animation: bounce 1s infinite;
  }
}
```

Small changes. Significant impact.

---

## Installation

Compatible with [skills.sh](https://skills.sh).

```bash
skills add accessibility-by-default
```

Or manually reference `skill.md` in your agent's skill list.

---

## Maintenance

This skill reflects WCAG 2.1 / 2.2 Level AA guidance and common frontend accessibility patterns as of 2026.

Web standards evolve. This skill should be updated when:
- WCAG releases major updates
- Browser support for accessibility features shifts significantly
- New anti-patterns emerge in common frameworks

---

## Credits

Created by Noé Júnior.

Built on public accessibility knowledge from W3C, WebAIM, The A11Y Project, and years of collective frontend work.

---

## License

Use freely. Accessibility knowledge is not proprietary.
