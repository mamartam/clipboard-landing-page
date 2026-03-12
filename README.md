# Clipboard landing page

This project was created based on a Frontend Mentor [https://www.frontendmentor.io/] challenge. The layout and design idea come from Frontend Mentor, while the code implementation is my own.

## 📦 About the project
<details>
  <summary><b>index.html</b></summary> 
   
  - Semantic Architecture
    
    I used HTML5 semantic tags. This improves both SEO and accessibility:
    
      - `<header>`: Contains the main hero section and primary call-to-action.
      - `<main>`: Wraps the core content to tell search engines where the unique information lives.
      - `<section>`: Each part of the page (Track, Access, Supercharge) is clearly defined as a separate logical block.
      - `<footer>`: Properly encapsulates the site navigation and social connections.
      

  - BEM Methodology (Block, Element, Modifier)
    
    The naming convention throughout the HTML follows the BEM methodology (e.g., `supercharge__box`, `footer__nav-list`).

     - Advantage: This makes the relationship between the HTML and SCSS transparent and prevents style leaking.
     - Scalability: It allows the code to be easily extended without breaking existing layouts.
    
  - Strategic Class Tagging for Spacing
    
    I implemented utility classes like `space__p-t` and `space__p-lr` for global spacing management. This approach allows for consistent padding and margins across different sections while keeping the main structural classes focused only on layout logic.
    
</details>

<details>
<summary><b>main.scss</b></summary> 
  
  For the styling of this project, I implemented a modular and scalable `SCSS` architecture.

  - Moduls

    I organized my styles into logical partials using the `@use` and `@import` rules. This keeps the main file clean and ensures a clear separation of concerns:

     - `_variables.scss`: Centralized storage for the brand's color palette, typography scales, and spacing constants.
     - `_mixins.scss`: Contains reusable logic, specifically for responsive design.
     - `_resets.scss` & `_helpers.scss`: Global resets and utility classes for consistent spacing across the project.
   
  - Advanced Responsive Design with Mixins
    
    Instead of cluttering the main logic with repetitive media queries, I used a custom mixin system (`@include` larger-screens).
    
     - Mobile-First Approach: Styles are written for mobile devices by default, with enhancements for tablet and desktop added via mixins.
     - Maintainability: Breakpoints are tied to variables (e.g., `$small-screen`, `$large-screen`), making it easy to adjust the layout site-wide by changing a single value.
  
  - BEM Implementation in SCSS
    
    I leveraged SCSS nesting and the ampersand (`&`) operator to perfectly mirror the BEM (Block Element Modifier) structure of my HTML.

     - This creates a visual hierarchy in the code that is easy to follow.
     - It ensures that styles for elements (like `&__logo` or `&__buttons-container`) are strictly scoped to their parent block, preventing CSS "leakage" and naming conflicts.
    
  - Efficient Layout Techniques

    - Flexbox & Grid Integration: I used Flexbox for alignment (like the button containers and social links) and CSS Grid for the complex footer navigation.
    - Dynamic Layout Shifts: In the footer, I used `grid-auto-flow: column` to transform a simple list into a sophisticated multi-column grid on desktop screens, optimizing the use of horizontal space.
    - Negative Margins for Visual Impact: For the "Track" section, I used strategic negative margins to allow the computer mockup to bleed off the edge of the screen, staying true to the original design layout.
  
</details>

## 🚀 How It Can Be Improved?
While the current version of the project is fully functional and follows best practices, there are several areas for future enhancement:

1. Dark Mode Support
Since the project uses a centralized SCSS variable system, implementing a Dark Mode would be a seamless next step. By using CSS Custom Properties (Variables) alongside SCSS variables, I could toggle the theme based on the user's system preferences.

4. Animation Enhancements
While the current version uses smooth transitions, I could incorporate AOS (Animate On Scroll) or Intersection Observer API to trigger subtle fade-in effects as the user scrolls through the different feature sections (Track, Access, Supercharge).

## 🍿 Video
[...](https://github.com/user-attachments/assets/896b9b50-5577-4ccf-a41e-686f778f97f8)
