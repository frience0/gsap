GSAP 2025 Website
A modern, interactive website showcasing high-performance animations built with the GreenSock Animation Platform (GSAP) version 3.13. This project leverages GSAP's free core library and bonus plugins, such as ScrollTrigger and SplitText, to create engaging scroll-based and interactive effects.
Features

Smooth scroll-triggered animations using GSAP's ScrollTrigger plugin
Text animations with SplitText for dynamic headline effects
Responsive design optimized for all major browsers
Lightweight and performant, built with vanilla JavaScript and GSAP
Easy-to-customize structure for developers

Prerequisites

Node.js (v16 or higher) for local development
A modern web browser (Chrome, Firefox, Safari, Edge)

Installation

Clone the repository:git clone https://github.com/your-repo/gsap-2025-website.git

Navigate to the project directory:cd gsap-2025-website

Install dependencies (for local server and build tools):npm install

Include GSAP via CDN or npm:
Via CDN in index.html:<script src="https://cdn.jsdelivr.net/npm/gsap@3.13/dist/gsap.min.js"></script>

<script src="https://cdn.jsdelivr.net/npm/gsap@3.13/dist/ScrollTrigger.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/gsap@3.13/dist/SplitText.min.js"></script>

Or via npm:npm install gsap

Then import in your JavaScript:import gsap from 'gsap';
import ScrollTrigger from 'gsap/ScrollTrigger';
import SplitText from 'gsap/SplitText';
gsap.registerPlugin(ScrollTrigger, SplitText);

Usage

Start a local development server:npm start

This will open the website in your default browser (e.g., http://localhost:3000).
Customize animations in src/js/main.js:
Example ScrollTrigger animation:gsap.to('.hero-section', {
opacity: 1,
y: 0,
duration: 1,
scrollTrigger: {
trigger: '.hero-section',
start: 'top 80%',
end: 'bottom 60%',
scrub: true,
},
});

Example SplitText animation:const split = new SplitText('.headline', { type: 'words' });
gsap.from(split.words, {
y: 50,
opacity: 0,
stagger: 0.05,
duration: 0.8,
});

Edit styles in src/css/styles.css for visual customization.
Build for production:npm run build

Output will be in the dist folder.

Project Structure
├── dist/ # Production build
├── src/
│ ├── css/ # Stylesheets
│ ├── js/ # JavaScript files
│ └── index.html # Main HTML file
├── package.json # Project dependencies and scripts
└── README.md # Project documentation

Resources

GSAP Official Documentation - Learn GSAP fundamentals and plugin usage.
GSAP Showcase - Inspiration from top GSAP-powered websites.
Webflow GSAP Integration - Details on GSAP's free availability.
GSAP GitHub Repository - Source code and licensing info.

License
This project is licensed under the MIT License. GSAP is free for commercial use under GreenSock's standard "no charge" license: GSAP License.
Acknowledgments

Built with GSAP 3.13, now 100% free thanks to Webflow.
Inspired by the GSAP community and showcases like Flowfest 2025.
