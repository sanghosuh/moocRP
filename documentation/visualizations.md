[Back to README](../README.md)

Visualizations
================

One main functionality of moocRP is the ability for researchers to upload analytics modules that they've created and share it with other researchers. This allows other researchers to view what's already been done and apply the same analytics module to various datasets and possibly alternative data types.

A <strong>data type</strong> could be something like MOOCdb.

A <strong>dataset</strong> could be the data for a specific offering of a course during a specific term.

File Structure
---
Uploaded files should be archived in a ZIP archive. The structure of the analytics module should be of this form:

    ````
    main.html
    css/
    js/
    ````

````main.html```` is used to display the main visualization - all script and stylesheet dependencies should be listed in ````main.html````. All script and CSS files should be placed in the ````js/```` and ````css/```` folders respectively.


Reading Data
---
moocRP uses a templating system called EJS. EJS allows moocRP to pass data from the server to the client through special variables using their syntax of brackets. Where you normally load in data in your analytics module, you should replace with ````"<%- dataset %>"```` or ````"<%= dataset %>"````. This allows your visualization to access the string-represented version of the dataset, which you can then process into any format you'd like.

Pre-processing Data
---
TODO

Sample Analytics Module
---
See a modification of [Sven Charleer's analytics module](http://www.github.com/kk415kk/moocrp_visualization).

Under construction.