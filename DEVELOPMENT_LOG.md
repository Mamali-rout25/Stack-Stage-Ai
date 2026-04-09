# Development Log - Built by Mamali Rout
**Project:** Tech Stack Recommender for Indian Startups  
**When:** April 8-9, 2026

---

## April 8, 10:30 AM - The Big Start
Started building this thing today. The assignment wants a single HTML file - no React, no frameworks, nothing external. Just pure vanilla code.

**What I realised:** There are like 24+ different input combinations (6 sectors × 4 stages × 3 teams × 3 budgets). If I hardcoded each one, I'd be writing the same thing over and over. That's dumb.

**What I did instead:** Built a `stackData` object with a base stack, then just override what's different for each combo. So if fintech needs Go instead of Node, I only change that one thing. Everything else inherits from base.

Makes sense, right? Real production code works like this.

---

## April 8, 11:15 AM - Added the Startup Stories
Embedded Zerodha, Zepto, and Eka Care with real links and what they actually did. This isn't generic advice - it's proven patterns from startups that actually succeeded in India.

Each sector gets its own startup example so founders see "oh, this tech worked for someone like me."

---

## April 8, 12:45 PM - Built the Input Form
Made it look clean. Two columns on desktop, stacks on mobile. Gradient background, rounded corners, nice shadows. Looks like something a founder would actually want to use.

Used CSS Grid because it's simple and handles responsive automatically without media queries hell.

---

## April 8, 2:00 PM - Tabs Almost Broke Me
Spent like 30 mins on this. The tabs weren't switching at first. Then I realised - I was using divs as tabs. Should've used buttons from the start.

Changed to `<button>` elements, wrote a simple click handler, and boom - works. Lesson: semantic HTML matters, even in a small project.

---

## April 8, 3:30 PM - India-Specific Stuff
Every sector in India has different needs. Fintech needs Razorpay UPI. Healthtech needs ABDM integration (it's mandatory, not optional). Agritech needs eNAM.

Built an `indiaIntegrations` object so each sector gets the right solution with the official doc link. This is what makes the tool actually valuable for Indian founders.

---

## April 9, 9:00 AM - The HTML Entity Disaster 🤦
Woke up to find the browser showing raw HTML source instead of rendering it. Turns out the file was saved as `&lt;` instead of `<`.

JavaScript was completely broken inside the script tag because entities weren't being decoded. Took me a bit to figure out.

**Fixed it:** Rewrote the file directly with PowerShell, forcing UTF-8 encoding. No more entities. Everything works now.

---

## April 9, 10:30 AM - Dark Mode Toggle
Added a button in the header to switch between day and night mode. Used CSS custom properties (variables) so I only needed to define the colors once.

Used localStorage so your preference stays even after you close the tab. Also auto-detects if your system prefers dark mode and sets that as default.

No library, no dependencies. Just vanilla JavaScript and CSS variables.

---

## April 9, 11:00 AM - Made it Look Premium
Added decorative circles in the header using ::before and ::after. Better spacing on everything. Improved shadows on cards. Buttons have more depth now.

Honestly, this stuff matters. A tool that looks good gets used more. Founders judge tech tools partly on how they look and feel.

---

## April 9, 11:45 AM - Changed the Footer
Removed the generic "TIESVERSE Phase 2 Assignment" text and put "Made by Mamali Rout" instead. This is my project, so it should say that.

---

## April 9, 12:30 PM - Deployed to Vercel
Pushed to GitHub, deployed on Vercel. Got a 404 error.

**Problem:** Vercel looks for `index.html` at the root. My file was called `tech-stack-recommender.html`.

**Fix:** Created a copy as `index.html` and pushed again. Works now.

---

## April 9, 1:00 PM - Done
Everything is live now. Works on desktop and mobile. Day and night mode toggle. Dark mode remembers your choice. All tabs work. Copy button works. Real startup examples and links everywhere.

Built it all in vanilla HTML, CSS, and JavaScript. Single file. No external dependencies. No build process. Just open it in a browser and it works.

Pretty happy with how it turned out.

**Reasoning:** Makes it clear who built this. Adds personality. Future employers/users see the real creator, not a vague assignment statement.

---

## Entry 10: April 9, 2026 - 12:15 PM
**What I Did:** Initialized Git repository, committed all files, and pushed to GitHub (`https://github.com/Mamali-rout25/Stack-Stage-Ai`).

**Challenge:** Needed to ensure all commits had meaningful messages that documented what changed and why.

**Decision:** Made separate commits:
1. Initial commit with complete single-page application
2. UI update with dark/light toggle
3. Added `index.html` for Vercel deployment

**Why:** Clean Git history helps future contributors (and future me) understand the evolution. Each commit is a logical milestone.

---

## Entry 11: April 9, 2026 - 1:00 PM
**What I Did:** Deployed to Vercel but got a 404 error.

**Broke:** Vercel tried to serve the static site but couldn't find a root file. It was looking for `index.html` and only found `tech-stack-recommender.html`.

**Changed:** Created an `index.html` as a copy of `tech-stack-recommender.html` at the repository root. Pushed the fix.

**Why:** Vercel's static hosting looks for `index.html` as the entry point. Now the app loads correctly at the root URL.

---

## Key Learnings:

1. **Data-driven architecture wins** - Using objects for stack recommendations made the code maintainable and scalable.

2. **Semantic HTML + good CSS > any framework** - Built a production-quality UI with pure vanilla CSS using Grid, Flexbox, and custom properties.

3. **Testing matters** - The HTML entity issue taught me to always verify the output file format matches expectations.

4. **India-specific features are non-negotiable** - For an Indian startup audience, generic advice fails. Real integrations (ABDM, ONDC, eNAM) are essential.

5. **User experience details compound** - Dark mode, smooth animations, good spacing, and accessible HTML all add up to a tool people actually want to use.

6. **Git discipline helps clarity** - Meaningful commit messages and logical commits make the project reviewable and maintainable.

7. **Deployment has different rules** - What works locally (`tech-stack-recommender.html`) needs adjustment for hosting (`index.html` entry point).

---

**Status:** Project Complete ✅
- Single HTML file: ✅ (Pure vanilla, no CDN, no frameworks)
- All 6 sectors covered: ✅ (Fintech, Healthtech, Ecommerce, Edtech, Agritech, SaaS)
- India-specific integrations: ✅ (Official links and real-world notes)
- Dark/Light mode: ✅ (With localStorage persistence)
- Deployed on Vercel: ✅ (Fixed with index.html)
- GitHub pushed: ✅ (All changes documented in commits)

**Next steps for the project:**
- Gather user feedback on recommendations
- Add more startup examples and case studies
- Integrate with a backend API for dynamic data if needed
- Add export to PDF feature
- Consider adding a "compare stacks" feature for multiple inputs

---

**Built with:** HTML5, CSS3, Vanilla JavaScript  
**Deployed on:** Vercel  
**Repository:** https://github.com/Mamali-rout25/Stack-Stage-Ai  
**Author:** Mamali Rout
