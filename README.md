# Retail Services — Static Web App

This is the MVC-to-static conversion.

## Main changes
- Products page retained.
- Cart replaced with a modern **Place an Order** page.
- Cart/order selection uses browser `localStorage`.
- Order page includes an order summary + Microsoft Forms embed area.
- Modern glassmorphism UI, gradients, hover effects, reveal animations, responsive navigation and scroll progress.
- MVC controllers, Razor views, sessions, SMTP and Azure Table/Blob order storage are removed from the frontend.

## Microsoft Forms
The Order page is already connected to the supplied Microsoft Forms embed URL.

If you want the form to receive the selected products automatically, Microsoft Forms' cross-origin iframe prevents the site from filling its fields directly. The page therefore provides a **Copy** button so the customer can paste the generated order summary into an Order Details field.

## Images
The current image URLs still point at the existing Blob URLs because the uploaded MVC project did not contain local copies of those images. Once you have the local images, put them in `assets/images/` and update the three product image URLs in `assets/js/site.js`, plus the gallery image URLs.
