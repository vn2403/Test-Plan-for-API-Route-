Test documentation


Running the Tests
Collection Runner:
Go to the Collection Runner in Postman.
Select the "Artists API Tests" collection.
Click "Run".



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
