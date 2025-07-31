# 📄 Accessibility Build & Break – Sweet Delights Bakery

**Assignment 3: Build & Break – Mini Accessible Page**  
Objective: Learn by building a fully accessible page and then intentionally breaking it with accessibility violations.

## ✅ Project Overview
This project demonstrates a simple product/landing page for Sweet Delights Bakery.  
Two versions were created:

- **Accessible Version** → Follows WCAG 2.1 guidelines.
- **Broken Version** → Contains intentional accessibility violations for testing with WAVE and Lighthouse.

## ⚠️ Accessibility Violations Introduced

| #  | Violation                  | Description                                                                 | Impact on Users                                      | WCAG Reference                          | Fix                                        |
|----|----------------------------|-----------------------------------------------------------------------------|------------------------------------------------------|-----------------------------------------|--------------------------------------------|
| 1  | Missing Alt Text           | Logo image has no alt attribute.                                            | Screen readers cannot describe the logo              | 1.1.1 Non-text Content (Level A)        | Add `alt="Sweet Delights Bakery Logo"`     |
| 2  | Empty Link                 | `<a href="#"></a>` with no label.                                           | Screen reader announces "link" without context       | 2.4.4 Link Purpose (Level A)            | Provide meaningful text or remove empty link |
| 3  | Poor Color Contrast        | Heading text #cccccc on white.                                              | Low vision users struggle to read                    | 1.4.3 Contrast (Minimum) (Level AA)     | Use darker color (e.g., #333333)           |
| 4  | Wrong ARIA Role            | Button uses `role="checkbox"`.                                              | Screen reader announces as checkbox instead of link  | 4.1.2 Name, Role, Value (Level A)       | Remove incorrect role; use semantic `<a>`  |
| 5  | Skipped Heading Levels     | `<h4>` directly after `<h2>`.                                               | Navigation disrupted                                 | 1.3.1 Info & Relationships (Level A)    | Change `<h4>` → `<h3>`                     |
| 6  | Redundant Alt Text         | Image alt = "Artisan Sourdough" same as visible heading.                    | Screen readers repeat information                    | 1.1.1 Non-text Content (Level A)        | Use empty `alt=""`                         |
| 7  | Missing Title on Iframe    | Embedded Google Map has no title.                                           | Screen readers only announce "iframe"               | 4.1.2 Name, Role, Value (Level A)       | Add `title="Map to Sweet Delights Bakery"` |
| 8  | Social Icons Without Alt   | Social media logos lack alt.                                                | Users don't know which platform each link is for     | 1.1.1 Non-text Content (Level A)        | Add descriptive alt like `alt="Facebook"`  |

## 🛠️ Tools Used
- **WAVE Accessibility Tool** → Detected missing alt, empty links, skipped headings.
- **Lighthouse Audit (Chrome DevTools)** → Flagged poor contrast and ARIA misuse.

## 📌 Summary
The accessible version of the page meets WCAG guidelines and is usable by keyboard-only and screen reader users.

The broken version demonstrates common accessibility pitfalls:
- Images without alt
- Poor color contrast
- Incorrect ARIA roles
- Redundant text for screen readers
- Missing iframe titles
- Inconsistent heading structure

Fixing these issues ensures inclusivity and a better user experience for all users.

## 🚀 Deliverables
1. Accessible Version Code
2. Broken Version Code
3. This documentation (README.md)
