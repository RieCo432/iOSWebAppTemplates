Creating iOS web apps can be very error prone.  The size requirements for icons and splash screens are odd and there are a few things that are non-obvious (e.g. the iPad landscape splash image is actually a portrait-shaped image but has it's contents rotated; Retina displays reserve 40 pixels for the status bar while non-retina reserve 20 pixels, etc.).  Also, if you screw something up, you get no errors.  It just simply doesn't work leaving you to guess/hack.

What started as a 15 minute attempt to get icons and splash screens working for my web app resulted in a couple of hours of what felt like pure hacking.  Many of the online resources (including Apple's!) were out of date and didn't include information on handling iPad retina icons/images.  I decided to share my results to hopefully spare others from the frustrating experience.

Fun facts:
<ul>
<li>iPhones don't need a landscape splash screen.  The apps always display a portrait splash image regardless of orientation.  The app itself will turn landscape as expected, but it always launches as portrait.</li>
<li>The iPad landscape splash screen is a weird thing -- it actually requires a portrait-shaped image with rotated content so if you view it in any image viewer, it will appear 90 degrees rotated. (see the sample images in the repo)</li>
<li>My examples use square images and allow the device to add the rounded corners and the lighting highlights. I think it looks far better than any attempt I would make.  See the <a href="http://developer.apple.com/library/ios/#documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html">Apple docs on configuring web apps</a> for information on how to precompose your icon's rounded corners and reflections.</li>
</ul>

<h2>webapp1-plain</h2>
The <strong>webapp1</strong> template is a simple web app that has icons and splash screens that has been tested on an iPhone 3Gs, iPhone 4, iPhone 4s, iPad 1, iPad 2, and the "new iPad (retina).

You can test <strong>webapp1</strong> by pointing your iOS Safari browser to <a href="http://gregsramblings.com/webapp1">http://gregsramblings.com/webapp1</a>, click the share button and select "Add to Home Screen".  You should see the icon and you should see splash screens when you launch it.

<h2>webapp2-add2home</h2>
This is the same as webapp1 but adds Matteo Spinelli's "add to home" script functionality that prompts the user to add the web app to their home screen with simple and clear instructions.  See <a href="http://cubiq.org/add-to-home-screen">http://cubiq.org/add-to-home-screen</a> for the latest script, docs and other information.

You can test <strong>webapp2</strong> by pointing your iOS Safari browser to <a href="http://gregsramblings.com/webapp2">http://gregsramblings.com/webapp2</a> - you should see a popup that points to the share button explaining how to add the app to the home screen.

<strong>more coming soon including offline support</strong>

<h2>Resources</h2>
Blog - <a href="http://gregsramblings.com">http://gregsramblings.com</a>

Twitter - <a href="http://twitter.com/gregsramblings">@gregsramblings</a>