=== Events Calendar ===

Contributors: snumb130
Donate link: http://www.wp-eventscalendar.com/donate
Version: 6.7.13
Tags: event, calendar, date, time, widget, admin, sidebar, plugin, javascript, thickbox, jquery, tooltip, ajax
Requires at least: 2.7.1
Tested up to: 3.1.3
Stable tag: 6.7.13

Events-Calendar is a versatile replacement for the original WordPress calendar adding many useful functions to keep track of your events.

== Description ==

Events-Calendar is a versatile replacement for the original calendar included with WordPress adding many useful functions to keep track of your events. The plugin has an easy to use admin section that displays a big readable calendar and lets you add and delete events. 

The plugin is widget ready so you can easily add a small calendar to the main sidebar with the ability to roll over the highlighted event day to see a brief description of the event or click the day to get a full description of the event without ever leaving your current page.

If you are not using a widget ready theme, you can still have the calendar on your sidebar.  Simply place `<?php sidebarEventsCalendar();?>` (or `<?php sidebarEventsList($number_of_items);?>` if you want a list) in the sidebar file. The widget can also show a specified number of events as a list.  You will find these options under the widget option.

The ability to add a large public calendar is available by posting a page and adding `[events-calendar-large]` to the page content to create a stand alone calendar page. Also, when entering an event from the admin section, you can check the box saying "Create Post for Event", which will cause a post to be created with the event information.

