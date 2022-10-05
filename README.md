# Timestamp Microservice


Live on replit
https://timestamp-ms.mcdanang.repl.co/

User Stories:
1. The API endpoint is GET [project-url]/api/:date?
2. A date is valid if can be successfully parsed by new Date(date).
3. API accepts unix time.
4. If the date is empty, the service uses the current timestamp.
5. If the date is valid, the api returns a JSON having the structure
{"unix": <Date.parse(date)>, "utc" : <date.toUTCString()> }
e.g. {"unix": 1479663089000 ,"utc": "Sun, 20 Nov 2016 17:31:29 GMT"}
6. If the date string is invalid the api returns a JSON having the structure
{"error" : "Invalid Date" }.

Example Usage:
[project url]/api/2015-12-25
[project url]/api/1451001600000
[project url]/api/

Example Output:
{"unix":1451001600000, "utc":"Fri, 25 Dec 2015 00:00:00 GMT"}
