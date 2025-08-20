---
# You can also start simply with 'default'
theme: default
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: /assets/intro.jpg
# some information about your slides (markdown enabled)
title: Software Development | Foundations
info: |
  ## Software Development | Foundations
# apply unocss classes to the current slide
class: text-left
drawings:
  persist: false
transition: slide-left
mdc: true
---

# Intro to Deployment
Unit 07 - Lesson 04

- [ ] Buying a Domain Name
- [ ] Connect our Domain Name to our app
- [ ] DNS servers: Recursor, Root, TLD, and Authoritative
- [ ] Lab: PHP continued, Input Validation, Edit and Delete functionality

<div class="abs-br m-6 text-xl">
  <a href="https://github.com/slidevjs/slidev" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

<!--
-->

---
transition: slide-left
---

# Recap

- career lab tmrw + tech lab tmrw at the same time
  - attend career lab first, then once finished come to the tech lab
  - I will record PHP's Input Validation, Edit/Delete functionality during the time you're at career lab, (or save that material for another class)
  - Once career lab is finished and you're back to tech lab we can either do AMA, and/or go over the [Getting Started page with Docker](https://www.docker.com/get-started/)
- For this class, get your credit card ready (if you wish), Buy a cheap domain name (I use namecheap.com) so we can practice connecting our Render apps to a legit domain
  - we'll go over the steps on how to buy a domain name
  - reminder: Github Education Pack gives a free `.me` domain for 1 year
- will mark Weather App assignments over weekend

---
transition: slide-left
---

# Buying a Domain Name

