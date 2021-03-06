=== WP Photo Album Plus ===
Contributors: opajaap
Donate link: https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=OpaJaap@OpaJaap.nl&item_name=WP-Photo-Album-Plus&item_number=Support-Open-Source&currency_code=USD&lc=US
Tags: photo, album, slideshow, video, audio, lightbox, iptc, exif, cloudinary, fotomoto, imagemagick, pdf
Version: 6.7.01
Stable tag: 6.7.00
Author: J.N. Breetvelt
Author URI: http://www.opajaap.nl/
Requires at least: 3.9
Tested up to: 4.8
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

This plugin is more than just a photo album plugin, it is a complete, highly customizable multimedia cms and display system.

== Description ==

This plugin is more than just a photo album plugin, it is a complete, highly customizable multimedia content management and display system.

Features:

* Any number of albums that contain any type of multimedia file as well as sub albums
* Full control over the display sizes, responsive as well as static
* Full control over links from any type of image
* Full control over metadata: exif, iptc can be used by keywords in item descriptions
* Up to 10 custom defined meta data fields, for albums and for media items
* Front-end uploads
* Bulk imports
* Built-in lightbox overlay system
* Built-in Google Maps to display maps based on the photo gpx exif data
* Built-in search functions on a.o. keywords and tags
* A customizable rating system
* Commenting system
* Moderate user uploads and comments
* Configurable email notification system
* 20 widgets a.o. upload, slideshow, photo of the day, top rated and commented items and many more
* Supports Cloudinary cloud storage service
* Supports Fotomoto print service
* Required maintenace is fully executed by background processes (cron jobs)
* Extended error/event logging system
* Extended documentation site: https://wppa.nl/

Plugin Admin Features:

You can find the plugin admin section under Menu Photo Albums on the admin screen.

* Albums: Create and manage Albums.
* Upload: To upload photos to an album you created.
* Import: To bulk import items to an album that are previously been ftp'd.
* Moderate: Change status of pending
* Export: To export albums
* Settings: To control the various settings to customize your needs.
* photo of the day widget settings
* Help & Info: Credits and link to the documentation site

Translations:

