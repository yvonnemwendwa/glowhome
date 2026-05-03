# GlowHome — Salon Booking Web Page

A mobile-style salon booking web page where clients in Nairobi book
a braider who travels to their home.

Built with **TailwindCSS** as part of a Generative AI course project.

---

## Live Demo

https://mellifluous-speculoos-c48e40.netlify.app/

---

## What the page does

- Choose a braiding service (Box braids, Knotless braids, Faux locs, Twist braids)
- Pick an available braider (Joy, Faith, Lydiah, Peace)
- Select a date and time
- Enter your name, home address, and phone number
- Confirm booking — a real email is sent via EmailJS to the salon owner
- Booked braiders are marked unavailable immediately after confirmation

---

## Technologies used

| Technology   | Purpose                                      |
|--------------|----------------------------------------------|
| HTML         | Page structure                               |
| TailwindCSS  | Styling via CDN — no build tools needed      |
| JavaScript   | Interactivity — selections, validation, state|
| EmailJS      | Sends booking confirmation emails            |
| Netlify      | Free deployment                              |
| Python       | Local development server (http.server)       |

---

## How to run locally

### Option 1 — Double click (simplest)
1. Download or clone this repository
2. Open the `glowhome` folder
3. Double-click `index.html`
4. It opens in your browser — done

### Option 2 — Python local server (recommended)
```bash
cd glowhome
python -m http.server 8000
```
Then open `http://localhost:8000` in your browser.

---

## EmailJS setup (to enable real emails)

The page sends booking emails using EmailJS. To connect your own email:

1. Create a free account at https://emailjs.com
2. Add a Gmail service and create an email template
3. Use these exact variable names in your template:
   `{{from_name}}` `{{phone}}` `{{address}}` `{{service}}`
   `{{price}}` `{{duration}}` `{{stylist}}` `{{date}}` `{{time}}`
4. In `index.html`, replace:
   - `YOUR_PUBLIC_KEY` with your EmailJS Public Key
   - `YOUR_SERVICE_ID` with your Service ID
   - `YOUR_TEMPLATE_ID` with your Template ID

---

## Project structure
---

## AI Prompts used

This project was built using Claude (claude.ai) as the primary
learning and development guide. All prompts used are documented
in the PDF toolkit submitted alongside this codebase.

---

## References

- TailwindCSS docs: https://tailwindcss.com/docs
- EmailJS docs: https://www.emailjs.com/docs/
- Netlify Drop: https://app.netlify.com/drop
