=== Simple GDPR ===
Contributors: Rick Hellewell @rhellewellgmailcom
Tags: GDPR, google analytics, privacy
Donate link: https://www.cellarweb.com
Requires at least: 4.9.6
Tested up to: 6.5
Requires PHP: 7.2
Version: 1.51
Stable tag: trunk
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Creates a simple GDPR notice with links to your Privacy Page. Optionally creates the Privacy Page. Optionally enables server-side Google Analytics with your GA ID (this helps track visitors that have ad blocking).

== Description ==
Simple process to create a 'cookies are OK' banner/button; assumes that site cannot be accessed unless you agree. Creates a privacy page based on US Better Business Bureau recommendations (your country might have different requirements). Also allows for use of Google Analytics via a server-side 'post', to allow analytics tracking if ad-blocking is enabled by the visitor.

Optionally, you can enable placing your Privacy Page link in the site footer.

This is not a very fancy plugin - it just does the basics: displays a notice,and requires the visitor to accept the terms. It 's for simple sites.

Optionally can add your Google Analytics (GA) code. GA process is run on the server side, not client-side. Many ad blockers will block client-side GA, which dilutes your analytics. Running GA on the server ensures that analytics are accurate. No personal information is included in the GA server-side process.

If you have a large site, or complex personal information retention or collection, you might want to find another solution. And 'we are not a lawyer ', so check with your legal folks for guidance. We make no guarantees about the  'legal worthiness ' or afford ability or suitability of our plugin.

Note: requires WP 4.9.6, which contains the new Privacy code/supporting functions. The plugin will not activate if you do not have WP 4.9.6 installed (or PHP 5.3 or higher).  You also need at least PHP 7.4.

Disclaimer: This plugin may not provide full protection for your site, depending on how your site stores and uses personal data. We think our technique meets the basic notification requirements of GDPR, but you should consult with your legal advisors for guidance on what your site needs to do for GDPR compliance. Here is the 'official' GDPR site: https://www.eugdpr.org/ .

For reference:

- We use the code from the Cookie Consent site at https://cookieconsent.insites.com/ to display the Acceptance message and track user response (via a cookie) to the message notice.
- For the generic Privacy Page we generate, we use the guidance from the US Better Business Bureau at https://www.bbb.org/reno/for-businesses/sample-privacy-policy/.
- If you use Google Analytics, then you should be aware of their privacy policy, which could apply to your use of GA; see it here https://www.google.com/analytics/terms/us.html .
- See also the Privacy section.

We suggest that you consult with your legal advisor for specific methods and messages needed for GDPR compliance on your site. We provide no warranty or guarantee of GDPR compliance. We are not providing any legal advice. We are not responsible in any way for your use of our suggested GDPR solution. Your mileage may vary. Objects in mirror are closer than you expect. All aspirin is alike. Professional driver on a closed course.

== Installation ==
This section describes how to install the plugin and get it working.

1. Download the zip file, uncompress, then upload to `/wp-content/plugins/` directory. Or install via the Add Plugin page.
1. Activate the plugin through the 'Plugins' menu in WordPress.
1. Change settings in Settings, 'Simple GDPR Settings' to your requirements.

* Note: do a "Save" on the Simple GDPR Settings page once after an upgrade to ensure all is well; your settings will be preserved.


== Frequently Asked Questions ==
= Do I have to do anything special to enable this? =

You should fill in the settings on the Settings page. They are just selecting your Privacy Page from the dropdown list of all page names.

Optionally, enter your Google Analytics ID if you want to enable service-side Google Analytics - this helps track visitors with ad-blocking enabled. Leave blank if you track analytics with another method, or don't want to track analytics.

The plugin also create a generic Privacy Page, using suggested test from the US Better Business Bureau. This is a page you can edit for your own needs. Or, select an existing Privacy Page via the dropdown list.

= When is the GDPR (Cookie Consent) notice displayed? =

The visitor will see the notice if the Cookie Consent cookie the plugin uses is not set. Once the visitor agrees, the message will go away for about a year. If the visitor deletes the cookie, they will see the message again the next time they visit the site.

