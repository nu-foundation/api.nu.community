
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
- Limit the number of results. 

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
	    "website": "http://www.peaceaustin.org/",
	    "url": "https://nu.community/f5520892-d201-11eb-a376-b2dcb76f8e11"
	  },
	  {
	    "id": "f55207d7-d201-11eb-a376-b2dcb76f8e11",
	    "name": "Peace Lutheran Church",
	    "address_1": "885 Pomeroy Avenue",
	    "address_2": null,
	    "state": "California",
	    "city": "Santa Clara",
	    "zipcode": "95051",
	    "country": "US",
	    "website": "http://peacejourney.org/",
	    "url": "https://nu.community/f55207d7-d201-11eb-a376-b2dcb76f8e11"
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
- Limit the number of results. 
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
	    "distance": 0.93,
	    "website": "http://www.stpaulsoakland.org/",
	    "url": "https://nu.community/f550dd88-d201-11eb-a376-b2dcb76f8e11"
	  }
	]