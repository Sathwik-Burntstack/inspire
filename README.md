# Inspire Educational Institutions — Premium Website

## Start the website

Run `npm install` once, then `npm run dev` (or `npm start`) inside the project folder and open `http://localhost:5500`. The site is static and has no npm dependencies; `package.json` provides both run commands and ensures npm recognizes this folder as the project root.

No npm dependencies need downloading. Files: `index.html` (content), `style.css` (design/animations), `app.js` (form/navigation/gallery), `assets/posters` (nine original uploaded posters converted to JPEG), `assets/videos` (nine supplied videos), and three classroom scene recreations based on the user-provided screenshots. Replace `assets/classroom-mentor.jpg`, `assets/small-group-learning.jpg` and `assets/outdoor-study.jpg` with the original photo files before public launch for pixel-accurate representation.

## Enquiry popup and lead capture

The popup opens after 4.8 seconds. It repeats after refresh unless a **backend confirms successful saving**. Form fields: parent name, phone, student class, subject and preferred time.

**Demo mode:** The form opens WhatsApp with a prefilled message to +91 99123 42261. The parent must press **Send** in WhatsApp. Without a backend, no form entry is automatically saved; the popup continues appearing on later refreshes. This prevents falsely promising lead storage.

**Production mode:** Set `LEAD_ENDPOINT` at the top of `app.js` to your own same-origin API URL that accepts POST JSON and returns `{ "status": "success" }` only after a durable save. The site then stops showing the automatic popup for that browser after a successful response. Build the API using Netlify Functions, Vercel Functions or your own server, with server-side credentials, validation, rate limits and spam protection. Your API can save to Google Sheets and send an email alert. Do not put private API keys in frontend JavaScript. Test the end-to-end process before launch.

## Business information used

Name: Inspire Educational Institutions / Learn to Lead. Established: 2013. Home-based tuition: students attend at the tutor's home. Address: East Marredpally, opposite HMWS Water Tank, behind Shenoy Hospital, Secunderabad – 500026. Phone: 9912342261 / 9912342265. Classes 3–10, Intermediate MPC/BiPC/MEC/CEC. Evening timings shown in posters: 5:30–7:30 PM and 6:00–8:30 PM.

## Confirm before public launch

- Actual teacher name, photo, qualification, and teaching experience (not provided). Do not invent a tutor profile.
- Google rating, reviews, review permissions and real student results (not verified). No invented testimonials are used.
- Whether a demo class is free, and current batch timings, fees, subjects and seats.
- Cambridge/IB availability and whether online or at-student-home classes are offered.
- Which number receives WhatsApp and automated lead alerts. Current WhatsApp links use 9912342261.
- Exact Google Maps pin and permission to publish identifiable classroom/student photos.
- Privacy notice and production spam protection.

The supplied Justdial and Claude URLs could not be automatically read. The website uses the user-supplied promotional images, videos and the seven-page development brief. The wordmark is rendered as text with a decorative symbol, rather than pretending to be the exact original logo. Replace it with the official transparent logo when provided.

## Publish

Deploy the whole folder to a static host (Netlify, Vercel, GitHub Pages). Add your live domain to the verified Google Business Profile. The website includes local SEO metadata and structured data; ranking is not guaranteed. Keep the video files because they are displayed in the gallery; videos load on demand.
