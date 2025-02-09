---
layout: post
title:  "Cheap blogging with Github Pages"
date:   2025-02-09 23:43:33 +0700
categories: jekyll github
---
Personal blogging site might be extinct in few years but if you're looking for no-cost blogging platform, Github Pages is an excellent option. Despite the zero cost, it still allow some level of control on the platform while also provides great performance, mainly from of the use of static site generator (SSG).
Here's a step-by-step guide to setting up GitHub Pages for your blog with a custom domain.

**1. Create repository:**

* Repository must be the same with your username and it will ends up as default domain name for your Github Pages site, e.g. yourusername.github.io
* Public repostitory is required for Github Pages.

**2. Choose Static Site Generator**

Using an SSG simplifies blog creation and improves pages performance. While many SSG is available out there, **Jekyll** is supported natively by Github Pages, so you should pick it unless you feel adventurous. You don't want to edit files directly in Github, so for development, you need to setup Jekyll in your local machine by refering to the docs https://jekyllrb.com/docs/.

**3. Customize your blog**
Once you setup SSG, you need to modify it first, whether the theme or your first blog post! In case of Jekyll, you can explore the generated files especially these files:
* `_config.yml` stores the Jekyll configurations. You can check the full guide on https://jekyllrb.com/docs/configuration/.
* `_posts/` will be your blog post folder. Please refer to https://jekyllrb.com/docs/posts/ on how to manage posts.
* `index.md` is the home page. Read more about pages here https://jekyllrb.com/docs/pages/.

**4. Push your blog files to GitHub and configure Github Pages**

* Push you repository to Github if you haven't.
* In your GitHub repository, go to "Settings."
* Scroll down to "Pages."
* For "Branch," select the `main` branch and the `/ (root)` folder.
* Click "Save."

**6. Set up your Custom Domain (optional)**

* **Add your domain:** In the "Pages" section, add your custom domain (e.g., `www.yourdomain.com` or `blog.yourdomain.com`) in the "Custom domain" field and click "Save."
* **Create DNS records:** In your domain registrar, create two DNS records:
    * **A record:** Point `yourdomain.com` (or subdomain) to GitHub's IP address: `185.190.108.153`.
    * **CNAME record:** Point `www.yourdomain.com` to `yourusername.github.io`.

**7. Profit!**

It might take few mins for Github to build your pages and few hours for your DNS to be propagated. This blog is built the same way and I only pay for the domain. Happy blogging!