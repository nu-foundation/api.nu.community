
# The Nu Community API Docs

## Base URL

    https://api.nu.community/v1/

## General Query URL

     https://api.nu.community/v1/?query=California

### Attributes
#### Query (varchar)
 - Country - United States or Canada
 - State or Province - California or Alberta
 - Postal Code - 94612
#### Limit (int)
- Limit the number of results 0-100
- Default 25
### Example Response

	// 20220419230315
	// https://api.nu.community/v1/?query=California&limit=2

	[
	  {
	    "id": "f5520892-d201-11eb-a376-b2dcb76f8e11",
	    "name": "Peace Lutheran Church",
	    "address_1": "885 Pomeroy Avenue",
	    "address_2": null,
	    "state": "California",
	    "city": "Santa Clara",
	    "zipcode": "95051",
	    "country": "US",
	    "lat": "37.341087",
	    "lng": "-121.987236",
	    "website": "http://www.peaceaustin.org/",
	    "url": "https://nu.community/f5520892-d201-11eb-a376-b2dcb76f8e11"
	  }
	]

## Coordinates Query URL
     https://api.nu.community/v1/coordinates/?latitude=37.804363&longitude=-122.271111&limit=10&unit=kilometers
### Attributes
#### Latitude 
- 37.804363
#### Longitude
- -122.271111
#### Limit
- Limit the number of results 0-100
- Default 25
#### Unit
- Miles or Kilometers

### Example Response

	// 20220419230658
	// https://api.nu.community/v1/coordinates/?latitude=37.804363&longitude=-122.271111&limit=2&unit=miles

	[
	  {
	    "id": "f5523df0-d201-11eb-a376-b2dcb76f8e11",
	    "name": "Oak Life Church",
	    "address_1": "337 17th Street",
	    "address_2": null,
	    "state": "California",
	    "city": "Oakland",
	    "zipcode": "94612",
	    "country": "US",
	    "lat": "37.805489",
	    "lng": "-122.267075",
	    "distance": 0.41,
	    "website": "http://www.oaklifechurch.com",
	    "url": "https://nu.community/f5523df0-d201-11eb-a376-b2dcb76f8e11"
	  },
	  {
	    "id": "f550dd88-d201-11eb-a376-b2dcb76f8e11",
	    "name": "St. Paul's Episcopal Church Oakland",
	    "address_1": "114 Montecito Avenue",
	    "address_2": null,
	    "state": "California",
	    "city": "Oakland",
	    "zipcode": "94610",
	    "country": "US",
	    "lat": "37.811073",
	    "lng": "-122.260185",
	    "distance": 0.93,
	    "website": "http://www.stpaulsoakland.org/",
	    "url": "https://nu.community/f550dd88-d201-11eb-a376-b2dcb76f8e11"
	  }
	]

# Errors

## 400
### Response
	// 20220419232909
	// https://api.nu.community/v1/

	{
	  "response_code": 400,
	  "response_desc": "Invalid request"
	}

## 400 - Country
### Response
	// 20220419232909
	// https://api.nu.community/v1/

	{
	  "response_code": 400,
	  "response_desc": "The country you enetered is not supported, yet!"
	}

## 400 - Distance
### Response
	// 20220419232909
	// https://api.nu.community/v1/

	{
	  "response_code": 400,
	  "response_desc": "Distance cannot be greater than 321,869 meters."
	}

## 400 - Limit
### Response
	// 20220419232909
	// https://api.nu.community/v1/

	{
	  "response_code": 400,
	  "response_desc": "Limit cannot be greater than 100."
	}
### Response
	// 20220419232909
	// https://api.nu.community/v1/

	{
	  "response_code": 400,
	  "response_desc": "Limit must be an whole number."
	}

## 400 - Units
	// 20220419232909
	// https://api.nu.community/v1/

	{
	  "response_code": 400,
	  "response_desc": "Unit must be either miles or kilometers."
	}

## 404
### Response
	// 20220419232909
	// https://api.nu.community/v1/

	{
	  "response_code": 404,
	  "response_desc": "No results found."
	}