Additional features will be added so make sure that you keep up to date on upcoming changes and new features by subscribing to the [RSS feed on the Events Calendar site](http://www.wp-eventscalendar.com/feed).

== Installation ==

1. Upload `events-calendar` folder to the `/wp-content/plugins/` directory.
2. Activate the plugin through the Plugins menu in the Dashboard.
3. Set options under Events Calendar/Options on the admin menu.
	
== Screenshots ==

1. Events Calendar Admin
2. Events Calendar Options
3. Events Calendar Widget Options
4. Events Calendar as Widget Calendar
5. Events Calendar as Widget List
6. Events Calendar as Large Calendar

== Upgrade Notice ==
= 6.7.13 =
* This update fixes the issue with slashes in events.  This will work on new events, and will be corrected when editing events.  Backup before upgrading.

= 6.7.12a =
* This update fixes an XSS injection attack to the Wordpress plugin admin page that allowed for execution of arbitrary HTML code.  When updating please backup your CSS file if you have made customizations to the stylesheet.

== Changelog ==
= 6.7.13 =
* This update fixes the issue with slashes in events.  This will work on new events, and will be corrected when editing events.  Backup before upgrading.

= 6.7.12 =
* This update fixes an XSS injection attack to the Wordpress plugin admin page that allowed for execution of arbitrary HTML code.  When updating please backup your CSS file if you have made customizations to the stylesheet.

= 6.7.11 =
* Removing sponsor message

= 6.7.10 =
* Fixed SQL injection vulnerability pointed out by @zap1989

= 6.7.9 =
* Changed the way the sponsor message is shown and hidden to prevent have hidden links that were hurting SEO.

= 6.7.8 =
* Checking for existance of timezone function
* Add Japanese language file from blog.bng.net

= 6.7.7 =
* Timezone is now reading from wordpress timezone for choosing current day.  I am silly.

= 6.7.6 =
* Added option to hide Sponsor messages
* Fix added for conflict with ddsmoothmenu.
* Removed call to dimensions jquery plugin.

= 6.7.5 =
* Removed calendar and time select buttons until errors are resolved.
* Added sponsorship message.

= 6.7.3 =
* Corrected problem where quotes not escaped properly in admin section with title.  Thanks Pat

= 6.7.2 =
* Events and tooltip issues in large calendar.

= 6.7.1 =
* Fixed disappearing tooltips.

= 6.7 =
* Fixed the hover error to show info when hover over date.

= 6.6.4 =
* Fixed error causing extra characters during activation.  Thanks brianlayman

= 6.6.3 =
* Added fix for thickbox popup show wrong day (props to nenya)
* Fixed error with tooltips not showing.  thanks dhobeika.

= 6.6.2 =
* Fixed error with loading image overwriting all pics.

= 6.6.1 =
* All changes in 6.6.1 came from byronrode
* Added the ability to enable/disable tooltips in the administration
* Fixed Wordpress 3.0 initialization issues
* Added "hasEvent" class to table cell for days that have events
* Modified the LargeCalendar and LargeCalendarJS to echo by default, but added the ability to return the markup using bool(true/false). This is merely documented for historical purposes as the change was needed for the new shortcode loading of the calendar to work and has no effect within any templates.
* Added Native WP Shortcode for the plugin to load the Large Calendar. Now loads by calling "[events-calendar-large]" replacing the existing method. Please replace where necessary in your pages/posts.
* The WP shortcode addition also stops the plugin from preventing other plugins/themes shortcodes to load when used on the same page as the calendar.
* Cleaned up JS from above which was looping when navigating through 2 or more months.
* Changed the JS in the sidebar calendar to load the JS and prev/next links correctly when navigating through months

= 6.6 =
* WPEC is now WP 2.7 and 2.8 ready. This fixes issues #20, #21 and #38..
* Fixed issue #17: Consistency with WP plugin UI conventions.
* Fixed issue #16: Larger description in textarea. 
* Fixed issue #18: displayLarge uses $options before it is set.
* Fixed issue #22: Click for more info not working
* Fixed issue #27: Events not showing on widget in public view.
* Fixed issue #29: Firefox reported 2 errors.
* Fixed issue #31: Start / End Times do not appear to take start / end date into consideration.
* Fixed issue #32: Tooltip doesn't show correctly when there is a large amount of text in the description. This is partly resolved in fact. The tooltip will grow larger depending on the text size but a very large amount of text will still shoow this problem. I would suggest making a post if you have too much text.
* Fixed issue #34: Wrong timezone: US (am/pm) vs. European time.
* Fixed issue #37: Ajax character set problems with Spanish language (and other too for sure).
* Fixed issue #40: Post titles are incorrect when they contain an '. 
* Fixed issue #42: Conflict with Register Plus plugin. pluggable.php is a BAD THING! When we start doing reminders and stuff like that, we may need to override some of these functions which will again break compatibility.
* Fixed issue #45: Showing incorrect day.
* Fixed issue #46: Widget in Sidebar will not change to Calendar view .
* Fixed issue #48: WordPress Database Error: invalid SQL syntax.
* Fixed issue #52: spacing between line too close.
* Fixed issue #56: Thickbox and 'moving' WordPress.
* Added license file and comments.
* Adapted the readme.txt file to the latest spec from wordpess.org

= 6.5.2.1 =
* Fixed tooltip type in ec_js.class.php

= 6.5.2 =
* *Done by [Heirem](http://heirem.fr)*
* Fixed Some corrections in recording into database.
* Fixed Bug in jQuery plugin Datepicker 1.5.2 : replace ui.datepicker.min.js by ui.datepicker.js
* Fixed In the small calendar navigation fails with the passage of years
* Fixed Implementation of effective jQuery extreme conflict management
* Added Option checkbox : jQuery extrem protection or not
* Fixed With some databases the 'EventsCalendar_main' table creation was not at the activation plugin
* Added Updated jQuery Tooltip in 1.3 
* Added jQuery bgiframe plugin for correcting Tooltips with IE
* Fixed jQuery event change() replaced by click() to work with IE
= Version 6.5.1 realised by Heirem, =
* Fixed Some optimisations of code in routines
* Fixed Validation W3C XHTML 1.0
* Fixed Conflicts jQuery code optionnal due to issues in navigation months in calendar
* Added Function to displays Events List in the sidebar without widgets.
* Fixed Links in Javascript code to réfresh calendar when permalinks issues
* Fixed Management of the coma during events records

= 6.5 =
* This version was realised by Heirem, with the active participation of Maida, Andy, Pepawo, Justin, Mayur
* Fixed Conflicts jQuery with orther plugin like cforms
* Fixed Options are now initialized at the activation 
* Fixed Line moved for compatibility with Role Scoper
* Fixed The days of the week are now displayed correctly in short format for the Slavic languages in UTF-8
* Fixed Event List is now localized
* Fixed The day of the week now corresponding to the date in all latitudes
* Fixed The dot is now supported as a separator for the interpretation of the date
* Fixed The creation of an event can not be done with a empty title
* Added Submenu Add Event
* Added Event List diplay a message when there is no events
* Added An event can now be linked to an article. A click on the Large calendar or in the Events list in sidebar opens the corresponding page
* Added The ThickBox is now a little larger
* Added An option to indiquet the adaptation of the stylesheet plugin
* Added In modification of event you can associate a post with its ID
* Added CSS Rules for the today date in the options
* Added Possibility to link an event to an external link to the site by its URI

= 6.4.1 =
* Added fix localization based on the Wordpress classe locale.php instead PHP function set_locale();
* Added Spain, German and Czech langages files.

= 6.4 =
* Added fix for file_get_contents by Ian72.
* Added localization by Heirem.  Also added French language files.

= 6.3.2 =
* Change in time and date format. (Ron)
* Added option to change length of day names in calendars (Ron)
* Fixed bug for event list tooltip.

= 6.3.1 =
* Fixed bug with using newlines in description of event
* Fixed bug with file_get_contents
* Added option to pick CSS formatting for the days with events in the widgets.

= 6.3 =
* Fixed major bug pointed out by Ron.  When month was changing, calendar was disappearing.  This is fixed.

= 6.2 =
* Ron added css for high lighting the current day in large calendar.  This can be edited in the events-calendar.css file.  Id is #todayLarge
* For widget calendar, if the theme style sheet provides style then the current date will be marked with theme styling.  If the theme does not contain this style then the current date will be with a red border.
* Fixed bug of showing all events in thickbox regardless of visibility level.

= 6.1 =
* Added Time Picker for time entries
* Fixed some access level issues and clearing duplicate entries.
* Took out COLLATE from database sql
* Dates will not reset when plugin

= 6.0.12 =
* Fixed type in time entry.

= 6.0.11 =
* Fixed css not allowing day header to show in IE

= 6.0.10 =
* Fixed edit form to make location to update.

= 6.0.9 =
* Hopefully, fixed conflict with NextGEN Gallery.  Thanks, LUcky.
* Fixed problem with quotes in text entries.

= 6.0.8 =
* Fixed some AJAX stuff for the calendar update messing with CSS.

= 6.0.7 =
* Fixed some database entries for old versions.

= 6.0.6 =
* Change str_ireplace to str_replace for use with php4

= 6.0.4 =
* Added functionality for the visibility level of each event.
* Changed the event list view to show events that have not ended yet, not only events that started before current day.

= 6.0.3 =
* Dates now show in the events list view.

= 6.0.2 =
* Fixed datbase problem, hopefully.

= 6.0.0 =
* Calendar is formatted the same as wordpress calendar.  Widget will take theme settings.
* Added Thickbox when day is clicked on.  Shows more event details.
* Added ajax fuction for changing months.

= 5.8.3 =
* Added feature to identify current day (Added by Diego)

= 5.8.2 =
* Added option to choose the color of the text display when you hover over an event date.  Also rearranged the menu a little in the widget options.

= 5.8.1 =
* Fixed some alignment errors.

= 5.8.0 =
* Fixed some of the cache problems that were occurring because of permissions to write to the directories.  I basically just took it out so the cache will not be used.
* Also added the ability to select the visibility level of the events.  You can choose the level of access that is required to see the events.  All existing events will default to Public access.  You will need to deactivate and reactivate the plugin to make sure that the database gets updated.

= 5.7.15 =
* Added a widget option to allow for the choosing of font size in the widget.

= 5.7.14 =
* Fixed some css stuff.

= 5.7.13 =
* Hopefully cleared up the Fatal Cache Error when trying to use iCal.

= 5.7.12 =
* Added link to widget title that will carry you to the admin page for the calendar

= 5.7.11 =
* Moved the Events Calendar tab under the Manage tab to show easier with Wordpress 2.5.

= 5.7.10 =
* Feature Added - Support for K2 sidebar modules has been added.  When you extract the plugin you will see a new folder.  If you are not using K2 sidebar modules then there is nothing extra you need to do.  If you are wanting to use this as a K2 sidebar module you will have to upload a file to the K2 theme.  The file is located in the plugin folder under the folder k2-module.  This file inside must be uploaded to the k2 module folder.  The directory is as follows: wp-content/themes/k2/app/modules

= 5.6.10 =
* Bug Fix - Fixed errors caused in PHP4 with ical parsing

= 5.5.10 =
* Bug Fix - Displaying duplicate March in drop down menu on widget.

= 5.5.9 =
* Added ability to show events from ical.  There is still some issue with irregular occurrances.  However, seems to work fine with DAILY, WEEKLY, MONTHLY, YEARLY standard reccurring events.

= Version 4.5.9 =
* Bug Fix - Error cause by themes not containging <?php wp_footer();?>  

= 4.5.8 =
* Bug Fix - Fixed error caused by using single quotes.
* Added Spanish translation from Covi
* Changed events list format to show current days events as well as future.

= 4.4.7 =
* Added ability for multiple languages, patch from Rauli Haverinen
* Added Finnish translation files from Rauli Haverinen

= 3.4.6 =
* Just straightened some code.

= 3.4.5 =
* Code beautification

= 3.3.5 =
* Took out donate link as it is on my site now.

= 3.3.4 =
* Added fix from Kerwin Kanago to correct problem in php4 fix from Brett Minnie

= 3.3.3 =
* Set color of text to black in hover box.  Fixed problem showing up with themes with light color text.
* Added option to choose minimum user level to edit event. (You must go to widget options and resave them or management page will not show up)

= 2.3.2 =
* Bug Fix - Calendar wouldn't accept events with day having leading zero.  Converted string to int to fix.

= 2.2.2 =
* Bug Fix - Problem caused with redeclaring str_split

= 2.2.1 =
* Display Calendar as upcoming event list. (revision by Dan Coulter - http://www.dancoulter.com)
* Choose diplay format of Date and Time. (revision by Dan Coulter)

= 1.2.1 =
* Hide empty fields.  (suggestion by Dan Coulter)
* php4 fix.  (revision by Brett Minnie - http://www.fractalmetal.co.za)

= 1.1.1 =
* Bug Fix - Wordpress variabl clashing with events variable.  Fixed bug displaying archives.

= 1.1.0 =
* Title Option
* Day Name Length Option

= 1.0.0 =
* First release.

== Frequently Asked Questions ==

= I use a theme with a dark background.  My events don't show well in the large calendar view. =

In the css folder there is a file called events-calendar.css. This file has the css for the calendar. It is commented as Large Calendar.