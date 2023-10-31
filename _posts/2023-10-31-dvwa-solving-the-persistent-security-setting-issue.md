---
layout: post
title: "Mastering DVWA: Solving the Persistent Security Setting Issue"
categories: metasploitable
---

**Introduction:** As aspiring ethical hackers and web security enthusiasts, we often delve into platforms like DVWA (Damn Vulnerable Web Application) to sharpen our skills. However, DVWA sometimes presents us with intriguing challenges beyond the vulnerabilities it was designed to showcase. One such puzzle is the persistent issue of security settings reverting to 'high' after we set them to 'low.' In this blog, we'll explore this issue and provide a step-by-step guide on how to solve it effectively.

**The Perplexing Problem:** Imagine you're all set to explore the security vulnerabilities in DVWA, and you decide to lower the security settings to make the environment more permissive for your tests. You navigate to the upload page, switch the security to 'low,' but as soon as you go back to that page, it mysteriously reverts to 'high.' What's going on?

**Understanding the Root Cause:** This seemingly confounding issue is often attributed to the way DVWA manages session data, primarily through cookies. DVWA, like many web applications, uses cookies to store information related to your session, including your security setting.

**The Solution Journey:** Let's embark on the journey to resolve this issue.

**1. Examine Cookies:** Start by opening your browser's developer tools and inspecting the cookies associated with DVWA. Look for cookies that might control the security settings.

**2. Edit the Cookie:** If you find a relevant cookie, try editing it. Change the value from 'high' to 'low.' However, proceed with caution when manipulating cookies, as this approach might not work for all web applications and could have unintended consequences.

**3. Session Variables:** In some cases, the security settings are controlled by session variables stored on the server rather than in cookies. To address this, you'll need to dig into DVWA's code to locate where these session variables are set and make the necessary adjustments.

**4. Browser Extensions:** Browser extensions designed for web security testing, such as Burp Suite or OWASP ZAP, are invaluable in situations like this. These tools provide more control and flexibility for manipulating cookies and other request parameters.

**5. Save Changes:** After modifying the cookie or session variable, remember to save your changes. Then, reload the DVWA page or revisit the upload page to confirm that the security setting remains 'low' as expected.

**6. Testing and Verification:** To ensure that the issue is resolved, try uploading your exploit after setting the security level to 'low.' Verify that the setting remains 'low' on the upload page.

**Conclusion:** Solving the persistent security setting issue in DVWA can be a rewarding exercise in problem-solving and understanding web application behavior. By following the steps outlined in this guide, you can gain more control over the environment and conduct thorough security testing while respecting the ethical principles that guide the world of cybersecurity. Happy hacking!
