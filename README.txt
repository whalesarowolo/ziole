Ziole website prototype source

Files
- style.css: complete reusable visual stylesheet (plain CSS, no build required).
- index.html: shared page shell, header and footer.
- app.js: page markup, demo content and browser interactions.
- forest.jpg: prototype hero image.

Preview
Extract the ZIP, then open index.html in a browser. Internet access is needed for the Google Fonts import; system fallback fonts work offline.

Wagtail integration
1. Copy style.css to your Django app at static/css/ziole.css.
2. In your shared base template, load static and link the stylesheet:
   {% load static %}
   <link rel="stylesheet" href="{% static 'css/ziole.css' %}">
3. Copy forest.jpg to static/images/forest.jpg for initial use, or upload it to Wagtail Images for editable content.
4. Reuse the HTML classes from index.html and the template strings in app.js in your Django templates.
5. Replace hash links such as #/services with Wagtail page links.
6. Replace hard-coded text with Wagtail fields.

Important
The prototype renders its page content through app.js. index.html alone does not contain the homepage sections. Use app.js as a markup reference, then replace its router with Wagtail templates. Do not include the complete app.js in a Wagtail site: it replaces main content and intercepts navigation. Reimplement only needed interactions such as the mobile menu and conditional form fields.
Forms are demo-only and do not send or store information. Articles and professional details are illustrative or awaiting verification. The stylesheet imports DM Sans and Libre Caslon Display from Google Fonts; review production font hosting and privacy requirements. The photograph is a prototype asset from Unsplash (photo-1441974231531-c6227db76b6e); review its source and intended production use.
