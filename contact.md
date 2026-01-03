---
layout: page
title: Contact
permalink: /contact
---

<p>{{ site.contact_page_description }}</p>

<form class="contact-form" action="https://formspree.io/f/mnjngzza" method="POST">
  <div class="form-item">
    <label class="form-label" for="name">Name <span>(required)</span></label>
    <input type="text" name="name" id="name" required>
  </div>
  <div class="form-item">
    <label class="form-label" for="email">Email <span>(required)</span></label>
    <input type="email" name="email" id="email" required>
  </div>
  <div class="form-item">
    <label class="form-label" for="message">Message <span>(required)</span></label>
    <textarea name="message" id="message" class="form-textarea" required></textarea>
  </div>
  <button type="submit" class="btn">Send Message</button>
</form>
