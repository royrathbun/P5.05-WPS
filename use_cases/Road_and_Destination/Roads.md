<b><h2>Parameters Necessary for...</h2></b>
 
<b><h3>Roads</h3></b>

<i>These parametetes have been taken from Google Developers Documentation 2018

><b>Path</b>
>>_The path parameter accepts a list of latitude/longitude pairs._

><b>Key</b>
>>_Must identify itself every time it sends a request to the Roads._

><b>interpolate</b>
>>_To interpolate a path to include all points forming the full road-geometry._

><b>snappedPoints</b>
>>_An array of snapped points. Each point consists of the following fields_
>>><b>Location</b>
>>>>_Contains a latitude and longitude_

>>><b>originalIndex</b>
>>>>_An integer that indicates the corresponding value in the original request_

>>><b>interpolate=true</b>
>>>>_The response will contain more coordinates than the request._

>>><b>originalIndex</b>
>>>>_These values are indexed from 0, so a point with an originalIndex of 4 will be the snapped value of the 5th latitude/longitude passed to the path parameter_

>>><b>placeId</b>
>>>>_A unique identifier for a place_

><b>warning_message</b>
>>_A string containing a user-visible warning

><b>speedlimits</b>
>>_An array of road metadata_

><b>Units</b>
>>_KPH or MPH or KNOTS_

><b>nearestRoads</b>...
>>_Indicates roads near to present location_

<b><h5>Example Request</h5></b>

>The following request will snap the specified points to the road geometry. This particular set of data follows a circular road; setting <b>interpolate=true</b> ensure that the returned geometry will match the curvature of the road. With <b>interpolate=false</b>, the snapped path will still follow the road, but the resulting polyline will not be as smooth.

<b>Request</b>

https://roads.googleapis.com/v1/snapToRoads?path=-35.27801,149.12958|-35.28032,149.12907|-35.28099,149.12929|-35.28144,149.12984|-35.28194,149.13003|-35.28282,149.12956|-35.28302,149.12881|-35.28473,149.12836&interpolate=true&key=API_KEY

<b>Response</b>

<img src="https://github.com/DGIWG/P5-Geospatial-Web-Services-Program/blob/master/_figures/1.PNG">
<img src="https://github.com/DGIWG/P5-Geospatial-Web-Services-Program/blob/master/_figures/2.PNG">
<img src="https://github.com/DGIWG/P5-Geospatial-Web-Services-Program/blob/master/_figures/3.PNG">
TBC
