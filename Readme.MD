Blogger Contempo Light Theme Light/Dark Mode Exploration
===============================================
This repository contains an exploration of implementing light/dark mode support for the Blogger Contempo Light Theme. The goal is to enhance user experience by allowing users to switch between light and dark modes based on system settings.

The code is experimental/exploratory and uses a simple approach of changing colours using the universal selector * at a top level. This has the risk of tripping up some features of the theme. It has been tested only with test blogs including test/demo blog given below. I am not using it for my regular Blogger blogs, as of now at least.

**[Contempo Theme Toggle Light/Dark Test/Demo Blog](https://contempo-ld.blogspot.com/)**


Steps to implement this feature
-----------------------------------------------
1. Save your current them by Theme -> Customize (dropdown) -> Backup.
2. Access the Theme HTML editor by navigating to Theme -> Edit HTML.
3. Add the contents of the file JustBeforeEndHead.html to just before the closing `</head>` tag in your theme's HTML.
4. Add the contents of the file JustBeforeEndBody.html to just before the closing `</body>` tag in your theme's HTML. You may have to follow any instructions in JustBeforeEndBody.html code to replace && by `&amp;&amp;` in the added code to avoid Blogger Theme HTML editor errors.
5. Save the changes to your theme.
6. To add a menu entry for toggling appearance mode: In Layout, in a Pages gadget (add it if not already present), add a page with following details:
    - Page name: Appearance Mode
    - Page URL: javascript:openModal(false)
7. Save the layout changes.

Now you can test the blog's light/dark mode support. 

By default, the 'System Dark Mode Support' feature is disabled. To enable it, click on the 'Appearance Mode' menu entry you added in step 6, and choose Enable under 'System Dark Mode Support' in the modal dialog that appears followed by OK. 

In the above dialog, you can also choose to show an icon button at bottom right of window (by default it is set to hide). Once the icon button is shown, you can click on it to show the appearance mode dialog again.

When 'System Dark Mode Support' is enabled, the blog will:
- use dark mode colours if the system setting is dark mode.
- use theme's original colours if the system setting is light mode.

More details about this experimental/exploratory work can be found in my blog post: [Blogger Contempo Light Theme: Challenges involved in providing light/dark mode support](https://raviswdev.blogspot.com/2025/10/contempo-light-theme-dark-mode.html).

Author & Initial Publication Date
-------------------------------
Ravi S. Iyer with assistance from ChatGPT.  
First published: 25 October 2025

License
----------------
This code is provided under the MIT License. See the LICENSE file for details.
