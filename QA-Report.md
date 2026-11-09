# Conquest Literary Media — redesign handoff

Prepared November 10, 2026. This is a static frontend redesign. The production website has not been modified or deployed.

## Included

29 HTML pages: every page discovered in the original main navigation and XML sitemaps, plus dedicated For Authors, Portfolio, Resources, and Privacy Policy pages. The original privacy policy was presented in a popup; it now has its own route. The sitemap-discovered manuscript-submission page, empty journal post, category archive, and author archive are retained. See route-inventory.json for the full list.

Shared black, ivory, and gold design system; cinematic workspace hero; original company logo; sticky navigation; two-line mobile toggle that transforms to an X; service dropdowns; three service introduction treatments; editorial content; native expandable FAQ and publishing-guide sections; modest entrance animations; reduced-motion support.

All seven service-detail pages retain their original substantive text. About, Blog / Insights, client reviews, 20 FAQs, six publishing-guide steps, and privacy-policy text were carried forward. Homepage and service-directory copy was edited for the new presentation. Original reviews are reproduced as company-published reviews; their authenticity has not been independently verified. Empty author and portfolio collections remain honest empty states. No fictional books, authors, outcomes, or statistics were added.

Manual email forms are provided for contact, manuscript inquiries, and client experiences. They validate required fields, prepare an encoded mailto URL, retain entered data, and provide a copy fallback. Long messages use the copy fallback to avoid mail-client URL limits. No backend, tracking code, email API, or form persistence is included. No messages were sent during testing.

## Verification completed

- Generated 29 pages; checked all local HTML links and referenced files: no missing destinations.
- Confirmed one H1 per page, document language, viewport metadata, titles, descriptions, canonical URLs, Open Graph fields, and a sitemap.
- JavaScript syntax check passed.
- Automated form checks passed: recipient, subject, Unicode, ampersands, question marks, hash signs, multiline content, validation gate, retained fields, copy behavior, and long-message fallback.
- Browser-reviewed desktop homepage, mobile homepage at 390px, and tablet contact layout at 768px.
- Browser-tested mobile menu and service dropdown; sticky header stays outside the scrolling drawer.
- Browser-tested service preselection and Copy Email Details. The browser denied clipboard access and the selectable-text fallback worked correctly.
- Browser-tested the self-contained preview, route navigation, and FAQ disclosure.
- Verified required form labels, native email validation, consent checkbox, keyboard focus styling, skip link, Escape handling, and reduced-motion CSS. This is not a formal accessibility certification.

## Required manual checks before production

1. Test opening the email application on Windows, macOS, iOS, and Android with a configured default mail client. The browser test did not open a real mail app or send mail.
2. Review the retained business details, policy, and company-published reviews. No verified social profile URLs were available in the inspected source, so no guessed social links were added.
3. Test representative pages in Safari and Firefox and on physical mobile devices. No Lighthouse/Core Web Vitals lab run or comprehensive screen-reader audit was performed.
4. Google Fonts loads the chosen serif and sans-serif families. System fonts remain available when offline. Images, CSS, and JavaScript are included locally.
5. Canonicals and sitemap target conquestliterarymedia.com. Change these if the final deployment uses another domain. Root and subdirectory hosting use relative links; clean directory URLs require a host that serves index.html within directories.
6. No original WordPress source repository was attached. This deliverable is a standalone static frontend, not an installed WordPress theme. Existing live admin features and infrastructure are untouched.

## Opening the files

For the portable preview, open Conquest-Website-Preview.html. All 29 pages and local images are embedded in that file; navigate using the menus. The preview iframe adds a wrapper for portability.

For the editable website, extract the ZIP and open index.html, or serve the extracted directory using a static web server. Edit style.css and script.js to change shared styling and interactions. No build dependencies or compilation are required.