= Is any data like a cookie stored in the visitor's browser?=

The "Cookie Consent" cookie is the only cookie stored when this plugin is activate. It only contains a 'yes' or 'no' value. There is no other user data stored on the visitor's browser, nor any data stored on your site other than the plugin options.

= Is there tracking of the user, or any user personal information? =

If you enable server-side Google Analytics (GA) by adding your GA ID number, the visitor's analytics are sent to GA. The visitor's IP address is anonymized before sending it to GA. The geocode for that anonymized IP address will only show the town location, not the user's specific location.

There is no other user-related data or activities saved on your server except the visited page information.

= Can I change the text of the 'Cookie Consent' notice? =

Not with this version. Maybe with a future version. Unless you dig into the code. We'll might add something to the settings page in a future version.

You can see the Cookie Consent message text and other information at https://cookieconsent.insites.com/ .

= Do I really need this GDPR stuff? =

We think so. But, we are not lawyers, so we can't tell you for sure. We just figured that a simple way to put up a notice would be helpful for all the sites we manage. And we didn't find an existing plugin that wasn't complex to use for simple sites. That's why we wrote the plugin. Then we figured that others might find it useful. So, here it is.

= Is all of this legal and compliant with GDPR? =

Who knows? We're not lawyers. But our personal, non-binding, your-mileage-may-vary opinion is that it is enough for simple sites (blogs, brochures, etc) to comply with the (in our opinion) silly GDPR law.

See the disclaimer above. We are providing this as a simple way of complying with the GDPR terms. Contact your legal advisors to see if it is good enough for your site.

= What about the Privacy Link in the footer? =

If enabled, your Privacy page title/link is displayed in your site's footer. Note that there is no CSS for that link; you can adjust CSS using the 'privacy-policy-link' class in your theme, or in Appearances, Customize, Additional CSS (if supported by your theme).

= Do you place a Privacy link in the site menus? = 

Nope. That's up to you. We didn't want to mess with your menu.

= What about the Google Analytics - what data does it send? =

Assuming that you enabled this feature by entering your GA User ID on the Settings page, the plugin will send some basic information to your GA account: page name/URL, geolocation, an anonymous IP address (last octet is blanked), a unique client ID value (to identify all the pages that person visits), and the referring page.

This should be all the info for basic analytics. And the data will be sent for all visitors, including those with ad blockers.

= Does this work with Google Analytics 4 ? =

No, this is only for Google Analytics Universal Analytics, where your GA code starts with UA.

= But Universal Analytics (UA) is going away in 2023, replaced with GA 4 =

Yes, we are aware. A future version of this plugin will use the UA or GA4 value. Still working on that.

= Does this plugin report additional analytics info to GA ? =

No, just the basics. If you want more extended GA analytics information, you'll most likely need a more powerful process, perhaps even one that you have to write.

Or use the GA Javascript version that works on the client side. Except that will still get blocked by many ad blockers. Our process is not affected by ad blockers.

= What if something doesn't work? = 

Contact us on the plugin support page.

= I got an idea for a new feature! = 

Use the Support page to send us new ideas.

== Screenshots ==
1. Shows the entire Settings page.
2. The top half of the Settings page.
3. The bottom half of the Settings page.

== Privacy ==

This plugin does not save any personal information on your server. It will store cookies on your visitor's browsers. If you have enabled Google Analytics (GA), GA is done on the server. GA data only includes the visited page, and an anonymized IP address. No personal information is sent to GA. No cookies related to GA are stored in the client's browser.

== Changelog ==

1.51 (7 May 2022)
* Better display of privacy page link in page footer if enabled.
* Some minor changes to the text of the settings.
* Tested for WP version 6.0.

1.50 (31 Mar 2022)
* Better coordination between privacy page settings on the plugin page, and in the Settings, Privacy page. Changing one will change the other.
* Changed the message next to the Privacy setting on the plugin options screen to indicate the sync between the privacy page value displayed in Settings.
* Some code optimizations to reduce possible non-fatal error messages on screen if options are not set.

