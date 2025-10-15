# Design Notes

Although the site structure is simple, it is designed to simulate a filing cabinet with multiple drawers and documents inside. Each document represents a section of the portfolio. The goal is to blend creative visual storytelling with the usability of a standard portfolio, while keeping the implementation strictly within HTML and CSS — without JavaScript.

## General Structure — Interaction with drawers and documents

This section explores different approaches to how the content inside the filing cabinet is presented and revealed to the user. Initially, I came up with three different ideas:


### 1. Full Scroll-Based Animation

**Idea.**  
Use a continuous scroll animation that opens drawers and reveals documents as the user scrolls down the page.

**Pros.**
- Highly immersive and visually appealing.
- Strong sense of storytelling.

**Cons.**
- Navigating to a deep section via anchor link (e.g., from the main navigation) would require scrolling through the entire animation.
- The alternative is to eliminate the main navigation, which leads to poor UX for users seeking quick access to content.

**Conclusion.** 
Visually strong, but not practical for structured navigation or recruiter-friendly usage.

---

### 2. Two-Level Navigation

**Idea.**  
Use the scroll animation to navigate between drawers, and include a secondary navigation within each drawer to access individual documents.

**Pros.**
- More closely mimics the interaction of a physical filing cabinet.
- Allows compartmentalized access to documents.

**Cons.**
- Overcomplicates the interface for a portfolio site.
- Reduces usability due to added navigation layers.

**Conclusion.**
Too heavy for the project’s scope and potentially confusing for users.

---

### 3. Controlled Details-Based Content Reveal (Final Choice ✅)

**Idea.**  
Use the scroll animation to navigate between drawers, and represent documents using the native `<details>` and `<summary>` HTML elements.

**Pros.**
- Semantic, accessible, and fully functional without JavaScript.
- Can be styled as clickable buttons inside each drawer.
- When navigating to a specific document via an anchor link, it opens automatically (a native feature of the `<details>` element).  
- Ensures only one document is open at a time (another native behavior of `<details>`).
- Cleanly separates visual storytelling (scroll animation) from content interaction (toggleable details).
- Maintains a recruiter-friendly navigation structure with just one navbar.

**Cons.**
- Slightly unconventional use of `<details>`, but acceptable when styled carefully.
- Requires custom styling to override native browser quirks.

**Conclusion.**
Best balance between creativity, usability, and technical feasibility. Offers full interaction without JavaScript, while maintaining content accessibility. When navigating via anchor link,
the target drawer opens (through scroll animation) and the corresponding document auto-expands while others collapse.

---

## Navigation Design — Access to content

This section considers how users should move between documents (sections of the portfolio), especially on different screen sizes. The design decision needed to align both with aesthetic goals and with best practices in usability and responsiveness.


### 1. Post-It Based Navigation (Final Choice ✅)

**Idea.**
Replace conventional menus with visible, stylized navigation elements resembling sticky notes (“post-its”), fixed on the screen. These act as persistent links to the main sections of the portfolio: Home, About Me, Skills, Projects, and Contact. 

This approach emerged as a response to a practical concern: uncertainty over whether documents inside drawers could be styled as clearly clickable elements (e.g., buttons or tabs within each drawer). If that were not possible, users would rely solely on the main navigation to move between sections, making it unacceptable to hide it behind a hamburger menu, which is very common on mobile. A horizontal top navbar was also rejected for mobile due to visual constraints. Post-its became the most fitting and cohesive solution, and were then adopted for all screen sizes to preserve consistency.

**Pros.**
- Visually coherent with the filing cabinet metaphor.
- Avoids common mobile UI patterns like hidden hamburger menus.
- Ensures immediate access to all sections on all screen sizes.
- Distinctive and memorable; reinforces the project's creative identity.
- Allows semantic, anchor-based navigation.
- Solves a potential UX issue when document-level interaction inside drawers is limited or not visually obvious.

**Cons.**
- Risk of visual clutter if not carefully designed, especially on smaller screens.
- May not be instantly recognized as navigation by all users unfamiliar with the metaphor.
- Slightly unconventional compared to expected UI norms in professional portfolios.
- If it becomes possible to add intuitive, styled buttons inside each drawer to extract documents, then conventional navigation (e.g., top nav) might provide a cleaner and more minimal interface.

**Conclusion.**
The post-it navigation pattern offers a strong balance between creativity, usability, and thematic consistency. It emerged not only as a stylistic choice, but also as a solution to the functional challenge of ensuring clear access to all sections. In scenarios where drawer content is not navigable on its own, visible navigation becomes essential, making post-its preferable to hidden menus. If in the future internal navigation within drawers is successfully implemented (e.g., with folder-like tabs that are easily recognised as buttons), traditional navbars may be reconsidered to improve visual simplicity.