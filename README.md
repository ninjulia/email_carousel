# Advanced Email: Carousel and Thumbnails
## Email Code | Progressive Enhancements

### Introduction

Email coded to showcase carousel and thumbnail functionality.  Design based on Adidas' "50% OFF! Black Friday Drops Now" email as seen on [Really Good Emails](https://reallygoodemails.com/emails/50-off-black-friday-drops-now). The email was originally sent in November 2016.

Images and code are modified from the original Adidas email. The images used here are courtesy of [placeimg.com](https://placeimg.com/) and used under [Creative Commons Licence](https://creativecommons.org/). Otherwise, all copyrights remain in control of their respective owners. 

The email showcased here was coded from scratch utilizing my email boilerplate framework (developed from Email on Acid and Litmus.com samples as a starting point). In addition to the advanced functionality, I added support for dark mode and tested for email clients post-2016.

### Advanced Email Functionality

I coded the advanced carousel and thumbnail functionality while referencing the [Email on Acid Tutorial: Animated Image Carousel for Email](https://www.emailonacid.com/blog/article/email-development/tutorial-animated-image-carousel-for-email/) and [Email on Acid Tutorial: Interactive Quiz](https://www.emailonacid.com/blog/article/email-development/how-to-build-an-interactive-quiz-in-email/). The effect will only work in email clients that support CSS Animations and the Interactive Checkbox Technique - aka the "checkbox hack." Supported clients are Webkit-based - iOS Mail (iPhone, iPad), Apple Mail, and Outlook for iOS and Mac. All other clients display fallback content of a hero image with a link through to the landing page (not linked in this example). 

### A Note About Outlook.com

While Outlook.com (Office365.com, Hotmail.com) passes the webkit support check, it does not render the carousel feature as expected.  Carousel images are displayed stacked in a veriticle layout. In some situations, this might be an acceptable fallback effect. Here, the solution was to target owa specifically applying the following css to the advanced layout: 

    [owa].hideme {
        display: none !important; 
        font-size: 0; 
        height: 0; 
        overflow: hidden; 
        mso-hide: all !important;
    }   

### Test Results

-[Email on Acid Test:](https://app.emailonacid.com/app/precheck/display/summary/z0xaudyYs8)