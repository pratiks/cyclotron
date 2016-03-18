# 1.27.0 (03/17/2016)

## Features

 - Annotation Chart: built-in support for editing annotations.  Annotations are stored in CyclotronData and can be shared between different charts.

 - CyclotronData: HTTP and JavaScript API for storing simple data directly in Cyclotron.  A new Data Source makes it easy to load from CyclotronData into Widgets.  Limited to 16MB

 - Analytics: Add number of unique, active “likes” on the Analytics page; enable additional statistics like average number of tags, editors, viewers per Dashboard

 - Angular.js upgraded to 1.4.x branch.

 ## Bug Fixes

  - Table Widget: numeralformat properties does not support inline JS unless used in a rule

# 1.26.0 (03/03/2016)

## Features

 - Like button always visible: instead of hiding when logged out, the clicking the Like button will prompt the user to login.

## Bug Fixes

 - Logout and Like button no longer shown when authentication is disabled

# 1.25.0 (02/18/2016)

## Features

 - Image Widget: added a new Widget for displaying images.

 - YouTube Widget: added a new Widget for displaying YouTube videos.

 - Data Source Broadcasting: rewrote all Data Sources and Widgets to communicate using global events.  This resolves memory leaks and performance degredation due to unremoved callbacks.

 - Improved logging, and added a configurable property to enable debug logging (globally)

## Bug Fixes

 - Removed unique constraint on email field for Users

## Breaking Changes

 - The Data Source api method 'getData()' has been deprecated.  Any custom Widgets should be rewritten to follow the new event-based messaging pattern.  Any custom Data Sources which use the Data Source Factory (recommended) will automatically use the new pattern.

# 1.24.0 (02/04/2016)

## Features

 - Scrolling Dashboards: Dashboards now automatically scroll if the Widgets on a page exceed the size of the browser.  If the Widgets on a page fit without overflowing, the Dashboard will appear as before without any scrollbars.  This replaces the previous behavior of fitting the page to the browser window, and hiding any overflowing content.

 - Likes: Added the ability for logged-in users to like (and unlike) dashboards.  Users can search for dashboards they liked, or sort search results by the number of likes

 - Sortable Search Results: The Dashboard Search results can be sorted using various keys such as Name, Tags, Visits, Likes, etc.

 - Advanced Search Filters: Dashboards can be searched using several new search filters: "is:deleted", "include:deleted", "likedby:<user>", "lastupdatedby:<user>".

## Bug Fixes

 - Data Sources must be created with unique names

 - Navigating through Cyclotron pages using browser back button does not work
 
 - Annotation Chart: annotationsWidth property in AnnotationChart widget should be a numerical field instead of a string

# 1.23.0 (01/21/2016)

## Features

 - Annotation Chart Widget: New Widget added, based on Google's Annotation Chart control.  Great for creating time-series line charts with or without annotated labels on the data.

 - Analytics API Improvements: added ?max property to most of the endpoints.

 - User API Improvements: collecting Department/Division property from Active Directory.

 - Highcharts upgraded to 4.2.0

## Bug Fixes

 - Fullscreen Graphs Won’t Scale Vertically

 - Chart Widget: Highcharts Property Linked Across Widgets

 - Login Fails for Service Accounts without Department/Division

# 1.22.0 (11/12/2015)

## Features

 - Chart Widget: Drilldown chart support added

 - Highcharts upgraded to 4.1.9

 - Node.js 4.0 support and testing

## Bug Fixes

 - Global Analytics: sort by page views descending.

 - Data Source Placement - Moved the Data Source property to the top of each Widget type (below title) for consistency.

# 1.20.0 (10/15/2015)

## Features

 - Initial public release of Cyclotron