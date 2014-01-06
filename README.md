kalendar
========

Revamped version of my flat_calendar plugin. Now offers more features and easier customization.  
Supports both custom and Google Calendar events. 

Supported customizations include:  
* __First day of the week__ — Default is monday but could be any day of the month
* __Toggle daylabel__
* __Starting month/year__ — Decide which month you would like to display from start
* __Color__

Usage
-------

flat_calendar could be initialized with both HTML and JS, but I have discountinued developing with HTML support. flat_calendar is still available as a repo https://github.com/ericwenn/flat_calendar if you would like HTML support.  
The reason for this is as the plugin grew more complex and more customizations were added initializing with HTML became harder. Both to write but also for me to parse.

So kalendar only supports JS initialization, and it is for the best.

First of all though, you have to import the .css and .js file to your project.

### Simple kalendar

```javascript
jQuery(".kalendar-element").kalendar();	
```
This will display a red, awesome but pretty useless calendar. No events, no customizations, no funnies.

### Customized kalendar

When initializing your kalendar, include a set of options. These are all of the available:  
__Especially note the tracking variable__
```javascript
$('.example').kalendar({

	// Events are objects, placed inside of an array
	events: [
		{
			title: "Title of event",
			start: {
				date: YYYYMMDD or "YYYYMMDD",	// "20131230"
				time: "HH.MM"					// "12.00"
			},
			end: {
				date: YYYYMMDD or "YYYYMMDD",	// "20131230"
				time: "HH.MM"					// "20.00"
			},
			location: "Location",				// "London"
			url: "http://*.*"					// "http://example.com"
		}
	],

	// Currently available colors are: red, blue, green, yellow. Red is the default.
	color: "blue",

	// Default is Monday, but any day of the week is applicable.
	firstDayOfWeek: "Sunday",

	// Google Calendar reference are objects, place inside of an array to support multiple calendars.
	// If you are unsure how to get an API-key visit: https://developers.google.com/google-apps/calendar/firstapp
	// If you are unsure how to get your calendar visit: https://support.google.com/calendar/answer/63962?hl=en
	googleCal: [{
		calendar: "calendarID",
		apikey: "APIkey"
	},
	{
		calendar: "calendarID",
		apikey: "APIkey"
	}],

	// Any name is possible, but note that not all names might fit in the UI

	monthHuman: [["JAN","January"],["FEB","February"], etc... ],

	// Regarding name lengths same applies here

	dayHuman: [["S","Sunday"],["M","Monday"], etc... ],

	// The text which represents links for events

	urlText: "View on Web",

	// I decided to track people using this plugin in order to make it even better. 
	// The things I collect are current URL, color or kalendar, whether you decided to show days or not and your selected first day of the week.
	// Pass this variable as false and no tracking whatsoever will be done.
	// ***TRUE IS SET AS DEFAULT*** 
	tracking: true
});

```

Todo
-----
* Reccuring events, both for Google Calendar but also custom ones.
* Add minified version
* Unique colors for each event
* Weeknumber
* 


Changelog
----
`v1.1.0 2014-01-04`: Added links for events.
`v1.0.0 2013-12-30`: First version published, yay!


Thanks
-----
I hope you will like using this plugin as much as I did creating it.  
If you have __any__ questions regarding this plugin, or just in general, please contact me.


Eric Wennerberg
http://ericwenn.se
https://twitter.com/ericwenn