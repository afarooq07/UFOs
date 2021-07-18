# UFOs

## Overview of Project
In module 11, we created a webpage with dynamic table to display UFO sighting related information. 

The scope of this challenge is to provide a more in-depth analysis of UFO sighting by providing additional filter criteria to the users that includes city, country, state and shape in addition to date.

<br />

## Resources
 Your site is published at https://afarooq07.github.io/UFOs/

 Folders/Files:
 - index.html
 - static/js/app.js
 - static/js/data.js
 - static/css
 - static/images


## Results
The new filter criteria uses event listerner that detects a change on each input and filters the table accordingly. 

the filter conditions are applied using AND logical. If two filter values are specified, then the filtered table will display all rows that satisfy both filter conditions. 

**Example** -  if we apply the following date and state filters, we will get two rows where date is 1/2/2010 in CA state:

<br />

<img src="/Images/filter1.png" width=700 align=center>

<br />
<br />

If shape filter it set to "light", then the table will be correctly reduced to one row as shown below:

<br />

<img src="/Images/filter2.png" width=700 align=center>

<br />
<br />

if we remove shape filter, we will get the same two rows again where state = CA and date = 1/2/2010:

<br />

<img src="/Images/filter3.png" width=700 align=center>

<br />
<br />


<br />

## Summary
**Drawback** - A disadvantge of this approach is potential performance issues when dealing with very large datasets. Every change to input form will trigger an update of the table on HTML which can slow down user analysis when the intention is to see results filtered by multiple user inputs.

**Recommendations:**
1) The current filters only allow AND operation. The functionality can be expanded to include additional filter types using a checkbox such as:
     - OR logic to show results with state = CA OR shape = circle as an example.
     - EXCLUDE logic to show all results where state <> CA etc.

<br />

2) Add a control (checkbox or radio button) to disable table filtering/update until all filter values have been entered by the user. Enabling table filtering will pickup any user inputs and filter the table accordingly. This can address performance issues when dealing with large datasets.

<br />