1.42 (26 Mar 2022) (also 1.41)
* Adjusted the PHP requirement down to 7.2 (from 7.4). Although we think that you should update your PHP version. The plugin has been tested with PHP 8.x.

1.40 (22 Mar 2022)
* Adjusted server-side GA call to use WP functions, instead of CURL, per WP guidelines.
* Improved gathering of page info to send to GA.
* Changes to the FAQ to add additional info about UA vs the new GA4. UA will go away sometime in 2023, but we'll have an update to work with GA4 by then (with any luck).


1.32 (12 Mar 2022)
* Tweaked the reported page to be the full URL of the page

1.31 (11 Mar 2022)
* Fixed a missing parameter of the Google Analytics server-side command

1.30 (11 Mar 2022)
* Fixed process of saving and using the options. This might require you to re-specify the values on the Settings screen. You should not have to re-create a Privacy page (unless you don't have one); you can select your existing Privacy page.
* Improved the server-side process of doing the Google Analytics call to be more efficient and accurate.
* We anonymize the IP address, changing the last octet to '0' before using that IP address in the server-side GA. The 'anonymize' flag in the GA call is set to false, since you can't anonymize twice (that eliminated GA geocoding). The result is that the IP address is still anonymized, just like your Privacy policy indicates.
* The only cookie stored by this plugin is the one associated with the Cookie Consent popup. This only stores they answer, not any other data.
* Improved the privacy page selection and saving that setting also in the Settings, Privacy page. If there is no privacy page selected in either place, a 'choose one' is shown to match what is seen in Settings, Privacy.
* Removed some unneeded functions; optimized others for slightly better efficiency.
* Standardized functions to start with "SGDPR" to eliminate possible 'duplicate function' errors.
* changed PHP version requirement to version 7.4
* Updated the screenshot images.
* Updated the FAQ area of this document.
* minor text changes and spelling corrections on Settings screen and this document.
* Changes to the 'branding' of the plugin to match our other plugins, including additional updated images in the assets folder.
* Added a sidebar to the Settings screen to show information about other plugins, and a donate button plus the CellarWeb logo.
* Changed various CellarWeb.com links as needed.
* **If you are upgrading from a prior version, check the settings after upgrading**

1.23 (19 Nov 2019)
* fixed some undefined constants that will cause problems in future PHP versions
* compatibility check for WP 5.3
* minor changes to function that creates a GUID value

1.22 (19 Apr 2019)
* put the 'z' parameter for the analytics array at the end, where it is supposed to be.

1.21 (10 Apr 2019)
* Set the server-side analytics code to get the geolocation of the visitor. This was not captured in prior versions.

1.20 (10 Apr 2019)
* Changed all array element names (the part in the brackets) to be strings, rather than 'assumed' strings. The use of 'assumed' strings was causing a PHP Warning about undefined constants. PHP ignores that, although that may cause a fatal error in PHP 8x (whenever that gets released). And the PHP Warnings were cluttering up the error.log file.
So all array element names are now proper strings.

1.11 (7 Jan 2019)
* The plugin needs to set a cookie, but some themes are non-standard, outputting content before
	this plugin can set the cookie. That causes a 'headers already sent' error. And some error
	settings may cause that error message to display on the screen.
  Since the themes are non standard in how they output content, we have to suppress the
  	'headers not sent' message. We do this by saving the error settings, turning off error 
	display, then setting the cookie. Then we restore the error settings to original settings.
	This effectively hides the error message, while still letting the cookie to be set.

1.10 (25 May 2018)
* added support for WP 4.9.6 Privacy functions
* added requirement for WP 4.9.6; plugin will automatically deactivate if not at that minimum version.
* added optional checkbox to display the Privacy page name/link in the page footer.
* some code cleanup

1.02 (4 May 2018)
* fixed issue with timing of when cookies are created
* added reminder when privacy page created that the new Privacy Page should be added to the site menu

1.01 (4 May 2018) - Initial Release

1.00 (28 April 2018) = unreleased version

== Upgrade Notice ==

Check and save settings after upgrade.



