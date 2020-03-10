# spring-boot-h2
Spring boot with h2 database example for e-commerce


1. http://localhost:8081/spring-boot-h2/console/
=> This url is used to check the h2 in memory database console.


2. URL : http://localhost:8081/spring-boot-h2/category-api/createCategory

Method : POST

Request: 
[
	{
		"categoryName" : "Men Wear",
		"categoryDesc" : "Men Wear"
	},
	{
		"categoryName" : "Jeans",
		"categoryDesc" : "Jeans"
	}
]

Response: "success"

3. URL: http://localhost:8081/spring-boot-h2/category-api/getAllCategory

Method : GET

Response:
	[
		{
			"catNo": 1,
			"categoryName": "Men Wear",
			"categoryDesc": "Men Wear"
		},
		{
			"catNo": 2,
			"categoryName": "Jeans",
			"categoryDesc": "Jeans"
		}
	]
4. URL : http://localhost:8081/spring-boot-h2/product-api/createProduct

Method : POST

Request:
	[
		{
			"category" : {
				"catNo" : "1"	
			},
			"productId" : "testid123",
			"productName" : "sai kurta",
			"productDesc" : "sai kurta from test",
			"productImgUrl" : "http://www.get.test.com/kurta.jpg"
		},
		{
			"category" : {
				"catNo" : "2"	
			},
			"productId" : "testid124",
			"productName" : "wrangler",
			"productDesc" : "wrangler from test",
			"productImgUrl" : "http://www.get.test.com/wrangler.jpg"
		}
	]

Response: "success"

5. URL : http://localhost:8081/spring-boot-h2/product-api/searchProducts?searchValue=wrangler

Method : GET

Response: 
	[
		{
			"id": 2,
			"category": {
				"catNo": 2,
				"categoryName": "Jeans",
				"categoryDesc": "Jeans"
			},
			"productId": "testid124",
			"productName": "wrangler",
			"productDesc": "wrangler from test",
			"productImgUrl": "http://www.get.test.com/wrangler.jpg"
		}
	]
