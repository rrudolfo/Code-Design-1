Page Structure: Semantic HTML
Your landing page should use semantic HTML5 elements to create a clear, accessible structure.

Required Outer Structure
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Your Product Name</title>
  <link rel="stylesheet" href="css/styles.css">
</head>
<body>
  <header id="header">
    <!-- Navigation goes here -->
  </header>

  <main>
    <!-- All your main content sections go here -->
  </main>

  <footer>
    <!-- Footer content goes here -->
  </footer>
</body>
</html>
Inside <main>: Use Sections
Break your content into logical <section> elements:

<main>
  <section id="hero">
    <!-- Hero content -->
  </section>

  <section id="video">
    <!-- Embedded video -->
  </section>

  <section id="features">
    <!-- Feature cards using <article> elements -->
  </section>

  <section id="data">
    <!-- Product data table -->
  </section>

  <section id="contact">
    <!-- Contact form -->
  </section>
</main>
Understanding <article> vs <section>
Use <section> for:	Use <article> for:
Thematic groupings of content	Self-contained, independent content
Major page divisions	Content that could stand alone
Content with a heading	Reusable components
Example: Features section, Contact section	Example: Feature cards, testimonials
💡 Rule of Thumb
If the content could be pulled out and used somewhere else independently → use <article>

Example: Features Section with Articles
<section id="features">
  <h2>Features</h2>

  <article>
    <img src="icon1.png" alt="Feature icon">
    <h3>Feature Name</h3>
    <p>Feature description...</p>
  </article>

  <article>
    <img src="icon2.png" alt="Feature icon">
    <h3>Feature Name</h3>
    <p>Feature description...</p>
  </article>

  <article>
    <img src="icon3.png" alt="Feature icon">
    <h3>Feature Name</h3>
    <p>Feature description...</p>
  </article>
</section>
Learn more: MDN – <article> vs <section>Links to an external site.

Required Elements
Your landing page must include all of the following elements with the specified IDs and classes.

1. Header/Navigation
Requirements:

Fixed-position header (stays at top when scrolling)
Header element with id="header"
Logo/brand image with id="header-img"
Navigation element with id="nav-bar"
Minimum 3 navigation links with class="nav-link"
💡 What You Implement
How your Figma design shows the navigation.

2. Hero Section
Requirements:

H1 headline (your product's value proposition)
Subheading/supporting text
Primary call-to-action button
3. Video/Media Section
✅ Required
Embed a video related to your product.

Requirements:

Embedded video with id="video"
Can use YouTube/Vimeo <iframe> OR HTML5 <video> element
Must be responsive (scales on mobile)
Embedding a YouTube video:

<iframe
  id="video"
  width="560"
  height="315"
  src="https://www.youtube.com/embed/VIDEO_ID"
  title="Product video"
  frameborder="0"
  allowfullscreen>
</iframe>
Making video responsive:

Wrap in a container with max-width
Maintain 16:9 aspect ratio
Consider width: 100%; height: auto; for simple scaling
4. Features Section
Requirements:

Minimum 3 feature cards
Each feature uses <article> element
Each feature has: icon/image, H3 heading, description text
Layout using CSS Grid or Flexbox
5. Data Table (In-Page)
⚠️ Important
Table appears in the page (not in a modal). Modal implementation is a stretch goal.

Requirements:

Table with id="data-table"
Contains product-specific data (specs, pricing, comparisons, testimonials)
Minimum 3 columns, 4–5 rows
Proper structure with <thead>, <tbody>, <th>, and <td>
<th> elements have scope attribute
Responsive on mobile
6. Contact Form
Requirements:

Form with id="contact-form"
Name input (type="text", required)
Email input (type="email", required – HTML5 validation)
Message textarea (required)
Submit button with id="submit"
All inputs have associated <label> elements
Form has action attribute (can use placeholder URL)
7. Footer
Navigation links/sitemap
Copyright notice
Optional: social media links
CSS Requirements
1. One CSS Transform
Add visual interest with a transform effect. Examples:

transform: translateY(-4px) – Button hover lift effect
transform: scale(1.05) – Card scale on hover
transform: rotate(45deg) – Icon rotation
2. One CSS Animation
Create motion with a @keyframes animation. Examples:

Page load fade-in
Slide-up animation with stagger
Pulse animation on CTA button
Navigation link fade-in sequence
3. Responsive Design
Your page must work on multiple screen sizes:

At least one @media query (recommended: 768px breakpoint)
Mobile-first or desktop-first approach
Flexible layouts that adapt to screen size
Images and video scale appropriately
4. Form Styling
Clear :focus states
Validation state styling (:invalid, :valid)
Mobile-friendly (16px min font size to prevent iOS zoom)
Distinct hover states on buttons
5. Table Styling
Border-collapse or border styling
Differentiated header row
Mobile responsive strategy (scroll, stack, or hide columns)
Optional: zebra striping, hover states
Accessibility Requirements
Required:

All images have descriptive alt attributes
Form inputs have associated labels (explicit or implicit)
Visible focus states on all interactive elements
Semantic HTML with proper heading hierarchy (H1 → H2 → H3)


Your README must include:

Project description
Which CSS transform you implemented
Which CSS animation you implemented
Which table content type you chose
Challenges encountered and solutions
Key learnings