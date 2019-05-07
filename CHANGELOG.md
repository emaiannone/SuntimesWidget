### ~

### v0.11.4 (2019-05-07)
* fixes bug "NotificationService is always running" (#323, #324).
* fixes bug "AlarmClockActivity started multiple times" (#325, #324).
* removes the "location mode" selector from widget configuration (widgets only support the "user-defined" mode) (#10).
* updates translation to Brazilian Portuguese (pt-br) (#320 by Neto Silva).

### v0.11.3 (2019-04-17)
* fixes crash when opening general settings (Esperanto) (#315).
* adds "rise/set order" help button to the widget configuration activity.
* misc. layout and icon changes (Widget List, About).
* updates translations to Polish (pl) and Esperanto (eo) (#317 by Verdulo).
* updates translation to Brazilian Portuguese (pt-br) (#319 by Neto Silva).

### v0.11.2 (2019-04-08)
* adds an option to disable the alarm clock launcher icon (#305).
* adds translation to Brazilian Portuguese (pt-br) (contributed by Neto Silva) (#304).
* updates translations to Polish (pl) and Esperanto (eo) (#307 by Verdulo).
* misc. widget layout fixes. Widgets now ignore the "large text" accessibility setting (#306). Use a custom theme to increase text size.
* fixes app crash (world map dialog)  (#309).

### v0.11.1 (2019-03-28)
* updates translations to Spanish (es-es) and Catalan (ca) (#301 by Raulvo).
* updates translations to Polish (pl) and Esperanto (eo) (#302 by Verdulo).

### v0.11.0 (2019-03-12)
* adds "Suntimes Alarms", an Alarm Clock (#140, #250, #261) with support for daily repeating alarms and notifications.
* adds a clock widget (#154, #260); displays solar time (Local Mean Time, Apparent Solar Time), or the time in a given timezone.
* adds a "share" action to the World Map dialog (exports to png) (#284).
* changes the default solar time mode to "Apparent Solar Time"; adds a help button to solar time mode selector.
* new permission: BOOT_COMPLETED. This permission is needed to restore active alarms after reboot. [PERMISSION]
* new permission: VIBRATE. This permission is used by alarm notifications. [PERMISSION]
* misc style and layout fixes.

### v0.10.3 (2019-01-31)
* adds app shortcuts (Android 7.1+); a shortcut to the Widget List, a shortcut to the Theme Editor (#288).
* reveals previously hidden azimuthal map projection in the World Map dialog (#284); layout issues for this projection continue to exist for smaller screens.
* fixes a CalculatorProvider bug where sun/moon queries returned the wrong data type (Calendar obj vs long timestamp).

### v0.10.2 (2019-01-10)
* fixes bug "'get location' does not honor the 'units of length' pref" (#290).
* improves the accuracy of the apparent solar time calculation (#291).
* updates translation to Basque (eu) (#294 by beriain). 

### v0.10.1 (2018-12-23)
* fixes bug "sun/moon circles are difficult to see (too small)" (#286) on lightmap and worldmap widgets.
* updates translation to Norwegian (nb) (#285 by FTno).
* updates dependency (Time4A 4.2-2018g).

### v0.10.0 (2018-12-09)
* adds support for themes to the app; it is now possible to customize the app's appearance using widget themes (#264, #275).
* adds "order" option to sun and moon widgets; "display tomorrow's sunrise once sunset time has passed" (#190).
* adds "distance units" (imperial, metric) to General Settings; display distances (altitude/elevation, shadow length) using meters or feet (#273).
* adds "shadow length" to the Sun Position dialog (#189, #273), and "object height" to General Settings.
* adds support for third-party apps and widgets through a ContentProvider (#266, #276); https://github.com/forrestguice/SuntimesWidget/wiki/Interfaces.
* removes Calendar permissions (READ_CALENDAR, WRITE_CALENDAR, READ_SYNC_STATS, WRITE_SYNC_SETTINGS); 
* removes Calendar Integration; this feature is now available as a separate apk (#239, #266, #277); https://github.com/forrestguice/SuntimesCalendars.
* extends the widget update strategy to support per widget updates; the sun and moon widgets may now trigger an update shortly after each event (in addition to the daily update at midnight).
* adds dst label to timezone dialog; displayed when selected timezone is using daylight saving time (#274).
* adds eot label to timezone dialog; displayed for apparent solar time (#274).
* adds "import themes" and "share themes" (export) to the theme list activity (#275). 
* adds "action color" to themes (button press color) (#275).
* fixes cropped text in theme config activity (#254); misc layout improvements.
* updates the legacy icon to match the appearance of the adaptive icon (#272).
* updates translation to Polish and Esperanto (eo, pl) (#282 by Verdulo).
* updates build; Android gradle plugin version bumped to `com.android.tools.build:gradle:3.0.0` (and gradle wrapper to `gradle-4.1`).
* updates dependency (Time4A 4.1-2018g).

### v0.9.5 (2018-11-12)
* modifies the default colors to improve contrast and readability (#247, #264, #268).
* fixes bug "language selectors fails for some languages" (#262).
* fixes empty widgetlist; an oversized label and icon are now displayed when the list is empty.
* fixes worldmap bug where the sun/moon positions are drawn despite sunlight/moonlight options toggled off.
* fixes settings activity iconography (unique icons for each header); the previous patch only fixed this for older Android versions where the icon attribute is completely ignored.
* updates translation to Basque (eu) (#271 by beriain).
* updates translation to Norwegian (nb) (#270 by FTno).
* updates translation to Polish and Esperanto (eo, pl) (#263, #267 by Verdulo).

### v0.9.4 (2018-10-28)
* fixes bug "widgets missing" (#258); installLocation set to internalOnly.
* fixes appearance of main table for locales with header text shorter than event times; sunset column now has minWidth.
* fixes appearance of snackbar warnings; now styled by theme.
* fixes readability of snackbar warnings for locales with long action button text.
* fixes Settings Activity iconography; unique icons for each header.
* updates translations to Spanish (es-es) and Catalan (ca) (#255 by Raulvo).
* updates translation to Norwegian (nb) (#253 by FTno).
* adds translation to Traditional Chinese (zh-tw) (contributed by ft42) (#252).

### v0.9.3 (2018-10-10)
* adds help to the "theme list" activity.
* adds translation to Italian (it) (contributed by Matteo Caoduro) (#249).

### v0.9.2 (2018-09-12)
* adds altitude ui to the datasource card; toggles altitude (hidden when datasource lacks support) (#245).
* fixes app crash when location has altitude greater equal 11000m (validation off-by-one) (#243).

### v0.9.1 (2018-08-30)
* fixes bug "export places; commas in place names break csv output bug" (#240).
* fixes bug "momentary hang/pause when adding or reconfiguring sunposition widgets (3x1 and 3x2)".
* adds permission explanations to fastlane app description.
* adds runtime permission explanations (a dialog displayed prior to each permission request).
* adds privacy link to about dialog (links to https://github.com/forrestguice/SuntimesWidget/wiki/Privacy); added privacy statement to readme.
* updates translation to Polish and Esperanto (eo, pl) (#238, #241 by Verdulo).
* updates translation to Norwegian (nb) (#236 by FTno).

### v0.9.0 (2018-08-14)
* changes default sun data source to time4a-time4j (supporting altitude based refinements).
* changes default 'en' location to New York City, and default 'en-US' location to Phoenix.
* enhances the data source selector; now tags the default source, and sources loaded via plugin.
* enhances data sources (plugins); support for loading external sources (not included with app) (#229).
* adds elevation to all default locations; default 'en' location changed to New York City, default 'en-US' location changed to Phoenix.  
* adds elevation UI to Location settings, main ActionBar, and widget title substitutions. 
* adds app pref "Use Elevation"; apply altitude based refinements; defaults true.
* adds app pref "On Date Long Press"; defaults to "Show Calendar".
* adds permissions READ_CALENDAR, WRITE_CALENDAR; needed to interact w/ Calendar app (add/remove events in custom calendars).
* adds permissions READ_SYNC_STATS, WRITE_SYNC_SETTINGS; needed to provide custom calendars (add/remove calendars via SyncAdapter).
* adds a SyncAdapter (LOCAL account) to provide the Calendar app with custom calendars.
* adds options to toggle visibility of twilight times displayed by the app (hide fields).   
* refactors widgetlist activity to use ActionBar (#230).
* adds 3x1 and 3x2 SunPosition previews to theme editor.
* adds 3x2 SunPosition widget showing world map.
* adds world map dialog to app; shows sunlight (day/night) and moonlight over an equirectangular map.
* adds theme "Dark (translucent)"; default theme with semitransparent widget background.
* adds to theming; custom background option (simple background color supporting transparency).
* updates translation to Polish and Esperanto (eo, pl) (#235 by Verdulo).
* updates translation to Norwegian (nb) (#224 by FTno).
* updates dependency (Time4A 3.44.2-2018b). 

### v0.8.6 (2018-07-05)
* updates translation to French (fr) (#220 by Aloha68).
* updates translation to Norwegian (nb) (#221 by FTno).
* updates translations to Polish and Esperanto (eo, pl) (#217 by Verdulo).

### v0.8.5 (2018-06-18)
* add gps pref "Passive Location"; use the passive location provider (use a separate app to manage location updates).
* fixes bug where the "GPS is disabled. Enable it?" dialog is not shown.
* updates translation to Norwegian (nb) (#214, #215 by FTno).

### v0.8.4 (2018-06-07)
* fixes polar regions usable hours bug (#209).
* fixes app crash on polar regions when no rise/set events (#212).
* fixes lightmap polar regions bugs where wrong color is shown during perpetual day/night (#209).
* fixes lightmap bug where durations are drawn incorrectly (near boundaries up to timezone offset).
* fixes lat/lon input validation bug (#211).
* fixes date format localization bug (#210).

### v0.8.3 (2018-05-31)
* adds translation to Norwegian (nb) (contributed by FTno) (#206).
* removes unused option "show seconds" from sun position widgets.

### v0.8.2 (2018-05-11)
* adds to theming; graph colors; day, civil, nautical, astronomical, and night colors.
* fixes bug where "export places" creates an empty file (#204).
* enhances calculator fallback behavior; e.g. SuntimesMoonData now overrides the default (sunrisesunsetlib -> Time4A4J).
* fixes bug where solstice/equinox card fails to hide when calculator lacks support (and fallback was supplied).
* fixes app crash (MoonDialog) if calculator failed to load (and fallback was supplied) (#198).
* fixes app crash (General Settings) when initializing defaults (api26) (#198).
* fixes bug where user-defined language fails to override locale (api26) (#197).


### v0.8.1 (2018-04-26)
* misc layout changes (improvements for locales w/ long strings).
* fixes column alignment of solstice/equinox in main table; now aligns w/ the sunrise column.
* fixes column alignment of moonrise/moonset in main table; now aligns w/ the sunrise column.
* changes label alignment of 3x1 SunPosition widget; now centered (#188).
* adds enhancements to the language selector; now sorted alphabetically, now displays name of language in that language (and displays localized language name in parenthesis).
* adds translation to Basque (eu) (contributed by beriain) (#193, #194).
* updates translation to German (de) (contributed by Wolkenschieber) (#191, #192).

### v0.8.0 (2018-04-10)
* fixes app crash (in ThemeConfigActivity) when the app is configured to use a calculator that lacks support for the moon feature.
* adds click behavior to main table headers; clicking sunrise/sunset highlights next sunrise/sunset.
* changes the default alarm label format (label now includes shortDate).
* adds moonrise and moonset to the AlarmDialog.
* adds moon dialog to app; shows major phases, rising/setting times, rising/setting position, current position, phase, and illumination (current).
* adds moon info to app (main table); rise/set, phase, and illumination (at lunar noon) (#52, #183).
* adds "moon data source" to general settings.
* fixes bug where solstice dialog is not correctly initialized (when "show solstice" option is false).
* fixes widget update alarms (more precise); sun and moon widgets update at midnight, solstice widgets update every 3hr, and sun position widgets update every 5min.
* adds 3x1 sun position widget; shows lightmap (and optional azimuth and elevation labels) (#107).
* adds 1x1 sun position widget; shows right ascension and declination.
* adds 1x1 sun position widget; shows azimuth and elevation angles (#169).
* adds sun azimuth and elevation angles to lightmap dialog (#169).
* adds "sun position" overflow menu item; shows lightmap dialog.
* updates translations (eo, pl) (#184, #186 by Verdulo).

### v0.7.4 (2018-03-26)
* adds "restore defaults" button to "On Tap: Launch App" help dialog.
* fixes widget config edittext auto-correct behavior (now disabled for title text, launch app).
* fixes app crash when location supplied by GPS has negative altitude (some Samsung devices).
* adds moontimes icon (displayed by moon widgets in widget list).
* simplifies datepicker (removes mode spinner) (#173).
* app automatically restarts on day/night change (when using nightmode theme).
* app automatically restarts on theme change or locale change.
* app automatically advances to next note (when card is unswapped) (registers/unregisters an alarm for next event).
* app automatically updates on date change (registers/unregisters an alarm for midnight).
* fixes bug where the date has advanced to the next day but the displayed times have not (after midnight up to difference between local time and timezone).
* fixes bug where the formatted date is off by a day (before midnight up to difference between local time and timezone).
* updates translations (eo, pl) (#180 by Verdulo).

### v0.7.3 (2018-03-16)
* reorders user interfaces prefs (organized into categories).
* fixes talkback accessibility issues; snackbar warning messages not announced, datetext and timezone fields announcing unused tags, timezone dialog announcing previous state on mode change.
* fixes app crash (api14, api15) when accessibility settings are disabled.
* fixes app crash when location name contains special characters (#177).

### v0.7.2 (2018-03-11)
* adds clock tap action: "Set Time Zone"; timezone label now clickable (launches TimeZoneDialog).
* default date tap action changed to "Set Date" (#173).
* enhances the "Set Date" dialog; adds "Today" button, quicker date selection (#173).
* better support for talkback (announceForAccessibility api16 and under).
* adds widget option "show time (with date)"; include the time when displaying dates.
* adds widget option "show hours"; include hours/minutes in time spans greater than a day.
* adds widget title substitution; %dt and %dT are for time (of last widget update).
* adds widget title substitution; %id is for appWidgetID (for debug purposes).
* adds widget option "show labels"; show/hide extra labels.
* updates dependency (Time4A 3.40-2018b). 
* updates url: AboutDialog now links https://forrestguice.github.io/SuntimesWidget/ 
* updates translations (eo, pl) (#171, #172, #175 by Verdulo); adds translated fastlane metadata.

### v0.7.1 (2018-02-28)
* fixes bug #120 (widget icons don't use theme icons); now works for all api versions.
* enhances the widget list; adds appWidgetID label to the list and widget (re)configure activity.
* adds widget ontap action; "update widget" to manually trigger widget updates.
* fixes (workaround) missing/deleted update alarms; opening the widget list now reschedules alarms (that may be missing / deleted (e.g. forced stop)).
* fixes widget update when a theme is modified; all widgets sharing that theme are updated.
* adds "themes" menu item to widgetlist activity; launches the theme editor (w/out navigating through widget config).
* adds "about" menu item to theme selector activity.
* fixes widget list scroll; state preserved on orientation change.
* fixes theme selector scroll; automatically scroll to the selected item.
* fixes theme selector ordering; sort items alphabetically, grid selector shows defaults first.
* enhances the theme selector; grid selector item layout shows more colors.
* enhances the theme selector; toggle the preview background (shows home screen wallpaper).
* enhances the theme editor; flip between multiple previews (adds moon widget previews).
* adds to theming; moon phase colors; the new moon, waxing, waning, and full moon colors are now themeable.
* adds to theming; "bold" title option, "bold" time option.

### v0.7.0 (2018-02-17)
* adds a 3x1 moon widget (showing major phases) (#52).
* adds a 2x1 moon widget (showing rise/set + phase + illumination) (#52).
* adds several 1x1 moon widgets (showing rise/set times, current phase, next phase, or illumination) (#52).
* adds twilight durations to the lightmap dialog.
* adds option to "places settings" to generate a list of world cities (by scanning locale defaults).
* adds "show weeks" option to app and solstice widget (#153).
* adds "show blue hour" option to app (#127).
* adds "show golden hour" option to app (#127).
* adds golden hour, blue hour (8deg), and blue hour (4deg) to rise/set times (#127).
* fixes en localization; e.g. "Fall" is better known as "Autumn" (#159), "color" vs "colour", etc.
* updates translations (eo, pl) (#160, #162, #163 by Verdulo).

### v0.6.2 (2018-02-03)
* adds option "verbose accessibility"; better support for TalkBack. 
* misc usability fixes (MainActivity, AlarmDialog); better support for TalkBack. 
* misc layout fixes (improved accessibility); better support for "large text".
* fixes bug "solstice/equinox dates not localized" (#146).
* adds "adaptive" launcher icon (used by api26+).
* updates translations (eo, pl) (#148, #149 by Verdulo).
 
### v0.6.1 (2018-01-23)
* adds translations to Catalan (ca) and Spanish (es-ES) (contributed by Raulvo) (#141).
* fixes bug; expected "11h 55s", actual "11h55s" (#b61d942).
* enhances the calculator selector used by widget configuration (now shows descriptive text).
* misc accessibility fixes (labelFor, dropDownVerticalOffset).
* adds web links in the About Dialog to the changelog and version commit.  
* updates translations (eo, pl) (#137 by Verdulo).

### v0.6.0 (2017-12-27)
* adds solstice/equinox tracking to app (#13).
* adds solstice/equinox widget (#13).
* adds option to show seconds in rise/set times displayed by widgets.
* adds option to show seconds in rise/set/delta times displayed by the app.

### v0.5.2 (2017-12-21)
* fixes "tomorrow will be" comparison; erroneously reported 1m (when actually 0s) for non-simple sources (1m is correct for sunrisesunsetlib and time4a-simple).
* misc refactoring to prevent memory leaks (LightMapTask, TimeZonesLoadTask).
* fixes flippable widget randomly displays 24hr time (#129).
* fixes table switch animation fails to play (#125).
* fixes automatic keyboard popup (WidgetConfigActivity, ThemeConfigActivity); prevent the keyboard from taking focus on activity start. 
* fixes stale/duplicate items in theme selector.
* fixes theme preview icons (now shown) (api22+).
* fixes theme icons don't use theme colors (api22+) (#120).
* fixes crash when adding widgets (api22+) (#126).
* updates dependency (Time4A 3.38-2017c).
* updates translations (eo, pl) (#123, #124 by Verdulo).

### v0.5.1 (2017-12-03)
* changes default data source to time4a-noaa (fallback remains sunrisesunsetlib).
* fixes 2x1 widget to show seconds (e.g. "Tomorrow will be 1m 4s shorter").
* restricts auto-backup to app settings and themes (now excludes widget settings and sqlite db).
* adds collapsed UI state to ColorChooser; expanded by clicking label. 
* adds to theme config activity: sunrise, sunset, and noon icon colors (fill, stroke, stroke width).
* fixes theme previews to display sunrise/sunset times (as configured by app) instead of static text.
* fixes widget sunrise, sunset, and noon icons to use theme colors.
* fixes widget titles to marquee over a single line when too long.
* fixes widgets to allow for vertical resize.
* lists 2x1 widget (previously only accessible by resizing 1x1 widget).
* fixes 2x1 layout for api versions <= 15 (previously inaccessible).
* updates dependency (Time4A 3.37-2017c).
* updates translations (eo, pl) (#115, #116 by Verdulo).

### v0.5.0 (2017-11-18)
* auto-backup reenabled.
* adds data source; Time4A (time4a-simple, time4a-noaa, time4a-cc, time4a-time4j) (contributions by MenoData) (#103).
* adds support for custom themes; theme editor activity (add / edit), theme selector activity (copy / delete / export) (#7).
* adds widget option "show noon" (#102); adds noon field to 1x3 widget, adds noon to flippable widget.
* adds widget option "show comparison" (show/hide comparison field on 1x3 widgets).
* adds option to show data source label in app UI / misc data source related UI enhancements.
* adds translation to Hungarian (hu) (contributed by Erci) (#106).
* updates translations (eo, pl) (#110 by Verdulo).

### v0.4.1 (2017-10-31)
* fixes data source setting not honored (#104).

### v0.4.0 (2017-06-12)
* adds translation to French (fr) (contributed by Jej) (#92).
* adds time format option (12hr / 24hr time) (#22).
* adds daylight savings time warning (#90).
* automatic backups now disabled.
* fixes app layout; times unreadable when using large font setting (related to #43).
* fixes lightmap rendering (now optimized to do work off the UI thread).
* updates translations (eo, pl) (#93, #94, #96, #97 by Verdulo).

### v0.3.1 (2017-04-15)
* misc UI tweaks, styles, and strings.
* fixes widget preview images.
* fixes ui bug "table switches unintentionally" (#20).
* fixes "allow resize" option (disabled for api 16 and under).
* updates translations (eo, pl) (#86, #87 by Verdulo).
* adds Junit and Espresso UI testing to the project.

### v0.3.0 (2017-02-23)
* adds data source; ca.rmen.sunrisesunset.
* adds solar time mode; local mean time, and apparent solar time (#66).
* adds "light map" horizontal stacked bar chart.
* adds "ui warnings" (snackbar alerts for unusual date or time zone configurations) (#54).
* adds time zone selector enhancements (color coding, sort by ID or UTC offset).
* adds widget layout option "allow resize" (disable widget resizing).
* adds widget title substitution; %s is for data source.
* fixes app crash (latitude edge case) (#74).
* fixes app crash ("set date" api10) (#75).
* fixes time zone selector loading (now loads asynchronously).
* fixes widget layout update bug / widget resizes itself after update (#77).
* fixes widget update behavior (now updates at midnight) (#77).
* updates translations (eo, pl) (#69, #72, #73, #79, #80, #83, #84 by Verdulo).

### v0.2.3 (2016-11-07)
* fixes alarm set incorrectly w/ user-defined timezones (#64).
* fixes solar noon sometimes incorrect for user-defined timezones (#65).
* fixes ui bug "dialog state lost on orientation change" (#63).
* fixes ui bug where TimeDateDialog settings were not immediately applied.

### v0.2.2 (2016-09-22)
* use network location provider if available (#49).
* fixes gps prefs not honored (#50).
* fixes app crash on SettingsActivity (api14, api15) (#55).
* fixes app crash on ExportPlaces (api18) (adds permission EXTERNAL_STORAGE) (#67).
* fixes misc SettingsActivity bugs (api10, api15) (#57, #58, #59, #60).
* updates translations (eo, pl) (#51 by Verdulo).

### v0.2.1 (2016-08-30)
* fixes unreadable app layouts when using non-english locales (#43).
* fixes missing actionbar overflow icons.
* fixes lat/lon input; touch dialog fields to begin editing (#37).
* updates translations (eo, pl) (#46, #47 by Verdulo).

### v0.2.0 (2016-08-13)
* adds translation to Polish (pl) and Esperanto (eo) (contributed by Verdulo) (#24, #26, #31, #35, #36).
* adds option to override the locale from within the app (#23).
* adds default location provided by the locale (#33).
* fixes lat/lon decimal separator bug (#29); fails to set the location when locale uses "," as the decimal separator.
* fixes timezone bug (#34); timezone ignored when using 24hr time.
* fixes ui bug "note doesn't adapt user defined dates" (#19).
* fixes ui bug "table switches unintentionally" (#20).

### v0.1.1 (2016-07-21)
* adds support for localization.
* adds translation to German (de) (contributed by Henrik "HerHde" H�ttemann) (#16).
* fixes app crash when using Show map without an installed map application.
* fixes app crash when sunrise or sunset does not occur for a given date/location.
* fixes "no data source" bug (#14); default value not properly displayed by settings -> general -> dataSource.
* fixes lat/lon precision; was unlimited but now rounded to 5 places (meter precision).
* fixes lat/lon input validation.

### v0.1.0 (2016-07-04)
* adds app activity that displays times for a given location and date
* adds widgetlist activity for reconfiguring home screen widgets
* fixes lat/lon input field bug

### v0.0.2 (2016-03-11)
* adds flippable widget
* adds ontap actions (reconfigure, launch activity)
* adds get gps fix (user defined location)

### v0.0.1 (2015-02-16)
* basic widget