- Options to buy domain name include: [Namecheap](https://www.namecheap.com/), [Hover](https://www.hover.com/), [Porkbun](https://porkbun.com/), [Cloudflare](https://www.cloudflare.com/en-au/products/registrar/)
- Search for a domain name you want to buy > Search

<img src="/assets/namecheap1.png" />

---
transition: slide-left
---

# Filter possibilities

- Click Beast mode to get additional filters. Filter from $0 to $5 > Select All **TLDs** > Generate

<img src="/assets/namecheap2.png" />

---
transition: slide-left
---

# Add to Cart

- Compare with other Domain Name registrars to see who has the better deal
- Once domain name is identified that you wish to buy, click Add to Cart 
<img src="/assets/namecheap3.png" >

---
transition: slide-left
---

# Checkout

- Select: how many years? auto-renew? Ensure you have Domain Privacy
- Confirm Order (need to Login/Create Account + verification code)

<img src="/assets/namecheap4.png" >


---
transition: slide-left
---

# Enter Credit Card Details, Pay Now

- After you enter Credit Card Details > Pay Now
<img src="/assets/namecheap5.png" >


---
transition: slide-left
---

# Purchase Summary

- Congrats you've purchased your first domain name!
- Now Click Manage
<img src="/assets/namecheap6.png" >

---
transition: slide-left
---

# Enter Name Servers

- `my-awesome-app.info`, won't work yet; need a way point to which servers have the answer
- Can get name servers from where we hosted our frontend (ex: Netlify, Render etc.)
<img src="/assets/namecheap7.png" >

---
transition: slide-left
---

# Add Domain you already own

- Click "Add or register domain" > select "Add a domain you already own"
<img src="/assets/netlify7.png">

---
transition: slide-left
---

# Add a Domain to Netlify DNS

- Click Continue
<img src="/assets/netlify5.png" style="height: 400px">

---
transition: slide-left
---

# Find Name Servers info

- Copy the name server values which we will paste in namecheap one at a time
<img src="/assets/netlify6.png" style="height: 300px">

---
transition: slide-left
---

# Paste values into NameCheap

- Choose Custom DNS in dropdown and Paste all 4 values
<img src="/assets/namecheap8.png">

- Click green checkmark to save > will get message but in reality will probably see results in less than 1 hour
<img src="/assets/namecheap9.png">



---
transition: slide-left
---

# Point our project to our domain

- In Netlify's case click "Go to Domain Management"

<img src="/assets/netlify1.png" >

---
transition: slide-left
---


# Add a domain

- Click Add a domain > Add a domain you already own

<img src="/assets/netlify2.png">

---
transition: slide-left
layout: two-cols
---

# Add Custom Domain 
1. Enter your custom domain name > click Verify
<img src="/assets/netlify3.png">

::right::
2. then click Add domain
<img src="/assets/netlify4.png">

- Periodically check https://my-awesome-app.info to see if it worked!


---
transition: slide-left
---

# Domain Name System (DNS)

- A name server is a part of the Domain Name System (DNS), which is like the internet's phone book
- Its job is to translate human-readable domain names (like yourdomain.com) into IP addresses (like 192.0.2.1)

<img src="/assets/dns.png" style="height: 350px">

---
transition: slide-left
---

# IP Addresses

- An IP address (Internet Protocol address) is a unique identifier assigned to each device connected to a network (like the internet). It works like a home address, allowing devices to send and receive data.
- There are two main versions:
  - IPv4, ex: 192.168.1.1, Size: 32 bits, Allows 4.3 billion unique addresses
  - IPv6, ex: 2001:0db8:85a3:0000:0000:8a2e:0370:7334, Size: 128 bits, Allows 3.4×10³⁸ addresses
<img src="/assets/ip.webp" style="height: 300px">

---
transition: slide-left
---

# How IP Addresses Work (Routing Basics)
- When you send a request (e.g., visit a website), your device uses its IP address to communicate.
- DNS translates domain names (like example.com) into an IP address.
- Routers use IP addresses to forward packets through the internet to the correct destination.
- The receiving device sees your IP address and sends a response back.
<img src="/assets/network.webp" style="height: 300px">

---
transition: slide-left
---

# TCP/IP Layers

<img src="/assets/tcpip.png" style="height: 450px">

---
layout: image-right
transition: slide-left
image: /assets/break.png
backgroundSize: 400px 300px
class: text-left
---

# 10 minute break

🍦 Cool Tips, Trends and Resources:
- 🏖️ [PHP Sandbox](https://phpsandbox.io/)
- ▶️ [Playlist: Me teaching PHP/mySQL at Georgian](https://www.youtube.com/playlist?list=PLhbE5nKJVCT--FKzucu-5gvjQparwTna7)
- 💻 [DNS server types](https://www.cloudflare.com/learning/dns/dns-server-types/)
- 🍁 [What is a CDN](https://www.cloudflare.com/learning/cdn/what-is-a-cdn/)
- 🌱 [Concept of DNS Simplified](https://x.com/thebitdoodler/status/1418951041568022528)

<br>
<hr>
<br>

- 🧪 [Enter anonymous lab questions](https://docs.google.com/forms/d/e/1FAIpQLSevvGARdHQikso-uLqFCO481MABKE5HofuSrlzEPMNQ2ZLykw/viewform?usp=dialog)
- ℹ️ [Course feedback survey](https://circuitstream.typeform.com/to/ZoyYk7px#course_id=SoftwareAN&instructor=9514)

---
transition: slide-left
---

# DNS server types

- Recursive resolver
  - (aka DNS recursor) is the first stop in a DNS query
  - responds with either cached data, or send a request to a root, TLD, authoritative nameserver
- Root nameserver
  - receive query for domain name, and responds by directing to TLD nameserver
- TLD nameserver
  - maintains info for all ".com" domain names for example, responds with authoritative nameserver
- Authoritative nameserver
  - the last step in the journey for an IP address lookup
  - contains info specific to the domain name and responds with IP address



---
transition: slide-left
---

# What is a CDN?

- CDN is a network of servers linked together with the goal of delivering content as quickly, cheaply, reliably and securely as possible
- to be performant, CDN will place servers at strategic locations (at highly interconnected locations)

<img src="/assets/cdn.png" style="height: 300px" >

---
transition: slide-left
---

# Deploy Node/Express/Vite app on Render

- Other options to deploy: AWS, Fly.io, Railway, Azure
- Change DB connection string to be an environment variable
- Deploy step-by-step, test that frontend communicates with backend api

---
transition: slide-left
---

# Lab: Serverless

- read https://www.netlify.com/blog/intro-to-serverless-functions/
- let's try to deploy a serverless function
- create a voting app that calls an API (i.e. serverless function) and draws a dynamic chart based on live votes


---
transition: slide-left
---

# Lab  
PHP continued: Server-side validation on blank fields

- Problem: On the input form try entering a bunch of space characters for the game title
- Problem: user can inspect DOM and remove `required` attributes or add `novalidate` to form tag to bypass client-side validation
- After extrapolating POST variables and before our `$sql` statement:
```php
// Validation #1: Prevent blank fields.  Use https://phpsandbox.io/ to test
$is_form_valid = true;

if (empty(trim($title)))) {
  echo "Please enter a title";
  exit; // temporarily can exit just to test if above works.  remove it after.
  $is_form_valid = false;
}

if ($is_form_valid) {
  // go ahead with all the SQL code all the way until echo "Game Saved?"
}
```

---
transition: slide-left
---

# PHP: Server-side Validation on year field

- Problem: try entering alphabetic characters in the year field
- Problem: try entering -000123 in the year field
- Solution: 
  - use [sanitize filters](https://phpdoctest.github.io/en/filter.filters.sanitize.html)
  - use [validate filters](https://www.php.net/manual/en/filter.constants.php#constant.filter-validate-bool)

```php
// replace our $year = $_POST['year'] with:
$year = filter_var($_POST['year'], FILTER_SANITIZE_NUMBER_INT); 
// can test above with values: "2021", "asdf", "-00123"

$year_regex = "/[0-9]{4}";

if ($year < 0 || strlen($year) != 4 || !preg_match($year_, $year)) {
  echo "PLease enter a valid year";
  $is_form_valid = false;
}
```

---
transition: slide-left
---

# PHP: Sanitize Input against XSS injection

- Problem: try entering `<h1>Frogger</h1>`
- Problem: try entering `<script>alert("hacked")</script>`

```php
// replace our $_POST statements with all our string inputs
$title = filter_var(trim($_POST['title']), FILTER_SANITIZE_STRING);
$genre = filter_var(trim($_POST['genre']), FILTER_SANITIZE_STRING);
$url = filter_var(trim($_POST['url']), FILTER_VALIDATE_URL);
```

---
transition: slide-left
---

# PHP: Delete functionality

---
transition: slide-left
---

# PHP: Edit functionality