<ul>
<li>Dutch translation by OpaJaap himself (<a href="http://www.opajaap.nl">Opa Jaap's Weblog</a>)</li>
<li>Slovak translation by Branco Radenovich (<a href="http://webhostinggeeks.com/user-reviews/">WebHostingGeeks.com</a>)</li>
<li>Polish translation by Maciej Matysiak</li>
<li>Ukranian translation by Michael Yunat (<a href="http://getvoip.com/blog">http://getvoip.com</a>)</li>
<li>Italian translation by Giacomo Mazzullo (<a href="http://gidibao.net">http://gidibao.net</a> & <a href="http://charmingpress.com">http://charmingpress.com</a>)</li>
<li>German translation by Stefan Eggers</li>
</ul>

== Installation ==

* Standard from the plugins page

= Requirements =

* The plugin requires at least wp version 3.1.
* The theme should have a call to wp_head() in its header.php file and wp_footer() in its footer.php file.
* The theme should load enqueued scripts in the header if the scripts are enqueued without the $in_footer switch (like wppa.js and jQuery).
* The theme should not prevent this plugin from loading the jQuery library in its default wp manner, i.e. the library jQuery in safe mode (uses jQuery() and not $()).
* The theme should not use remove_action() or remove_all_actions() when it affects actions added by wppa+.
Most themes comply with these requirements.
However, check these requirements in case of problems with new installations with themes you never had used before with wppa+ or when you modified your theme.
* The server should have at least 64MB of memory.

== Frequently Asked Questions ==

= What do i have to do when converting to multisite? =

* See https://wppa.nl/changelog/installation-notes/#multisite

= Which other plugins do you recommend to use with WPPA+, and which not? =

* Recommended plugins: qTranslate, Comet Cache, Cube Points, Simple Cart & Buy Now.
* Plugins that break up WPPA+: My Live Signature.
* Google Analytics for WordPress will break the slideshow in most cases when *Track outbound clicks & downloads:* has been checked in its configuration.

= Which themes have problems with wppa+ ? =

* Photocrati has a problem with the wppa+ embedded lightbox when using page templates with sidebar.

= Are there special requirements for responsive (mobile) themes? =

* No, WPPA+ is responsive by default

= After update, many things seem to go wrong =

* After an update, always clear your browser cache (CTRL+F5) and clear your temp internetfiles, this will ensure the new versions of js files will be loaded.
* And - most important - if you use a server side caching program (like WP Total Cavhe) clear its cache.
* Make sure any minifying plugin (like W3 Total Cache) is also reset to make sure the new version files are used.
* Visit the Photo Albums -> Settings page -> Table VII-A1 and press Do it!
* When upload fails after an upgrade, one or more columns may be added to one of the db tables. In rare cases this may have been failed.
Unfortunately this is hard to determine.
If this happens, make sure (ask your hosting provider) that you have all the rights to modify db tables and run action Table VII-A1 again.

= How does the search widget work? =

* A space between words means AND, a comma between words means OR.
Example: search for 'one two, three four, five' gives a result when either 'one' AND 'two' appears in the same (combination of) name and description.
If it matches the name and description of an album, you get the album, and/or the photo.
OR this might apply for ('three' AND 'four') OR 'five'.
The tokens must be at least 3 characters in length.

= How can i translate the plugin into my language? =

* See the translators handbook: https://make.wordpress.org/polyglots/handbook/
* Here is the polyglot page for this plugin: https://translate.wordpress.org/projects/wp-plugins/wp-photo-album-plus

= How do i install a hotfix? =

* See the documentation on the WPPA+ Docs & Demos site: https://wppa.nl/docs-by-subject/development-version/

== Changelog ==

See for additional information: <a href="http://www.wppa.nl/changelog/" >The documentation website</a>

= 6.7.01 =

= Bug Fixes =

* Under some circumstances the audiobar under slideshow was mis-aligned. Fixed.
* Many textual fixes (mainly typos).

= New Features =

* Table IX-A11: Minimum tags. These tags exist even when there are no photos that have one or more of these tags.
* Table IX-A12: Login link. Change this if you have a custom login page and you have ticked Table IV-F1: Commenting login or Table IV-E1: Rating login.

= Other Changes =

* Widgets have been revised to make the activation screens more consistent in usage and appearance.

= 6.7.00 =

= Bug Fixes =

* Many textual fixes, thanx to Stefan Eggers who has completed the german translations.
* Fixed a rounding issue in the calculation of wppa container width when the width in the shortcode was set to a fraction, causing intermittent layout issues.

= New Features =

* New shortcode attribute **timeout** for slideshows (type="slide", type="slideonly", type="slideonlyf"). Usage: [wppa type="slide" album="13" timeout="2000"][/wppa] for 2000ms. (2s.) timeout.
[wppa type="slide" album="13" timeout="random"][/wppa] for a random timeout between 2 and 7 times the animation speed.
* Completed translations for the German language, by Stefan Eggers

= 6.6.x =

* See https://wppa.nl/changelog/changelog-6-6-x/

= 6.5.x =

* See https://wppa.nl/changelog/changelog-6-5-x/

= 6.4.x =

* See https://wppa.nl/changelog/changelog-6-4-x/

= 6.3.x =

* See https://wppa.nl/changelog/changelog-6-3-x/

= 6.2.x =

* See https://wppa.nl/changelog/changelog-6-2-x/

= 6.1.x =

* See https://wppa.nl/changelog/changelog-6-1-x/

= 6.0.x =

* See https://wppa.nl/changelog/changelog-6-1-x/#6.0.0

== About and Credits ==

* WP Photo Album Plus is extended with many new features and is maintained by J.N. Breetvelt, ( http://www.opajaap.nl/ ) a.k.a. OpaJaap
* Thanx to R.J. Kaplan for WP Photo Album 1.5.1, the basis of this plugin.

== Licence ==

WP Photo Album is released under the GNU GPL licence. ( http://www.gnu.org/copyleft/gpl.html ))