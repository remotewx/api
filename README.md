# Remote Jobs API

The Remotewx Jobs API returns the list of all active remote job listings on the [Remotewx job board](https://remotewx.com/). The API supports an URL endpoint for HTTPS requests and JSON formats as responses.

## Endpoint

`GET https://remotewx.com/api`


## URL Parameters

Following optional url parameters can be used to filter job listings.

* limit - Limit the number of job listing results
* q - Search job listing title and description.

## Example

`curl 'https://remotewx.com/api?limit=1'`

Returns a JSON response with the following format:

```javascript
{
  "legal": "API Terms of Service: Please link back to the URL on Remotewx and mention Remotewx as a source, so we get traffic back from your site. If you do not we'll have to suspend API access. Please do not submit our jobs to third Party websites like Google Jobs, LinkedIn Jobs, etc. Our free API is only dedicated to indie developers willing to build websites to share remote jobs. Have any questions about API? Please contact @remotewxcom on Twitter.",
  "usage": "Documentation: https://github.com/remotewx/api",
  "version": 1.0,
  "jobs": [
    {
      "id": "38z8h89hio", // Unique ID
      "createdAt": 1625639220,
      "category": 7, // 1 = Programming, 2 = Design, 4 = DevOps & SysAdmin, 5 = Management & Finance, 6 = Product, 7 = Support, 8 = Sales & Marketing, 9 = Other
      "title": "Job Title",
      "type": "fullTime or contract",
      "company": "Company Name",
      "region": "anywhere", //  anywhere, us, canada, europe, north-america, south-america, amer, asia, africa, australia, uk, emea, apac, other
      "url": "https://remotewx.com/remote-jobs/company-name-position-title",
      "logo": "https://remotewx.com/assets/logos/6fENFRrWhp-1625563835.png", // soon .png will be replaced by .webp
      "description": "Full HTML description",
      "salary": "$10.000 - $200.000" // Annual in USD or null
    }
  ],
  "totalRows": 1 // number of results
}
```

Have any questions about our API? Please contact [@remotewxcom](https://twitter.com/remotewxcom) on Twitter.
