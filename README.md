# Melbourne AI Automation Landing Page - Maintenance & Customization Guide

Welcome! This comprehensive guide will help you maintain, update, and customize your Melbourne AI Automation landing page. Whether you're new to HTML and CSS or looking for specific guidance, you'll find detailed, step-by-step instructions for all common tasks.

---

## Table of Contents

1. [Overview of Your Landing Page](#overview-of-your-landing-page)
2. [Updating Text Content](#updating-text-content)
3. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
4. [Fixing and Updating Links](#fixing-and-updating-links)
5. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
6. [Common Customization Tasks](#common-customization-tasks)
7. [Troubleshooting Guide](#troubleshooting-guide)
8. [Best Practices](#best-practices)

---

## Overview of Your Landing Page

Your landing page is built with:

- **HTML5**: The structure and content
- **Tailwind CSS**: A utility-first CSS framework for styling (loaded from CDN)
- **Inter Font**: A modern, professional typeface from Google Fonts
- **Vanilla JavaScript**: For interactive features like accordions and smooth scrolling

### Page Sections

Your landing page contains these main sections:

| Section | ID/Location | Purpose |
|---------|-------------|---------|
| Navigation Header | `<header>` | Sticky navigation with logo and menu |
| Hero Section | After header | Main headline and call-to-action |
| Features Section | `id="features"` | Three core features with icons |
| Benefits Section | `id="benefits"` | Three benefits with gradient icons |
| CTA Section | Background image overlay | Call-to-action with background |
| About Us Section | After CTA | Company information and mission |
| Testimonials Section | `id="testimonials"` | Four customer testimonials |
| FAQ Section | `id="faq"` | Five expandable FAQ items |
| Footer | `<footer>` | Links, contact info, and social media |

---

## Updating Text Content

### What is Text Content?

Text content is the visible words and sentences on your website. Unlike code, you can safely edit text without worrying about breaking functionality.

### Finding Text to Edit

All text content is located between HTML tags. Here's what to look for:

```html
<h1>This is a heading</h1>
<p>This is a paragraph</p>
<span>This is inline text</span>
```

### Section-by-Section Text Updates

#### 1. **Header/Navigation Text**

**Location**: Lines 47-50 in the `<header>` section

**Current Code**:
```html
<span class="font-bold text-xl text-gray-900 hidden sm:inline">Melbourne AI</span>
```

**To Change**: Replace `Melbourne AI` with your company name

**Example**:
```html
<span class="font-bold text-xl text-gray-900 hidden sm:inline">Your Company Name</span>
```

**What the classes mean**:
- `font-bold` = Makes text bold
- `text-xl` = Makes text extra large
- `text-gray-900` = Makes text dark gray/black
- `hidden sm:inline` = Hides on mobile, shows on small screens and up

---

#### 2. **Navigation Menu Links**

**Location**: Lines 52-57

**Current Code**:
```html
<a href="#features" class="text-gray-700 font-medium hover:text-blue-600 smooth-transition">Features</a>
<a href="#benefits" class="text-gray-700 font-medium hover:text-blue-600 smooth-transition">Benefits</a>
<a href="#faq" class="text-gray-700 font-medium hover:text-blue-600 smooth-transition">FAQ</a>
<a href="#testimonials" class="text-gray-700 font-medium hover:text-blue-600 smooth-transition">Testimonials</a>
```

**To Change Menu Text**: Replace the text between the `>` and `</a>` tags

**Example** (to add a new menu item):
```html
<a href="#pricing" class="text-gray-700 font-medium hover:text-blue-600 smooth-transition">Pricing</a>
```

**What the classes mean**:
- `text-gray-700` = Gray text color
- `font-medium` = Medium font weight (between normal and bold)
- `hover:text-blue-600` = Text turns blue when you hover over it
- `smooth-transition` = Changes color smoothly (not instantly)

---

#### 3. **Hero Section (Main Headline)**

**Location**: Lines 73-87

**Current Code**:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight tracking-tight mb-6">
    Melbourne AI Automation
</h1>
<p class="text-xl md:text-2xl text-gray-700 font-light leading-relaxed mb-8">
    AI Automation For Small Business
</p>
<p class="text-lg text-gray-600 leading-relaxed mb-10 max-w-2xl mx-auto">
    Transform your small business with intelligent automation solutions. Reduce manual tasks, increase productivity, and scale your operations without breaking the bank.
</p>
```

**To Change**:

1. Replace `Melbourne AI Automation` with your headline
2. Replace `AI Automation For Small Business` with your subtitle
3. Replace the longer paragraph with your description

**Example**:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight tracking-tight mb-6">
    Your Company Name
</h1>
<p class="text-xl md:text-2xl text-gray-700 font-light leading-relaxed mb-8">
    Your Tagline Here
</p>
<p class="text-lg text-gray-600 leading-relaxed mb-10 max-w-2xl mx-auto">
    Your description paragraph goes here. Keep it concise and focused on the main benefit to your customer.
</p>
```

**What the responsive classes mean**:
- `text-4xl` = Size on mobile
- `md:text-5xl` = Size on medium screens (tablets)
- `lg:text-6xl` = Size on large screens (desktops)
- `leading-tight` = Tight line spacing
- `tracking-tight` = Tight letter spacing
- `mb-6` = Margin (space) below the element

---

#### 4. **Feature Cards Text**

**Location**: Lines 107-160 (Features Section)

**Current Code Example** (Feature 1):
```html
<h3 class="text-xl font-bold text-gray-900 mb-3">Low Cost</h3>
<p class="text-gray-600 leading-relaxed mb-4">
    Enterprise-grade automation without the enterprise price tag...
</p>
<ul class="space-y-2 text-sm text-gray-600">
    <li class="flex items-start">
        <span class="text-blue-600 mr-3 font-bold">✓</span>
        <span>Transparent, predictable pricing</span>
    </li>
```

**To Change**:

1. Replace feature title (e.g., `Low Cost`)
2. Replace feature description
3. Update bullet points by replacing text after `<span>`

**Example**:
```html
<h3 class="text-xl font-bold text-gray-900 mb-3">Your Feature Name</h3>
<p class="text-gray-600 leading-relaxed mb-4">
    Your feature description goes here. Explain what this feature does and why it matters.
</p>
<ul class="space-y-2 text-sm text-gray-600">
    <li class="flex items-start">
        <span class="text-blue-600 mr-3 font-bold">✓</span>
        <span>Your first benefit</span>
    </li>
    <li class="flex items-start">
        <span class="text-blue-600 mr-3 font-bold">✓</span>
        <span>Your second benefit</span>
    </li>
</ul>
```

---

#### 5. **Benefits Section Text**

**Location**: Lines 173-230 (Benefits Section)

Similar to Features, you'll find:
- Section heading (line 174)
- Benefit titles (lines 189, 206, 223)
- Benefit descriptions (lines 191-193, 208-210, 225-227)
- Metric text at bottom (lines 198, 215, 232)

**To Change** (Example for first benefit):
```html
<h3 class="text-xl font-bold text-gray-900 mb-3">Your Benefit Name</h3>
<p class="text-gray-600 leading-relaxed">
    Your benefit description explaining the value proposition.
</p>
<div class="mt-6 pt-6 border-t border-gray-200">
    <p class="text-sm text-green-600 font-semibold">Your metric or stat here</p>
</div>
```

---

#### 6. **CTA (Call-to-Action) Section Text**

**Location**: Lines 239-250

**Current Code**:
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-white tracking-tight mb-6">
    Ready to Transform Your Business?
</h2>
<p class="text-lg md:text-xl text-gray-100 leading-relaxed mb-10 max-w-2xl mx-auto">
    Join small businesses across Melbourne who are already automating their workflows and saving countless hours every week.
</p>
```

**To Change**:
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-white tracking-tight mb-6">
    Your CTA Headline
</h2>
<p class="text-lg md:text-xl text-gray-100 leading-relaxed mb-10 max-w-2xl mx-auto">
    Your persuasive paragraph encouraging action.
</p>
```

---

#### 7. **About Us Section Text**

**Location**: Lines 257-279

**Current Code**:
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 tracking-tight mb-12 text-center">
    About Melbourne AI Automation
</h2>

<div class="space-y-8">
    <p class="text-lg text-gray-700 leading-relaxed">
        Melbourne AI Automation was founded in 2023...
    </p>
    
    <p class="text-lg text-gray-700 leading-relaxed">
        We believe that every business...
    </p>
</div>
```

**To Change**:
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 tracking-tight mb-12 text-center">
    About Your Company
</h2>

<div class="space-y-8">
    <p class="text-lg text-gray-700 leading-relaxed">
        Your first paragraph about your company's founding and mission.
    </p>
    
    <p class="text-lg text-gray-700 leading-relaxed">
        Your second paragraph about your values and approach.
    </p>
</div>
```

---

#### 8. **Testimonials Text**

**Location**: Lines 308-375 (Testimonials Section)

**Current Code Example** (First testimonial):
```html
<p class="text-gray-700 leading-relaxed mb-6">
    "Melbourne AI Automation has completely transformed how we manage customer orders..."
</p>
<div class="pt-6 border-t border-gray-200">
    <p class="font-semibold text-gray-900">Sarah Mitchell</p>
    <p class="text-sm text-gray-600">Owner, Mitchell's E-commerce Store</p>
</div>
```

**To Change**:
```html
<p class="text-gray-700 leading-relaxed mb-6">
    "Your customer testimonial goes here. Make it specific and include measurable results."
</p>
<div class="pt-6 border-t border-gray-200">
    <p class="font-semibold text-gray-900">Customer Name</p>
    <p class="text-sm text-gray-600">Job Title, Company Name</p>
</div>
```

---

#### 9. **FAQ Text**

**Location**: Lines 388-450 (FAQ Section)

**Current Code Example** (First FAQ):
```html
<button class="faq-toggle w-full px-6 py-4 text-left font-semibold text-gray-900 bg-gray-50 hover:bg-gray-100 smooth-transition flex items-center justify-between" onclick="toggleAccordion(this)">
    <span>What is Melbourne AI Automation and how does it work?</span>
    <svg>...</svg>
</button>
<div class="accordion-content bg-white">
    <div class="px-6 py-4 text-gray-700 leading-relaxed">
        <p>Melbourne AI Automation is a comprehensive automation platform...</p>
    </div>
</div>
```

**To Change**:
```html
<button class="faq-toggle w-full px-6 py-4 text-left font-semibold text-gray-900 bg-gray-50 hover:bg-gray-100 smooth-transition flex items-center justify-between" onclick="toggleAccordion(this)">
    <span>Your FAQ Question?</span>
    <svg>...</svg>
</button>
<div class="accordion-content bg-white">
    <div class="px-6 py-4 text-gray-700 leading-relaxed">
        <p>Your answer to the FAQ question goes here.</p>
    </div>
</div>
```

---

#### 10. **Footer Text**

**Location**: Lines 457-530

**Company Info** (Lines 462-468):
```html
<span class="font-bold text-lg text-white">Melbourne AI</span>
<p class="text-gray-400 text-sm leading-relaxed">
    Transforming small businesses through intelligent automation solutions.
</p>
```

**To Change**:
```html
<span class="font-bold text-lg text-white">Your Company Name</span>
<p class="text-gray-400 text-sm leading-relaxed">
    Your company tagline or brief description.
</p>
```

**Footer Links** (Lines 471-532):

Each section has links you can update:
```html
<li><a href="#features" class="text-gray-400 hover:text-blue-400 smooth-transition">Features</a></li>
```

**Contact Info** (Lines 513-520):
```html
<p class="text-gray-400 text-sm mb-2">
    Email: <a href="mailto:admin@mai.com" class="text-blue-400 hover:text-blue-300 smooth-transition">admin@mai.com</a>
</p>
<p class="text-gray-400 text-sm">
    Melbourne, Victoria, Australia
</p>
```

**To Change**:
```html
<p class="text-gray-400 text-sm mb-2">
    Email: <a href="mailto:your-email@yourcompany.com" class="text-blue-400 hover:text-blue-300 smooth-transition">your-email@yourcompany.com</a>
</p>
<p class="text-gray-400 text-sm">
    Your City, Your State, Your Country
</p>
```

**Copyright Text** (Lines 530-533):
```html
<p class="text-gray-400 text-sm mb-4 md:mb-0">
    &copy; 2025 Melbourne AI Automation. All rights reserved.
</p>
```

**To Change**:
```html
<p class="text-gray-400 text-sm mb-4 md:mb-0">
    &copy; 2025 Your Company Name. All rights reserved.
</p>
```

---

### Text Update Best Practices

✅ **Do**:
- Keep text concise and scannable
- Use action verbs (Transform, Streamline, Automate)
- Include specific numbers and metrics when possible
- Maintain consistent tone throughout
- Test readability on mobile devices

❌ **Don't**:
- Change anything inside HTML tags (like `class="..."`)
- Delete opening or closing tags
- Use special characters that might break the code
- Make paragraphs too long (keep under 3 sentences)

---

## Modifying Tailwind CSS Classes

### What is Tailwind CSS?

Tailwind CSS is a "utility-first" framework that uses pre-made classes to style elements. Instead of writing custom CSS, you apply classes directly to HTML elements.

### Understanding Tailwind Classes

Here's a breakdown of common Tailwind classes used in your landing page:

| Class | What It Does | Example |
|-------|-------------|---------|
| `text-{size}` | Sets text size | `text-sm`, `text-lg`, `text-4xl` |
| `text-{color}-{shade}` | Sets text color | `text-blue-600`, `text-gray-700` |
| `bg-{color}-{shade}` | Sets background color | `bg-blue-600`, `bg-gray-50` |
| `p-{number}` | Sets padding (space inside) | `p-4`, `p-8` |
| `m-{number}` | Sets margin (space outside) | `m-4`, `mb-6` (margin-bottom) |
| `w-{number}` | Sets width | `w-10`, `w-full` |
| `h-{number}` | Sets height | `h-10`, `h-screen` |
| `rounded-{size}` | Rounds corners | `rounded-lg`, `rounded-full` |
| `shadow-{size}` | Adds shadow | `shadow-md`, `shadow-lg` |
| `flex` | Uses flexbox layout | `flex items-center justify-between` |
| `grid` | Uses grid layout | `grid grid-cols-3 gap-8` |
| `hover:{class}` | Applies on hover | `hover:bg-blue-700` |
| `md:`, `lg:` | Responsive prefixes | `md:text-5xl`, `lg:px-8` |

### Common Customization Examples

#### Example 1: Changing Button Color

**Current Code**:
```html
<a href="https://mai.com" class="bg-blue-600 text-white px-8 py-4 rounded-lg font-semibold text-lg hover:bg-blue-700 smooth-transition hover:shadow-lg hover:scale-105 inline-block">
    Start Your Automation Journey
</a>
```

**To Change to Green**:
```html
<a href="https://mai.com" class="bg-green-600 text-white px-8 py-4 rounded-lg font-semibold text-lg hover:bg-green-700 smooth-transition hover:shadow-lg hover:scale-105 inline-block">
    Start Your Automation Journey
</a>
```

**What Changed**:
- `bg-blue-600` → `bg-green-600` (background color)
- `hover:bg-blue-700` → `hover:bg-green-700` (hover color)

**Available Colors** (in Tailwind):
- `blue`, `green`, `red`, `purple`, `orange`, `yellow`, `pink`, `indigo`, `cyan`, `teal`

**Color Shades** (lighter to darker):
- `50`, `100`, `200`, `300`, `400`, `500`, `600`, `700`, `800`, `900`

---

#### Example 2: Changing Section Background Color

**Current Code** (Features Section):
```html
<section id="features" class="py-20 md:py-24 lg:py-28 bg-white">
```

**To Change to Light Gray**:
```html
<section id="features" class="py-20 md:py-24 lg:py-28 bg-gray-50">
```

**Other Background Options**:
```html
<section id="features" class="py-20 md:py-24 lg:py-28 bg-blue-50">
```

---

#### Example 3: Changing Card Border and Shadow

**Current Code** (Feature Card):
```html
<div class="feature-card-hover bg-white border border-gray-200 rounded-xl p-8 hover:border-blue-300">
```

**To Add More Shadow**:
```html
<div class="feature-card-hover bg-white border border-gray-200 rounded-xl p-8 shadow-lg hover:shadow-2xl hover:border-blue-300">
```

**What Changed**:
- Added `shadow-lg` (default shadow)
- Changed `hover:border-blue-300` to `hover:shadow-2xl` (bigger shadow on hover)

---

#### Example 4: Changing Text Size

**Current Code**:
```html
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 tracking-tight mb-4">
    Powerful Features Built for Your Business
</h2>
```

**To Make Smaller**:
```html
<h2 class="text-2xl md:text-3xl lg:text-4xl font-bold text-gray-900 tracking-tight mb-4">
    Powerful Features Built for Your Business
</h2>
```

**What Changed**:
- `text-3xl` → `text-2xl` (mobile size)
- `md:text-4xl` → `md:text-3xl` (tablet size)
- `lg:text-5xl` → `lg:text-4xl` (desktop size)

---

#### Example 5: Changing Spacing

**Current Code**:
```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
```

**To Reduce Gap Between Items**:
```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-4">
```

**What Changed**:
- `gap-8` → `gap-4` (smaller space between grid items)

**Gap Options**: `gap-2`, `gap-4`, `gap-6`, `gap-8`, `gap-12`

---

#### Example 6: Changing Icon Background

**Current Code** (Feature Icon):
```html
<div class="w-12 h-12 bg-blue-100 rounded-lg flex items-center justify-center mb-6">
    <svg class="w-6 h-6 text-blue-600" ...>
```

**To Change to Purple**:
```html
<div class="w-12 h-12 bg-purple-100 rounded-lg flex items-center justify-center mb-6">
    <svg class="w-6 h-6 text-purple-600" ...>
```

**What Changed**:
- `bg-blue-100` → `bg-purple-100` (background)
- `text-blue-600` → `text-purple-600` (icon color)

---

### Responsive Design Classes

Your landing page uses responsive design, which means it looks good on all device sizes. Tailwind uses these prefixes:

| Prefix | Screen Size | Example |
|--------|------------|---------|
| (none) | Mobile (all sizes) | `text-lg` |
| `sm:` | Small screens (640px+) | `sm:px-6` |
| `md:` | Medium screens (768px+) | `md:text-5xl` |
| `lg:` | Large screens (1024px+) | `lg:px-8` |
| `xl:` | Extra large (1280px+) | `xl:text-6xl` |

**Example**:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
    This heading is:
    - 4xl on mobile phones
    - 5xl on tablets (768px+)
    - 6xl on desktops (1024px+)
</h1>
```

### How to Find and Modify Classes

**Step 1**: Locate the element in your HTML file

**Step 2**: Find the `class="..."` attribute

**Step 3**: Identify the classes you want to change

**Step 4**: Replace with new Tailwind classes

**Example**:
```html
<!-- Before -->
<button class="bg-blue-600 text-white px-8 py-4 rounded-lg">Click Me</button>

<!-- After -->
<button class="bg-green-600 text-white px-8 py-4 rounded-xl">Click Me</button>
```

### Common Class Combinations

Here are useful class combinations for common elements:

**Primary Button**:
```html
class="bg-blue-600 text-white px-8 py-4 rounded-lg font-semibold hover:bg-blue-700 smooth-transition"
```

**Secondary Button**:
```html
class="border-2 border-blue-600 text-blue-600 px-8 py-4 rounded-lg font-semibold hover:bg-blue-50 smooth-transition"
```

**Card**:
```html
class="bg-white border border-gray-200 rounded-xl p-8 shadow-md hover:shadow-lg"
```

**Section Container**:
```html
class="py-20 md:py-24 lg:py-28 bg-white"
```

**Grid Layout (3 columns)**:
```html
class="grid grid-cols-1 md:grid-cols-3 gap-8"
```

### Color Palette Reference

Your landing page primarily uses:

- **Primary**: `blue-600` (accent color)
- **Text**: `gray-900` (headings), `gray-700` (body), `gray-600` (secondary)
- **Backgrounds**: `white`, `gray-50` (light), `gray-900` (dark)
- **Accents**: `green`, `purple`, `orange` (for benefit icons)

To maintain consistency, use these colors when making changes.

---

## Fixing and Updating Links

### What Are Links?

Links are clickable elements that take you to different pages or websites. In HTML, they use the `<a>` tag with an `href` attribute:

```html
<a href="https://example.com">Click Here</a>
```

- `<a>` = The link tag
- `href` = The destination (where the link goes)
- `Click Here` = The visible text

### Types of Links on Your Page

Your landing page has three types of links:

1. **Internal Links** - Link to sections on the same page
2. **External Links** - Link to other websites
3. **Navigation Links** - Links in the header and footer

---

### Finding All Links on Your Page

Here's a complete list of all links in your landing page:

#### Navigation Header Links (Lines 52-57)

```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#testimonials">Testimonials</a>
<a href="https://mai.com">Get Started</a>
```

#### Hero Section Links (Lines 89-96)

```html
<a href="https://mai.com">Start Your Automation Journey</a>
<a href="#features">Learn More</a>
```

#### CTA Section Link (Line 248)

```html
<a href="https://mai.com">Get Started Today</a>
```

#### Footer Product Links (Lines 478-482)

```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="https://mai.com">Pricing</a>
```

#### Footer Resources Links (Lines 486-491)

```html
<a href="blog.html">Blog</a>
<a href="#">Documentation</a>
<a href="#">Case Studies</a>
<a href="#">Support</a>
```

#### Footer Legal Links (Lines 495-500)

```html
<a href="privacy.html">Privacy Policy</a>
<a href="terms.html">Terms of Service</a>
<a href="#">Cookie Policy</a>
<a href="#">Contact Us</a>
```

#### Footer Contact (Lines 508-509)

```html
<a href="mailto:admin@mai.com">admin@mai.com</a>
```

#### Footer Social Media (Lines 525-540)

```html
<a href="#">LinkedIn</a>
<a href="#">Twitter</a>
<a href="#">Facebook</a>
```

---

### Updating External Links (Website URLs)

External links go to other websites. You'll see them starting with `https://` or `http://`

#### Step-by-Step: Update Your Main Website Link

**Current Code**:
```html
<a href="https://mai.com" class="bg-blue-600 text-white px-6 py-2 rounded-lg font-medium hover:bg-blue-700 smooth-transition hover:shadow-lg">Get Started</a>
```

**Step 1**: Find `href="https://mai.com"`

**Step 2**: Replace `https://mai.com` with your actual website URL

**Step 3**: Save the file

**Example**:
```html
<a href="https://yourcompany.com" class="bg-blue-600 text-white px-6 py-2 rounded-lg font-medium hover:bg-blue-700 smooth-transition hover:shadow-lg">Get Started</a>
```

**Important**: 
- Keep the `https://` part (it means secure connection)
- Replace only the domain name (yourcompany.com)
- Don't change anything inside `class="..."`

---

#### Where to Update Your Main URL

Update `https://mai.com` to your URL in these locations:

1. **Navigation Header** (Line 57)
   ```html
   <a href="https://mai.com" class="...">Get Started</a>
   ```

2. **Hero Section - First Button** (Line 89)
   ```html
   <a href="https://mai.com" class="...">Start Your Automation Journey</a>
   ```

3. **Hero Section - Learn More** (Line 94)
   ```html
   <a href="#features" class="...">Learn More</a>
   ```
   (This one stays the same - it links to the Features section)

4. **CTA Section** (Line 248)
   ```html
   <a href="https://mai.com" class="...">Get Started Today</a>
   ```

5. **Footer Product Links** (Line 481)
   ```html
   <a href="https://mai.com" class="...">Pricing</a>
   ```

**Quick Find & Replace Method**:
- Open your HTML file in any text editor
- Press `Ctrl+H` (Windows) or `Cmd+H` (Mac)
- Find: `https://mai.com`
- Replace with: `https://yourcompany.com`
- Click "Replace All"

---

### Updating Email Link

**Current Code** (Line 509):
```html
<a href="mailto:admin@mai.com" class="text-blue-400 hover:text-blue-300 smooth-transition">admin@mai.com</a>
```

**To Change**:

1. Find `mailto:admin@mai.com`
2. Replace `admin@mai.com` with your email address
3. Also update the visible text (the part after `>`)

**Example**:
```html
<a href="mailto:hello@yourcompany.com" class="text-blue-400 hover:text-blue-300 smooth-transition">hello@yourcompany.com</a>
```

**Important**: Keep `mailto:` - it tells the browser this is an email link

---

### Updating Social Media Links

**Current Code** (Lines 525-540):
```html
<a href="#" class="text-gray-400 hover:text-blue-400 smooth-transition" aria-label="LinkedIn">
    <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
        <!-- LinkedIn icon -->
    </svg>
</a>
```

**To Add Your Social Media**:

Replace the `#` with your social media URL

**Examples**:
```html
<!-- LinkedIn -->
<a href="https://linkedin.com/company/yourcompany" class="text-gray-400 hover:text-blue-400 smooth-transition" aria-label="LinkedIn">

<!-- Twitter/X -->
<a href="https://twitter.com/yourcompany" class="text-gray-400 hover:text-blue-400 smooth-transition" aria-label="Twitter">

<!-- Facebook -->
<a href="https://facebook.com/yourcompany" class="text-gray-400 hover:text-blue-400 smooth-transition" aria-label="Facebook">
```

**What to Replace**:
- `#` → Your full social media URL
- `yourcompany` → Your actual company name/handle

---

### Fixing Placeholder Links

Some links currently point to `#` (which does nothing) or placeholder pages. Here's how to fix them:

**Current Placeholder Links**:
```html
<a href="#">Documentation</a>
<a href="#">Case Studies</a>
<a href="#">Support</a>
<a href="#">Cookie Policy</a>
<a href="#">Contact Us</a>
```

**Option 1: Link to External Pages**
```html
<a href="https://yourcompany.com/documentation">Documentation</a>
<a href="https://yourcompany.com/case-studies">Case Studies</a>
<a href="https://yourcompany.com/support">Support</a>
<a href="https://yourcompany.com/cookies">Cookie Policy</a>
<a href="https://yourcompany.com/contact">Contact Us</a>
```

**Option 2: Link to Local Files** (pages on your server)
```html
<a href="documentation.html">Documentation</a>
<a href="case-studies.html">Case Studies</a>
<a href="support.html">Support</a>
<a href="cookies.html">Cookie Policy</a>
<a href="contact.html">Contact Us</a>
```

**Option 3: Hide the Link** (if you don't have the page yet)
```html
<!-- Remove the <a> tag entirely or comment it out -->
<!-- <a href="#">Documentation</a> -->
```

---

### Creating Internal Section Links

Internal links jump to sections on the same page using the `#` symbol.

**How They Work**:

1. **Link**: `<a href="#features">Features</a>`
2. **Target Section**: `<section id="features">...</section>`

The `id` must match what's after the `#` in the link.

**Your Current Internal Links**:

| Link | Target Section | ID |
|------|-----------------|-----|
| `#features` | Features Section | `id="features"` |
| `#benefits` | Benefits Section | `id="benefits"` |
| `#faq` | FAQ Section | `id="faq"` |
| `#testimonials` | Testimonials Section | `id="testimonials"` |

**To Add a New Internal Link**:

**Step 1**: Add an ID to the section
```html
<section id="pricing" class="py-20 md:py-24 lg:py-28 bg-white">
    <h2>Our Pricing</h2>
    ...
</section>
```

**Step 2**: Create a link to it
```html
<a href="#pricing" class="text-gray-700 font-medium hover:text-blue-600 smooth-transition">Pricing</a>
```

**Important**: 
- IDs must be unique (only one per page)
- Use lowercase letters and hyphens (no spaces)
- Link must have `#` before the ID name

---

### Link Best Practices

✅ **Do**:
- Use descriptive link text (not "Click Here")
- Test all links after updating
- Use `https://` for secure connections
- Keep external links opening in same window (unless specified)
- Maintain consistent styling with existing links

❌ **Don't**:
- Change anything inside `class="..."` when updating links
- Delete the `href` attribute
- Use spaces in internal link IDs
- Break the `<a>` tag structure

---

### Testing Your Links

After updating links, test them:

1. **Open your HTML file** in a web browser
2. **Click each link** to verify it works
3. **Check that**:
   - External links open the correct website
   - Internal links scroll to the correct section
   - Email links open your email client
   - No 404 errors appear

---

## Adding Privacy and Terms Pages

### Overview

Privacy and Terms pages are legal documents that protect both you and your users. They're required for most websites.

Your landing page already has links to these pages:

**Footer** (Lines 496-500):
```html
<a href="privacy.html">Privacy Policy</a>
<a href="terms.html">Terms of Service</a>
<a href="#">Cookie Policy</a>
```

But the actual pages don't exist yet. Let's create them.

---

### Step 1: Create the Privacy Policy Page

**Step 1a: Create a new file**

1. Open your text editor
2. Create a new blank file
3. Save it as `privacy.html` in the same folder as your `index.html`

**Step 1b: Add the HTML structure**

Copy and paste this complete Privacy Policy page:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Melbourne AI Automation">
    <meta name="author" content="Melbourne AI Automation">
    <title>Privacy Policy - Melbourne AI Automation</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');
        * {
            font-family: 'Inter', sans-serif;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Navigation Header -->
    <header class="sticky top-0 z-50 bg-white shadow-sm">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center">
                <div class="flex items-center space-x-2">
                    <div class="w-10 h-10 bg-gradient-to-br from-blue-600 to-blue-700 rounded-lg flex items-center justify-center">
                        <span class="text-white font-bold text-lg">MAI</span>
                    </div>
                    <span class="font-bold text-xl text-gray-900 hidden sm:inline">Melbourne AI</span>
                </div>
            </div>
            <a href="index.html" class="text-gray-700 font-medium hover:text-blue-600">Back to Home</a>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-20 md:py-24 lg:py-28 bg-white">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-4">Privacy Policy</h1>
            <p class="text-gray-600 mb-12">Last updated: January 2025</p>
            
            <div class="prose prose-lg max-w-none space-y-8">
                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">1. Introduction</h2>
                    <p class="text-gray-700 leading-relaxed">
                        Melbourne AI Automation ("we," "us," "our," or "Company") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website and use our services.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">2. Information We Collect</h2>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        We collect information in various ways, including:
                    </p>
                    <ul class="list-disc list-inside text-gray-700 space-y-2 ml-4">
                        <li><strong>Information You Provide:</strong> Name, email address, phone number, and other information you voluntarily provide when contacting us or using our services.</li>
                        <li><strong>Automatic Information:</strong> IP address, browser type, pages visited, and time spent on pages through cookies and similar tracking technologies.</li>
                        <li><strong>Third-Party Information:</strong> Information from payment processors and other service providers.</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">3. How We Use Your Information</h2>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        We use the information we collect to:
                    </p>
                    <ul class="list-disc list-inside text-gray-700 space-y-2 ml-4">
                        <li>Provide, maintain, and improve our services</li>
                        <li>Process transactions and send related information</li>
                        <li>Send promotional communications (with your consent)</li>
                        <li>Respond to your inquiries and customer support requests</li>
                        <li>Analyze usage patterns to improve user experience</li>
                        <li>Comply with legal obligations</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">4. How We Protect Your Information</h2>
                    <p class="text-gray-700 leading-relaxed">
                        We implement appropriate technical, administrative, and physical security measures to protect your personal information against unauthorized access, alteration, disclosure, or destruction. However, no method of transmission over the Internet or electronic storage is completely secure.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">5. Sharing Your Information</h2>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        We do not sell, trade, or rent your personal information to third parties. We may share your information with:
                    </p>
                    <ul class="list-disc list-inside text-gray-700 space-y-2 ml-4">
                        <li>Service providers who assist in operating our website and conducting our business</li>
                        <li>Legal authorities when required by law</li>
                        <li>Business partners with your consent</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">6. Your Rights</h2>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        Depending on your location, you may have certain rights regarding your personal information, including:
                    </p>
                    <ul class="list-disc list-inside text-gray-700 space-y-2 ml-4">
                        <li>The right to access your personal information</li>
                        <li>The right to correct inaccurate data</li>
                        <li>The right to request deletion of your data</li>
                        <li>The right to opt-out of marketing communications</li>
                    </ul>
                    <p class="text-gray-700 leading-relaxed mt-4">
                        To exercise these rights, please contact us at admin@mai.com.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">7. Cookies</h2>
                    <p class="text-gray-700 leading-relaxed">
                        Our website uses cookies to enhance your experience. Cookies are small files stored on your device that help us remember your preferences and understand how you use our site. You can control cookie settings through your browser.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">8. Third-Party Links</h2>
                    <p class="text-gray-700 leading-relaxed">
                        Our website may contain links to third-party websites. We are not responsible for the privacy practices of these external sites. We encourage you to review their privacy policies before providing any information.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">9. Children's Privacy</h2>
                    <p class="text-gray-700 leading-relaxed">
                        Our services are not directed to children under the age of 13. We do not knowingly collect personal information from children. If we become aware that we have collected information from a child, we will delete such information promptly.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">10. Changes to This Policy</h2>
                    <p class="text-gray-700 leading-relaxed">
                        We may update this Privacy Policy from time to time. Changes will be effective immediately upon posting to the website. Your continued use of our services constitutes your acceptance of the updated policy.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">11. Contact Us</h2>
                    <p class="text-gray-700 leading-relaxed">
                        If you have questions about this Privacy Policy or our privacy practices, please contact us at:
                    </p>
                    <div class="bg-gray-50 p-6 rounded-lg mt-4">
                        <p class="text-gray-700"><strong>Melbourne AI Automation</strong></p>
                        <p class="text-gray-700">Email: admin@mai.com</p>
                        <p class="text-gray-700">Melbourne, Victoria, Australia</p>
                    </div>
                </section>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-16 md:py-20">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="border-t border-gray-800 pt-8 flex flex-col md:flex-row items-center justify-between">
                <p class="text-gray-400 text-sm mb-4 md:mb-0">
                    &copy; 2025 Melbourne AI Automation. All rights reserved.
                </p>
                <a href="index.html" class="text-gray-400 hover:text-blue-400">Back to Home</a>
            </div>
        </div>
    </footer>
</body>
</html>
```

**Step 1c: Customize the Privacy Policy**

Replace these placeholder sections with your actual information:

1. **Company Name**: Replace `Melbourne AI Automation` with your company name
2. **Email Address**: Replace `admin@mai.com` with your email
3. **Location**: Replace `Melbourne, Victoria, Australia` with your location
4. **Last Updated Date**: Update the date at the top
5. **Policy Content**: Customize each section to match your actual practices

---

### Step 2: Create the Terms of Service Page

**Step 2a: Create a new file**

1. Open your text editor
2. Create a new blank file
3. Save it as `terms.html` in the same folder as your `index.html`

**Step 2b: Add the HTML structure**

Copy and paste this complete Terms of Service page:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - Melbourne AI Automation">
    <meta name="author" content="Melbourne AI Automation">
    <title>Terms of Service - Melbourne AI Automation</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');
        * {
            font-family: 'Inter', sans-serif;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Navigation Header -->
    <header class="sticky top-0 z-50 bg-white shadow-sm">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center">
                <div class="flex items-center space-x-2">
                    <div class="w-10 h-10 bg-gradient-to-br from-blue-600 to-blue-700 rounded-lg flex items-center justify-center">
                        <span class="text-white font-bold text-lg">MAI</span>
                    </div>
                    <span class="font-bold text-xl text-gray-900 hidden sm:inline">Melbourne AI</span>
                </div>
            </div>
            <a href="index.html" class="text-gray-700 font-medium hover:text-blue-600">Back to Home</a>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-20 md:py-24 lg:py-28 bg-white">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-4">Terms of Service</h1>
            <p class="text-gray-600 mb-12">Last updated: January 2025</p>
            
            <div class="prose prose-lg max-w-none space-y-8">
                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">1. Agreement to Terms</h2>
                    <p class="text-gray-700 leading-relaxed">
                        These Terms of Service ("Terms") constitute a legally binding agreement between you ("User," "you," or "your") and Melbourne AI Automation ("Company," "we," "us," or "our"). By accessing or using our website and services, you agree to be bound by these Terms. If you do not agree to abide by the above, please do not use this service.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">2. Use License</h2>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        Permission is granted to temporarily download one copy of the materials (information or software) on our website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                    </p>
                    <ul class="list-disc list-inside text-gray-700 space-y-2 ml-4">
                        <li>Modifying or copying the materials</li>
                        <li>Using the materials for any commercial purpose or for any public display</li>
                        <li>Attempting to decompile or reverse engineer any software contained on the website</li>
                        <li>Transferring the materials to another person or "mirroring" the materials on any other server</li>
                        <li>Removing any copyright or other proprietary notations from the materials</li>
                        <li>Transmitting the materials over a network</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">3. Disclaimer</h2>
                    <p class="text-gray-700 leading-relaxed">
                        The materials on our website are provided on an 'as is' basis. Melbourne AI Automation makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">4. Limitations</h2>
                    <p class="text-gray-700 leading-relaxed">
                        In no event shall Melbourne AI Automation or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on our website, even if we or our authorized representative has been notified orally or in writing of the possibility of such damage.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">5. Accuracy of Materials</h2>
                    <p class="text-gray-700 leading-relaxed">
                        The materials appearing on our website could include technical, typographical, or photographic errors. Melbourne AI Automation does not warrant that any of the materials on our website are accurate, complete, or current. We may make changes to the materials contained on our website at any time without notice.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">6. Materials and Services</h2>
                    <p class="text-gray-700 leading-relaxed">
                        Melbourne AI Automation has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by us of the site. Use of any such linked website is at the user's own risk.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">7. Modifications</h2>
                    <p class="text-gray-700 leading-relaxed">
                        Melbourne AI Automation may revise these terms of service for our website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">8. Governing Law</h2>
                    <p class="text-gray-700 leading-relaxed">
                        These terms and conditions are governed by and construed in accordance with the laws of Victoria, Australia, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">9. User Responsibilities</h2>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        As a user of our services, you agree to:
                    </p>
                    <ul class="list-disc list-inside text-gray-700 space-y-2 ml-4">
                        <li>Provide accurate and complete information</li>
                        <li>Maintain the confidentiality of your account information</li>
                        <li>Not engage in any illegal or unauthorized activities</li>
                        <li>Not interfere with or disrupt the integrity or performance of our services</li>
                        <li>Comply with all applicable laws and regulations</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">10. Intellectual Property Rights</h2>
                    <p class="text-gray-700 leading-relaxed">
                        All content on our website, including text, graphics, logos, images, and software, is the property of Melbourne AI Automation or its content suppliers and is protected by international copyright laws. Unauthorized reproduction or distribution is prohibited.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">11. Limitation of Liability</h2>
                    <p class="text-gray-700 leading-relaxed">
                        In no case shall Melbourne AI Automation, our directors, officers, or employees be liable for any indirect, incidental, special, or consequential damages arising from your use of or inability to use our services.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">12. Contact Us</h2>
                    <p class="text-gray-700 leading-relaxed">
                        If you have any questions about these Terms of Service, please contact us at:
                    </p>
                    <div class="bg-gray-50 p-6 rounded-lg mt-4">
                        <p class="text-gray-700"><strong>Melbourne AI Automation</strong></p>
                        <p class="text-gray-700">Email: admin@mai.com</p>
                        <p class="text-gray-700">Melbourne, Victoria, Australia</p>
                    </div>
                </section>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-16 md:py-20">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="border-t border-gray-800 pt-8 flex flex-col md:flex-row items-center justify-between">
                <p class="text-gray-400 text-sm mb-4 md:mb-0">
                    &copy; 2025 Melbourne AI Automation. All rights reserved.
                </p>
                <a href="index.html" class="text-gray-400 hover:text-blue-400">Back to Home</a>
            </div>
        </div>
    </footer>
</body>
</html>
```

**Step 2c: Customize the Terms of Service**

Replace these placeholder sections:

1. **Company Name**: Replace `Melbourne AI Automation` with your company name
2. **Email Address**: Replace `admin@mai.com` with your email
3. **Location**: Replace `Melbourne, Victoria, Australia` with your location
4. **Governing Law**: Update to match your actual jurisdiction
5. **Terms Content**: Customize each section to match your actual business terms

---

### Step 3: Verify Links Work

**Step 3a: Check your index.html**

Make sure these lines exist in your footer (they should):

```html
<a href="privacy.html">Privacy Policy</a>
<a href="terms.html">Terms of Service</a>
```

**Step 3b: Test the links**

1. Open `index.html` in your browser
2. Scroll to the footer
3. Click "Privacy Policy" - it should open `privacy.html`
4. Click "Terms of Service" - it should open `terms.html`
5. Click "Back to Home" on each page - it should return to `index.html`

**Step 3c: Troubleshoot if links don't work**

| Problem | Solution |
|---------|----------|
| Links don't work | Make sure all three files (`index.html`, `privacy.html`, `terms.html`) are in the same folder |
| Page looks broken | Copy the code exactly as provided above |
| Links return 404 error | Check file names are spelled correctly (lowercase, .html extension) |

---

### Step 4: Optional - Add Cookie Policy Page

If you want a Cookie Policy page as well:

**Step 4a: Create the file**

1. Create a new file named `cookies.html`
2. Save it in the same folder as `index.html`

**Step 4b: Add this code**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Cookie Policy - Melbourne AI Automation">
    <meta name="author" content="Melbourne AI Automation">
    <title>Cookie Policy - Melbourne AI Automation</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');
        * {
            font-family: 'Inter', sans-serif;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Navigation Header -->
    <header class="sticky top-0 z-50 bg-white shadow-sm">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center">
                <div class="flex items-center space-x-2">
                    <div class="w-10 h-10 bg-gradient-to-br from-blue-600 to-blue-700 rounded-lg flex items-center justify-center">
                        <span class="text-white font-bold text-lg">MAI</span>
                    </div>
                    <span class="font-bold text-xl text-gray-900 hidden sm:inline">Melbourne AI</span>
                </div>
            </div>
            <a href="index.html" class="text-gray-700 font-medium hover:text-blue-600">Back to Home</a>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-20 md:py-24 lg:py-28 bg-white">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-4">Cookie Policy</h1>
            <p class="text-gray-600 mb-12">Last updated: January 2025</p>
            
            <div class="prose prose-lg max-w-none space-y-8">
                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">1. What Are Cookies?</h2>
                    <p class="text-gray-700 leading-relaxed">
                        Cookies are small files that are stored on your device when you visit our website. They help us remember your preferences, understand how you use our site, and provide a better user experience. Cookies are not programs and cannot harm your device.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">2. Types of Cookies We Use</h2>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        We use the following types of cookies:
                    </p>
                    <ul class="list-disc list-inside text-gray-700 space-y-2 ml-4">
                        <li><strong>Essential Cookies:</strong> Required for the website to function properly</li>
                        <li><strong>Performance Cookies:</strong> Help us understand how visitors use our website</li>
                        <li><strong>Preference Cookies:</strong> Remember your preferences and settings</li>
                        <li><strong>Marketing Cookies:</strong> Track your activity to show relevant advertisements</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">3. How to Control Cookies</h2>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        You can control or delete cookies through your browser settings. Here's how:
                    </p>
                    <ul class="list-disc list-inside text-gray-700 space-y-2 ml-4">
                        <li><strong>Chrome:</strong> Settings > Privacy and Security > Cookies and other site data</li>
                        <li><strong>Firefox:</strong> Options > Privacy & Security > Cookies and Site Data</li>
                        <li><strong>Safari:</strong> Preferences > Privacy > Cookies and website data</li>
                        <li><strong>Edge:</strong> Settings > Privacy, search, and services > Clear browsing data</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">4. Third-Party Cookies</h2>
                    <p class="text-gray-700 leading-relaxed">
                        Some cookies may be set by third-party services we use, such as analytics providers. These services have their own cookie policies, and we encourage you to review them.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">5. Changes to This Policy</h2>
                    <p class="text-gray-700 leading-relaxed">
                        We may update this Cookie Policy from time to time. Changes will be effective immediately upon posting.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">6. Contact Us</h2>
                    <p class="text-gray-700 leading-relaxed">
                        If you have questions about this Cookie Policy, please contact us at:
                    </p>
                    <div class="bg-gray-50 p-6 rounded-lg mt-4">
                        <p class="text-gray-700"><strong>Melbourne AI Automation</strong></p>
                        <p class="text-gray-700">Email: admin@mai.com</p>
                        <p class="text-gray-700">Melbourne, Victoria, Australia</p>
                    </div>
                </section>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-16 md:py-20">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="border-t border-gray-800 pt-8 flex flex-col md:flex-row items-center justify-between">
                <p class="text-gray-400 text-sm mb-4 md:mb-0">
                    &copy; 2025 Melbourne AI Automation. All rights reserved.
                </p>
                <a href="index.html" class="text-gray-400 hover:text-blue-400">Back to Home</a>
            </div>
        </div>
    </footer>
</body>
</html>
```

**Step 4c: Update the footer link**

In `index.html`, find this line (around line 499):
```html
<a href="#">Cookie Policy</a>
```

Replace it with:
```html
<a href="cookies.html">Cookie Policy</a>
```

---

### Step 5: Best Practices

✅ **Do**:
- Keep policies clear and easy to understand
- Update policies when your practices change
- Include your contact information
- Review policies annually
- Test all links before publishing

❌ **Don't**:
- Copy policies from competitors without customization
- Leave placeholder information in policies
- Forget to update company information
- Ignore legal requirements for your jurisdiction

---

## Common Customization Tasks

### Task 1: Change Your Logo

**Current Logo** (Line 47-50):
```html
<div class="w-10 h-10 bg-gradient-to-br from-blue-600 to-blue-700 rounded-lg flex items-center justify-center">
    <span class="text-white font-bold text-lg">MAI</span>
</div>
```

**Option A: Replace with Text**
```html
<span class="font-bold text-xl text-blue-600">YourLogo</span>
```

**Option B: Replace with Image**
```html
<img src="logo.png" alt="Company Logo" class="h-10 w-auto">
```

(Make sure `logo.png` is in the same folder as `index.html`)

**Option C: Keep Gradient but Change Letters**
```html
<div class="w-10 h-10 bg-gradient-to-br from-blue-600 to-blue-700 rounded-lg flex items-center justify-center">
    <span class="text-white font-bold text-lg">YC</span>
</div>
```

---

### Task 2: Add a New Feature Card

**Current Feature Card** (Lines 113-135):
```html
<div class="feature-card-hover bg-white border border-gray-200 rounded-xl p-8 hover:border-blue-300">
    <div class="w-12 h-12 bg-blue-100 rounded-lg flex items-center justify-center mb-6">
        <svg class="w-6 h-6 text-blue-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2m0-8c1.11 0 2.08.402 2.599 1M12 8V7m0 1v8m0 0v1m0-1c-1.11 0-2.08-.402-2.599-1M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path>
        </svg>
    </div>
    <h3 class="text-xl font-bold text-gray-900 mb-3">Low Cost</h3>
    <p class="text-gray-600 leading-relaxed mb-4">
        Enterprise-grade automation without the enterprise price tag...
    </p>
    <ul class="space-y-2 text-sm text-gray-600">
        <li class="flex items-start">
            <span class="text-blue-600 mr-3 font-bold">✓</span>
            <span>Transparent, predictable pricing</span>
        </li>
    </ul>
</div>
```

**To Add a Fourth Feature**:

1. Find the closing `</div>` of the third feature card (line 160)
2. Add this new card after it:

```html
<!-- Feature 4: Your New Feature -->
<div class="feature-card-hover bg-white border border-gray-200 rounded-xl p-8 hover:border-blue-300">
    <div class="w-12 h-12 bg-blue-100 rounded-lg flex items-center justify-center mb-6">
        <svg class="w-6 h-6 text-blue-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m7 0a9 9 0 11-18 0 9 9 0 0118 0z"></path>
        </svg>
    </div>
    <h3 class="text-xl font-bold text-gray-900 mb-3">Your Feature Name</h3>
    <p class="text-gray-600 leading-relaxed mb-4">
        Your feature description explaining the benefit and value.
    </p>
    <ul class="space-y-2 text-sm text-gray-600">
        <li class="flex items-start">
            <span class="text-blue-600 mr-3 font-bold">✓</span>
            <span>Your first benefit</span>
        </li>
        <li class="flex items-start">
            <span class="text-blue-600 mr-3 font-bold">✓</span>
            <span>Your second benefit</span>
        </li>
    </ul>
</div>
```

3. Update the grid to show 4 columns on large screens:

**Current** (Line 108):
```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
```

**Change to**:
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
```

---

### Task 3: Change Color Scheme

Your landing page uses blue as the primary color. To change the entire color scheme:

**Find and Replace** (Using Find & Replace in your text editor):

| Find | Replace | New Color |
|------|---------|-----------|
| `blue-600` | `green-600` | Green |
| `blue-700` | `green-700` | Green |
| `blue-100` | `green-100` | Green |
| `blue-50` | `green-50` | Green |

**Or manually update key areas**:

1. **Navigation buttons** (Line 57)
2. **Hero buttons** (Lines 89, 94)
3. **Feature icons** (Lines 116, 133, 150)
4. **CTA button** (Line 248)
5. **Footer links** (Lines 478-540)

---

### Task 4: Add Google Analytics

**Step 1**: Get your Google Analytics ID from Google Analytics dashboard

**Step 2**: Add this code in the `<head>` section (after line 9):

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

**Step 3**: Replace `GA_MEASUREMENT_ID` with your actual ID (e.g., `G-1234567890`)

---

### Task 5: Add a Contact Form

**Step 1**: Find a form service (Formspree, Netlify Forms, or EmailJS)

**Step 2**: Add this form code where you want it:

```html
<section class="py-20 md:py-24 lg:py-28 bg-gray-50">
    <div class="max-w-2xl mx-auto px-4 sm:px-6 lg:px-8">
        <h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-8 text-center">Get In Touch</h2>
        
        <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST" class="space-y-6">
            <div>
                <label class="block text-gray-700 font-semibold mb-2">Name</label>
                <input type="text" name="name" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:border-blue-600">
            </div>
            
            <div>
                <label class="block text-gray-700 font-semibold mb-2">Email</label>
                <input type="email" name="email" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:border-blue-600">
            </div>
            
            <div>
                <label class="block text-gray-700 font-semibold mb-2">Message</label>
                <textarea name="message" rows="5" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:border-blue-600"></textarea>
            </div>
            
            <button type="submit" class="w-full bg-blue-600 text-white px-8 py-3 rounded-lg font-semibold hover:bg-blue-700 smooth-transition">
                Send Message
            </button>
        </form>
    </div>
</section>
```

---

## Troubleshooting Guide

### Issue 1: Page Looks Broken After Editing

**Symptoms**: Styles are missing, layout is messed up, or elements are in weird positions

**Solutions**:

1. **Check for missing closing tags**
   - Make sure every `<div>` has a closing `</div>`
   - Make sure every `<p>` has a closing `</p>`
   - Count opening and closing tags

2. **Check Tailwind CSS is loaded**
   - Make sure this line is in your `<head>`:
   ```html
   <script src="https://cdn.tailwindcss.com"></script>
   ```

3. **Restore from backup**
   - If you can't find the error, restore your original file and make changes again more carefully

---

### Issue 2: Links Don't Work

**Symptoms**: Clicking a link does nothing or shows 404 error

**Solutions**:

1. **Check href attribute**
   ```html
   <!-- Wrong -->
   <a href"https://example.com">Link</a>
   
   <!-- Correct -->
   <a href="https://example.com">Link</a>
   ```

2. **Check file names match exactly**
   - File is named `privacy.html` but link says `privacy.HTML` ❌
   - File is named `privacy.html` and link says `privacy.html` ✅

3. **Check files are in same folder**
   - All HTML files should be in the same directory

---

### Issue 3: Text Content Doesn't Show

**Symptoms**: You edited text but it doesn't appear on the page

**Solutions**:

1. **Hard refresh your browser**
   - Windows: `Ctrl + Shift + R`
   - Mac: `Cmd + Shift + R`

2. **Check you saved the file**
   - Look for an asterisk (*) in your editor's title bar (unsaved changes)

3. **Check you're editing the right file**
   - Make sure you're editing `index.html`, not a backup

---

### Issue 4: Styling Changes Don't Apply

**Symptoms**: You changed Tailwind classes but styles don't update

**Solutions**:

1. **Hard refresh browser** (see above)

2. **Check class name is correct**
   - `text-blue-600` ✅
   - `text-blue600` ❌ (missing hyphen)
   - `textblue-600` ❌ (wrong order)

3. **Make sure you didn't delete other classes**
   - Each class should be separated by a space
   ```html
   <!-- Correct -->
   class="text-lg text-gray-700 font-medium"
   
   <!-- Wrong -->
   class="text-lg text-gray-700 font-medium" (missing space)
   ```

---

### Issue 5: Mobile Version Looks Bad

**Symptoms**: Page looks fine on desktop but broken on mobile

**Solutions**:

1. **Check responsive classes**
   ```html
   <!-- Good - works on all sizes -->
   class="text-2xl md:text-3xl lg:text-4xl"
   
   <!-- Bad - only shows on desktop -->
   class="lg:text-4xl"
   ```

2. **Test on actual mobile device**
   - Use Chrome DevTools (F12) to view mobile version

3. **Check viewport meta tag exists**
   ```html
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   ```

---

### Issue 6: Images Don't Show

**Symptoms**: Image tags show broken image icon

**Solutions**:

1. **Check file path**
   ```html
   <!-- If image is in same folder -->
   <img src="image.png" alt="Description">
   
   <!-- If image is in subfolder -->
   <img src="images/image.png" alt="Description">
   ```

2. **Check file extension**
   - File is named `logo.jpg` but code says `logo.png` ❌

3. **Check file exists**
   - Make sure the image file is in the correct folder

---

### Issue 7: Accordion (FAQ) Doesn't Expand

**Symptoms**: Clicking FAQ questions doesn't expand the answers

**Solutions**:

1. **Check JavaScript is enabled**
   - Enable JavaScript in your browser settings

2. **Check script is included**
   - Make sure this code is at the bottom of your HTML:
   ```html
   <script>
       function toggleAccordion(button) {
           const content = button.nextElementSibling;
           const icon = button.querySelector('svg');
           // ... rest of function
       }
   </script>
   ```

3. **Check onclick attribute exists**
   ```html
   <button ... onclick="toggleAccordion(this)">
   ```

---

### Issue 8: Form Doesn't Submit

**Symptoms**: Clicking submit button does nothing

**Solutions**:

1. **Check form action**
   ```html
   <form action="https://formspree.io/f/YOUR_ID" method="POST">
   ```
   - Replace `YOUR_ID` with actual form ID

2. **Check input names**
   ```html
   <input type="text" name="name" required>
   ```
   - All inputs need `name` attribute

3. **Check form service is active**
   - Verify your form service account is active and verified

---

## Best Practices

### 1. Version Control & Backups

**Always keep backups**:
- Save original `index.html` as `index-backup.html`
- Use version control (Git) if possible
- Create a new file before making major changes

**Example Backup Workflow**:
```
index.html (current version)
index-v1.html (backup)
index-v2.html (another backup)
```

---

### 2. Testing Checklist

Before publishing changes, test:

- [ ] All text displays correctly
- [ ] All links work (internal and external)
- [ ] Page looks good on mobile (test with DevTools)
- [ ] Page looks good on tablet (test with DevTools)
- [ ] Page looks good on desktop
- [ ] All buttons are clickable
- [ ] All images load
- [ ] FAQ accordion expands/collapses
- [ ] Forms submit correctly
- [ ] No console errors (F12 > Console tab)

---

### 3. Naming Conventions

Use consistent, descriptive names:

**File Names**:
- `index.html` (main page)
- `privacy.html` (privacy policy)
- `terms.html` (terms of service)
- `about.html` (about page)
- `contact.html` (contact page)

**Image Names**:
- `hero-background.png`
- `feature-icon-1.svg`
- `testimonial-avatar.jpg`

**Avoid**:
- `file1.html`, `file2.html`
- `image.jpg`, `image2.jpg`
- Spaces in file names: `my file.html` ❌
- Capital letters: `MyFile.html` (use `my-file.html` instead)

---

### 4. Performance Optimization

**Reduce page load time**:

1. **Compress images**
   - Use tools like TinyPNG or ImageOptim
   - Target max 100KB per image

2. **Minimize CSS/JS**
   - Remove unused code
   - Use minification tools

3. **Lazy load images**
   ```html
   <img src="image.jpg" loading="lazy" alt="Description">
   ```

---

### 5. SEO Best Practices

**Improve search engine visibility**:

1. **Update meta tags** (in `<head>`):
   ```html
   <meta name="description" content="Your page description (160 characters)">
   <meta name="keywords" content="keyword1, keyword2, keyword3">
   <title>Your Page Title - Your Company</title>
   ```

2. **Use descriptive alt text** for images:
   ```html
   <img src="feature.png" alt="Descriptive text about the image">
   ```

3. **Use heading hierarchy**:
   ```html
   <h1>Main Title (only one per page)</h1>
   <h2>Section Title</h2>
   <h3>Subsection Title</h3>
   ```

---

### 6. Accessibility Best Practices

**Make your site usable for everyone**:

1. **Use semantic HTML**:
   ```html
   <header></header>
   <nav></nav>
   <main></main>
   <section></section>
   <footer></footer>
   ```

2. **Include alt text for images**:
   ```html
   <img src="logo.png" alt="Company Logo">
   ```

3. **Use descriptive link text**:
   ```html
   <!-- Good -->
   <a href="/about">Learn more about our company</a>
   
   <!-- Bad -->
   <a href="/about">Click here</a>
   ```

4. **Ensure color contrast**:
   - Text should be easily readable against background
   - Use contrast checker tools

---

### 7. Regular Maintenance

**Keep your site healthy**:

| Task | Frequency |
|------|-----------|
| Update content | Monthly |
| Check broken links | Quarterly |
| Update copyright year | Annually |
| Review analytics | Monthly |
| Backup files | Weekly |
| Update policies | Annually |

---

### 8. Security Best Practices

**Protect your website**:

1. **Use HTTPS**
   - Ensure your hosting provider uses SSL certificates

2. **Keep software updated**
   - Update any CMS or backend software regularly

3. **Validate form inputs**
   - Never trust user input
   - Always validate on the server side

4. **Protect sensitive information**
   - Never hardcode API keys or passwords
   - Use environment variables

---

## Quick Reference

### File Structure

```
your-project-folder/
├── index.html           (main landing page)
├── privacy.html         (privacy policy)
├── terms.html           (terms of service)
├── cookies.html         (cookie policy)
├── images/              (folder for images)
│   ├── logo.png
│   └── hero-bg.jpg
└── css/                 (optional: custom styles)
    └── custom.css
```

---

### Common Tailwind Classes Reference

```html
<!-- Text Size -->
text-xs, text-sm, text-base, text-lg, text-xl, text-2xl, text-3xl, text-4xl, text-5xl, text-6xl

<!-- Text Color -->
text-gray-900, text-gray-700, text-gray-600, text-blue-600, text-green-600, text-white

<!-- Background Color -->
bg-white, bg-gray-50, bg-blue-600, bg-green-600, bg-gray-900

<!-- Padding/Margin -->
p-4, p-6, p-8 (padding)
m-4, m-6, m-8 (margin)
mb-4, mb-6, mb-8 (margin-bottom)
mt-4, mt-6, mt-8 (margin-top)

<!-- Border & Shadow -->
border, border-gray-200, rounded-lg, rounded-xl, shadow-md, shadow-lg

<!-- Flexbox/Grid -->
flex, items-center, justify-between (flexbox)
grid, grid-cols-1, grid-cols-2, grid-cols-3, gap-8 (grid)

<!-- Responsive -->
md:text-5xl (medium screens and up)
lg:px-8 (large screens and up)

<!-- Hover Effects -->
hover:bg-blue-700, hover:text-blue-600, hover:shadow-lg
```

---

### HTML Tag Reference

```html
<!-- Structure -->
<header></header>      <!-- Top of page -->
<nav></nav>            <!-- Navigation -->
<main></main>          <!-- Main content -->
<section></section>    <!-- Content section -->
<footer></footer>      <!-- Bottom of page -->

<!-- Text -->
<h1></h1>              <!-- Main heading -->
<h2></h2>              <!-- Section heading -->
<p></p>                <!-- Paragraph -->
<span></span>          <!-- Inline text -->

<!-- Links & Images -->
<a href="">Link</a>    <!-- Link -->
<img src="" alt="">    <!-- Image -->

<!-- Forms -->
<form></form>          <!-- Form container -->
<input type="text">    <!-- Text input -->
<textarea></textarea>  <!-- Multi-line text -->
<button></button>      <!-- Button -->

<!-- Lists -->
<ul></ul>              <!-- Unordered list -->
<ol></ol>              <!-- Ordered list -->
<li></li>              <!-- List item -->

<!-- Containers -->
<div></div>            <!-- Generic container -->
<article></article>    <!-- Article content -->
```

---

## Getting Help

If you encounter issues not covered in this guide:

1. **Check the official Tailwind CSS documentation**
   - https://tailwindcss.com/docs

2. **Search Stack Overflow**
   - Tag your question with `html`, `css`, `tailwind`

3. **Review the original code comments**
   - Look for hints in the HTML comments

4. **Use browser DevTools**
   - Press F12 to inspect elements and debug

5. **Validate your HTML**
   - Use https://validator.w3.org/

---

## Conclusion

You now have a comprehensive guide to maintain and customize your Melbourne AI Automation landing page. Start with small changes, test thoroughly, and refer back to this guide whenever you need help.

**Key Takeaways**:
- ✅ Always backup your files before making changes
- ✅ Test changes in your browser before publishing
- ✅ Use this guide as a reference for common tasks
- ✅ Keep your content fresh and updated
- ✅ Monitor your site's performance and user feedback

Happy customizing! 🚀