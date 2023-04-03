# 🌎 **flaskWebsite**
This is my second website, built using Flask and Tailwind CSS. My first website was built with Streamlit, but I'm starting to learn more about HTML and CSS so I'm building a new website from scratch.

## 🖥️ **GPT-4 Wrote a description of my website:** 

This website is a personal resume site for Bassim. The site is built using HTML, CSS, and JavaScript, along with the Flask framework for the backend and the TailwindCSS utility-first CSS framework for styling. The code is organized into a standard HTML5 document structure, including a doctype declaration, a head section with metadata, and a body section containing the site's content.

The head section contains metadata like the site's title and description, which are important for search engine optimization (SEO). It also includes a link to an external CSS file, "output.css", which is generated from TailwindCSS. Additionally, there is an embedded style block that contains custom CSS, such as the keyframes animation for the "background-pan" and the "rotating-gradient-border" class. This custom CSS is used to create a visually appealing gradient border effect throughout the site.

The body section is structured using a combination of divs, headings, paragraphs, lists, and SVGs. It begins with a gradient border at the top of the page, followed by a container that holds the main content. The main content consists of various sections, each with headings and paragraphs that describe Bassim's expertise, skills, and learning objectives. These sections are organized using the CSS Grid layout, which makes the content responsive and easy to read on various screen sizes.

The website also features interactive SVG icons, representing Bassim's IT skills and learning objectives. These icons are created using SVG paths and are styled with a linear gradient to give them a modern and engaging appearance.

Towards the end of the body section, there is a contact form that allows users to send messages directly to Bassim. This form uses the Formspree service to handle form submissions, ensuring that messages are sent to Bassim's email without the need for any server-side code.

Lastly, there is a JavaScript script at the bottom of the body section, which adds a fun interaction to the headings. When a user hovers over a heading, the letters in the heading are temporarily replaced with random letters, giving the impression of a scramble effect. This interaction is achieved by using event listeners, intervals, and string manipulation.

Overall, this website is a clean, modern, and interactive personal resume site that showcases Bassim's skills and expertise in a visually appealing and engaging manner.

# 🛠️  **Components**
## 📝 **Form**
This website features text components in addition to a Formspree form. The form works flawlessly, sending me an email each time it's submitted. 

---
## 🎨 **Gradients**
I created an aminated gradient border around my text box and at the top of my page using the following tailwind code:
```css
from-violet-600 via-blue-600 to-fuchsia-600
```
However, in order to animate the gradient I had to copy the hex codes to create the @keyframes animation. I then created an infinite gradient animation.


This is the animation code:
```css
    @keyframes background-pan {
    from {
        background-position: 0% center;
    }
    to {
        background-position: -200% center;
    }
    }

    .rotating-gradient-border {
    animation: background-pan 5s linear infinite;
    background: linear-gradient(
        to right,
        #7C3AED,
        #2563EB,
        #C026D3,
        #7C3AED
    );
    background-size: 200% auto;
    }
```
---
## **SVG Graphics**
I initially wanted to add a lottie animation to my website, but an SVG graphic was much easier to implement. 

The two SVG sizes are currently mismatched, but they appear to be the same size when the page is loaded. This is due to the design of the SVGs themselves, one appears smaller than the other.

I used the following SVG code:
```html
<svg width="175" height="175" viewBox="0 0 200 200" fill="none" xmlns="http://www.w3.org/2000/svg"> <g clip-path="url(#clip0_231_240)"> <path fill-rule="evenodd" clip-rule="evenodd" d="M0 49H27.5H28V48.9943C39.6432 48.7286 49 39.207 49 27.5V0H55V28C55 39.598 64.402 49 76 49C87.598 49 97 39.598 97 28V0H103V28C103 39.598 112.402 49 124 49C135.598 49 145 39.598 145 28V0H152V28C152 39.598 161.402 49 173 49H200V55H172C160.402 55 151 64.402 151 76C151 87.598 160.402 97 172 97H200V103H172C160.402 103 151 112.402 151 124C151 135.598 160.402 145 172 145H200V151H173C161.402 151 152 160.402 152 172V173V200H145V172C145 160.402 135.598 151 124 151C112.402 151 103 160.402 103 172V200H97V172C97 160.402 87.598 151 76 151C64.402 151 55 160.402 55 172V200H49V172.5C49 160.793 39.6432 151.271 28 151.006V151H27.5H0V145H28C39.598 145 49 135.598 49 124C49 112.402 39.598 103 28 103L0 103V97L28 97C39.598 97 49 87.598 49 76C49 64.402 39.598 55 28 55L0 55V49ZM76 97C87.598 97 97 87.598 97 76C97 64.402 87.598 55 76 55C64.402 55 55 64.402 55 76C55 87.598 64.402 97 76 97ZM124 97C135.598 97 145 87.598 145 76C145 64.402 135.598 55 124 55C112.402 55 103 64.402 103 76C103 87.598 112.402 97 124 97ZM97 124C97 135.598 87.598 145 76 145C64.402 145 55 135.598 55 124C55 112.402 64.402 103 76 103C87.598 103 97 112.402 97 124ZM124 145C135.598 145 145 135.598 145 124C145 112.402 135.598 103 124 103C112.402 103 103 112.402 103 124C103 135.598 112.402 145 124 145Z" fill="url(#paint0_linear_231_240)"/> </g> <defs> <linearGradient id="paint0_linear_231_240" x1="20.5" y1="16" x2="100" y2="200" gradientUnits="userSpaceOnUse"> <stop stop-color="#ACAAFF"/> <stop offset="1" stop-color="#C0E8FF"/> </linearGradient> <clipPath id="clip0_231_240"> <rect width="200" height="200" fill="white"/> </clipPath> </defs> </svg>          
```
---
``` html
<svg width="200" height="200" viewBox="0 0 200 200" fill="none" xmlns="http://www.w3.org/2000/svg"> <g clip-path="url(#clip0_105_351)"> <path d="M156.064 143.936L112.127 100L156.064 56.0636L200 100L156.064 143.936ZM43.9364 143.936L0 100L43.9364 56.0636L87.8728 100L43.9364 143.936ZM100 200L56.0636 156.064L100 112.127L143.936 156.064L100 200ZM100 87.8728L56.0636 43.9364L100 0L143.936 43.9364L100 87.8728Z" fill="url(#paint0_linear_105_351)"/> </g> <defs> <linearGradient id="paint0_linear_105_351" x1="20.5" y1="16" x2="100" y2="200" gradientUnits="userSpaceOnUse"> <stop stop-color="#ACAAFF"/> <stop offset="1" stop-color="#C0E8FF"/> </linearGradient> <clipPath id="clip0_105_351"> <rect width="200" height="200" fill="white"/> </clipPath> </defs> </svg>        
```


## Plans
My next website will be builtl with Astro.