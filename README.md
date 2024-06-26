
***
Directions
1. Please create a test plan for this route, addressing positive and negative tests 
2. Please create an automated test for this route. Pseudocode is acceptable. Assume the general framework is already in place

***
Resolved assignment (links)
1. Test Plan for API Route  ->  https://docs.google.com/document/d/1OfoLhPLUtCZCOqJdYGMYT9jB_bVfQC7ehMfxZ6vjYQ4/edit?usp=sharing
2. Pseudocode/JS" -> https://docs.google.com/document/d/1J1-aaF5QX3TNQGpz-qGlXnazpy7kc_cNUBf-MwN5dfI/edit?usp=sharing
   
***
References: API Documentation
Route GET /v4/catalog/artists/
Artists are the producers or performers of music in the Beatport catalog. This route returns a list
of artists whose music is in the Beatport catalog.
Parameters
Name string (query)
Filter name by case-insensitive text containment.
Name_exact string (query)
Filter by name exact match.
Created string (query)
Filter by exact, less/greater than equal, and range. Supports slice syntax: `date=1970-01-01` (exact)
`date=:1971-01-01` (less than equal) `date=1970-01-01:` (greater than equal)
`date=1970-01-01:1971-01-01` (range)
Updated string (query)
Filter by exact, less/greater than equal, and range. Supports slice syntax: `date=1970-01-01` (exact)
`date=:1971-01-01` (less than equal) `date=1970-01-01:` (greater than equal)
`date=1970-01-01:1971-01-01` (range)
Id number (query)
Filter by artist ID exact match. Supports `OR` lookup: `param=value1,value2`
Enabled string (query)
Filter by enabled.
Page integer (query)
A page number within the paginated result set.
Per_page integer (query)
The number of results to return per page.
Response
A successful request returns the HTTP 200 OK status code and a JSON response body with the
following properties.
Count integer
Next string | $uri
Previous string | $uri
Results array
The “Results” array contains artist objects with the following structure
{
"created": "2023-03-21T15:15:48-06:00",
"id": 1095995,
"image": {
"id": 5539565,
"Uri":
"https://geo-stage-media.beatport.com/image_size/590x404/0dc61986-bccf-49d4-8fa
d-6b147ea8f327.jpg",
"Dynamic_uri":
"https://geo-stage-media.beatport.com/image_size/{w}x{h}/0dc61986-bccf-49d4-8fa
d-6b147ea8f327.jpg"
},
"name": "Kobe",
"slug": "kobe",
"updated": "2023-03-21T15:21:23-06:00",
"website": null,
"url": "https://api.beatportstage.com/v4/catalog/artists/1095995/",
"dj_association": null
}
