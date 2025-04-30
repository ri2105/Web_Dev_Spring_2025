
# Ridwan Islam Personal Portfolio Website 

## Project Overview

This project is a responsive, interactive website built using **Bootstrap**, **CSS**, and **JavaScript**. The goal was to create a unique design and functionality while leveraging Bootstrap’s responsive grid system—without relying heavily on media queries.

---

## Documentation of My Process

1. **Planning and Wireframing**  
   I began by sketching the basic layout of the site and defining the core sections (navbar, profile, about, project, contact). 

2. **Bootstrap Integration**  
   I used Bootstrap's CDN to quickly scaffold the page with built-in responsiveness and component structure. Bootstrap's grid system (`container`, `row`, `col`) helped me maintain layout consistency across screen sizes.

3. **Customization**  
   To avoid the default “Bootstrap look,” I customized its appearance by:
   - Overriding Bootstrap variables and styles in my own CSS.
   - Tweaking button shapes, shadows, and transitions.
   - Modifying components like navbar and cards to have a unique aesthetic.

4. **Interactivity**  
   I implemented interactivity using JavaScript and jQuery, such as:
   - Theme toggle (light/dark mode) with persistent user preference.
   - Smooth scrolling behavior.
   - Collapsing mobile navbar after clicking a link.

5. **Testing & Responsiveness**  
   I tested the site across various screen sizes and browsers using Chrome DevTools and adjusted spacing, margins, and component behavior accordingly.

---

## Interesting Code Snippets

### Dark Mode Toggle with `localStorage`
This feature allows users to switch themes and remembers their preference across sessions:

```js
const toggle = document.querySelector('#theme-toggle');
const body = document.body;

toggle.addEventListener('click', () => {
  body.classList.toggle('dark-mode');
  localStorage.setItem('theme', body.classList.contains('dark-mode') ? 'dark' : 'light');
});

window.addEventListener('DOMContentLoaded', () => {
  if (localStorage.getItem('theme') === 'dark') {
    body.classList.add('dark-mode');
  }
});
```

### Auto-Collapse Mobile Navbar
Improves UX by collapsing the navbar after a link is clicked in mobile view:

```js
document.querySelectorAll('.nav-link').forEach(link => {
  link.addEventListener('click', () => {
    const navCollapse = document.querySelector('.navbar-collapse');
    if (navCollapse.classList.contains('show')) {
      new bootstrap.Collapse(navCollapse).hide();
    }
  });
});
```

---

## Issues Encountered

- **Navbar not auto-collapsing in mobile view**: Resolved with custom JavaScript tied to Bootstrap's Collapse component.
- **Overriding Bootstrap CSS**: Required inspecting deeply nested class rules and being cautious about specificity to avoid breaking responsiveness.
- **Form handling**: Initially considered building a back-end but instead used Formspree for quick form submission without server code.

---

## What I Learned

- Advanced use of **Bootstrap's grid system** and utility classes to avoid manual media queries.
- How to deeply **customize Bootstrap’s visual design** without breaking its core structure.
- Building user-focused features like **theme toggling**, **smooth navigation**, and **mobile-first behaviors**.
- Integration of **external JavaScript libraries**  alongside Bootstrap’s JavaScript utilities.

---

## Next Steps

If I had more time and tools, I would:
- **Add animations and transitions** with libraries like GSAP for a more dynamic experience.
- **Improve accessibility (a11y)** by adding ARIA labels, focus management, and testing with screen readers.
- **SEO Optimization** and analytics tracking for real-world deployment.

---