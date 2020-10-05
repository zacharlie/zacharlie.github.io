# ArcGIS REST Table

Learn by example datatable for displaying attribute data for feature classes using the ArcGIS Javascript REST API.

Designed to dynamically build the table columns in accordance with the data returned by the request.

## Data sources

Within the index.html there are some commented out urls to display different types of valid get requests, including some with additional or more complex queries and some that access a local data source in JSON format.

Note that the JSON uses the structure returned from ArcGIS REST Services, such as this [example](https://sampleserver6.arcgisonline.com/arcgis/rest/services/WorldTimeZones/MapServer/2/?f=pjson), not standard geojson.

## Notes

For local files, the application will need to run as a web service in order to prevent modern browsers blocking content due to Cross-Origin Resource Sharing (CORS) security procedures.

With python you can easily fire up `python -m http.server --bind 127.0.0.1 9101` which should make the index.hml available at http://127.0.0.1:9101 from the browser.
