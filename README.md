# E-Commerce-API-Nodejs
This API supports e-commerce operations, such as product and category listing, product details, cart management, and order processing. It uses Mongo database to manage product/category data, user cart information, and order details. The API can also handle token management in the system.

## Setup
 
```
    $ git clone https://github.com/IshanKapoor12/E-Commerce-API-Nodejs.git
    $ cd E-Commerce-API-Nodejs
    $ npm install
```
  - Connect to a database on Mongo Atlas and fill in the Environment Variables.

  ### Run The Service
  ```
  $ nodemon server.js
  ```
## API Endpoints

## User Routes

### * Create User

`POST |  /api/v1/users/register` 

| Key       | Value          |
| --------- | -----------    |
| name      | Admin          |
| email     | admin@admin.com|
| password  | password       |
| phone     | +9318437947     |
| isAdmin   | true           |
| street    | Main Street    |
| apartment | Block C        |
| zip       | 10870          |
| city      | New Delhi      |
| country   | India          |

### * Login User

`POST |  /api/v1/users/login` 

| Key        | Value          |
| ---------  | -----------    |
| email      | admin@admin.com|
| password   | password       |

### * Get Users

`GET |  /api/v1/users` 

### * Get Single Users

`GET |  /api/v1/users/{id}` 

### * Delete User

`DELETE |  /api/v1/users/{id}` 

### * Get Users Count

`GET |  /api/v1/users/get/count` 

## Category Routes

### * Create Category

`POST |  /api/v1/categories` 

| Key   | Value      |
| ------| ---------- |
| name  | Category 1 |
| icon  | icon-health|
| color | #55879     |

### * Get Categories

`GET |  /api/v1/categories` 

### * Get Single Category

`GET |  /api/v1/categories/{id}` 

### * Update Category

`PUT |  /api/v1/categories/{id}` 

| Key   | Value      |
| ------| ---------- |
| name  | Category 1 |
| icon  | icon-health|
| color | #55879     |

### * Delete Category

`DELETE |  /api/v1/categories/{id}`

## Product Routes

### * Create Product

`POST |  /api/v1/products` 

| Key            | Value           |
| ---------      | -----------     |
| name           | Product 1       |
| description    | Description     |
| richDescription| Rich Description|
| image          | image           |
| brand          | Brand 1         |
| price          | 50              |
| category       | {category_id}   |
| countInStock   | 100             |
| rating         | 4.5             |
| numReviews     | 40              |
| isFeatured     | true            |

### * Get Products

`GET |  /api/v1/products` 

###  * Get Single Category

`GET |  /api/v1/products/{id}` 

###  * Get Product Count

`GET |  /api/v1/products/get/count` 

###  * Get Featured Product Count

`GET |  /api/v1/products/get/featured/{count}`

### * Upload Gallery Images

`POST |  /api/v1/products/gallery-images/{id}`
| Key            | Value           |
| ---------      | -----------     |
| images         | Array of images |

### * Update Product

`PUT |  /api/v1/products` 
| Key            | Value           |
| ---------      | -----------     |
| name           | Product 1       |
| description    | Description     |
| richDescription| Rich Description|
| image          | image           |
| brand          | Brand 1         |
| price          | 50              |
| category       | {category_id}   |
| countInStock   | 100             |
| rating         | 4.5             |
| numReviews     | 40              |
| isFeatured     | true            |

### * Delete Product

`DELETE |  /api/v1/products/{id}`

## Orders Routes

### * Create Order

`POST |  /api/v1/orders` 
```
{
	"orderItems":[
		{
			"quantity": 3,
			"product" : "602e9c348e700335d8532b14"
		},
			{
			"quantity": 2,
			"product" : "602bde0161fcc409fc149734"
		}
	],
	"shippingAddress1" : "No 45,Park Street",
	"shippingAddress2" : "No 46,Main Street",
	"city" : "Colombo",
	"zip" : "10600t",
	"country" : "Sri Lanka",
	"phone" : "+94717185748",
	"user" : "602e9b718e700335d8532b13"
}
```
### * Get Orders

`GET |  /api/v1/orders` 

### * Get Single Order

`GET |  /api/v1/orders/{id}` 

### * Get Total Order Count

`GET |  /api/v1/orders/get/count`

### * Get Total Sales

`GET |  /api/v1/orders/get/totalsales`

### * Get User Order

`GET |  /api/v1/orders/get/usersorders/{userid}`

### * Update Single Order

`PUT |  /api/v1/orders/{id}` 

### * Delete Single Order

`DELETE |  /api/v1/orders/{id}` 

## Author
Ishan Kapoor
