Blogger Contempo Light Theme — Light/Dark Mode Exploration
===============================================
This repository explores adding light/dark mode support to the Blogger Contempo Light theme.
The goal is to enhance the user experience by allowing visitors to automatically switch between light and dark modes based on their system settings.

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

By default, the 'Follow System Light/Dark Mode Setting' feature is turned off. To enable it, click the 'Appearance Mode' menu entry you added in step 6, then check 'Follow System Light/Dark Mode Setting' in the modal dialog that appears, and click OK. 

In the same dialog, you can also choose to show a floating button at the bottom right of the window (it is turned off by default). Once the floating button is visible, you can click it anytime to reopen the Appearance Mode dialog. 

When 'Follow System Light/Dark Mode Setting' is turned on, the blog will:
- use dark mode colours when the system setting is dark mode.
- use theme's original colours when the system setting is light mode.

More details about this experimental/exploratory work can be found in my blog post: [Blogger Contempo Light Theme: Challenges involved in providing light/dark mode support](https://raviswdev.blogspot.com/2025/10/contempo-light-theme-dark-mode.html).

Author & Initial Publication Date
-------------------------------
Ravi S. Iyer with assistance from ChatGPT.  
First published: 25 October 2025

License
----------------
This code is provided under the MIT License. See the LICENSE file for details.
