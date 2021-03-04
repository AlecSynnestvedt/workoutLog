# workoutLog
A CRUD PERN application that reinforced my API skills and taught me a lot about the fundamentals of React. 

You can see testing verification in /server/screens, which includes screenshots of endpoint testing via Postman as the "client." I've also included them here directly.[screens.zip](https://github.com/AlecSynnestvedt/workoutLog/files/6080399/screens.zip)


================
POSTMAN'S JSON EXPORT:
================
{
	"info": {
		"_postman_id": "9eadf822-b62a-4b67-844b-f9e982282d87",
		"name": "workoutLog",
		"schema": "https://schema.getpostman.com/json/collection/v2.1.0/collection.json"
	},
	"item": [
		{
			"name": "http://localhost:5000/user/register",
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\n    \"user\": {\n        \"email\": \"user@email.com\",\n        \"password\": \"password\"\n    }\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "http://localhost:5001/user/register",
					"protocol": "http",
					"host": [
						"localhost"
					],
					"port": "5001",
					"path": [
						"user",
						"register"
					]
				},
				"description": "Test to make sure the server is running"
			},
			"response": []
		},
		{
			"name": "Register a User",
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\n    \"user\": {\n        \"email\": \"user@email.com\",\n        \"password\": \"password\"\n    }\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "http://localhost:5000/user/register",
					"protocol": "http",
					"host": [
						"localhost"
					],
					"port": "5000",
					"path": [
						"user",
						"register"
					]
				},
				"description": "To register a user"
			},
			"response": []
		},
		{
			"name": "Register Another User",
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\n    \"user\": {\n        \"email\": \"user@email.com\",\n        \"password\": \"password\"\n    }\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "http://localhost:5000/user/register",
					"protocol": "http",
					"host": [
						"localhost"
					],
					"port": "5000",
					"path": [
						"user",
						"register"
					]
				},
				"description": "More sample data"
			},
			"response": []
		},
		{
			"name": "Log IN a user",
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\n    \"user\": {\n        \"email\": \"user@email.com\",\n        \"password\": \"password\"\n    }\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "http://localhost:5000/user/login",
					"protocol": "http",
					"host": [
						"localhost"
					],
					"port": "5000",
					"path": [
						"user",
						"login"
					]
				},
				"description": "Log a user in"
			},
			"response": []
		},
		{
			"name": "Attempt to log in a non-user",
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\n    \"user\": {\n        \"email\": \"notauser@email.com\",\n        \"password\": \"password\"\n    }\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "http://localhost:5000/user/login",
					"protocol": "http",
					"host": [
						"localhost"
					],
					"port": "5000",
					"path": [
						"user",
						"login"
					]
				},
				"description": "for testing"
			},
			"response": []
		},
		{
			"name": "Create a new WL entry",
			"request": {
				"method": "POST",
				"header": [
					{
						"key": "Authorization",
						"value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MTEsImlhdCI6MTYxNDYzMzE4MywiZXhwIjoxNjE0NzE5NTgzfQ.1XHAQ2xSez2TWdF9VLfBKE3nh7f15MoGl7SZzh5gqgU ",
						"type": "text"
					}
				],
				"body": {
					"mode": "raw",
					"raw": "{\n    \"entry\": {\n        \"description\": \"test\",\n        \"definition\": \"test\",\n        \"result\": \"test\"\n    }\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "http://localhost:5000/wl/create",
					"protocol": "http",
					"host": [
						"localhost"
					],
					"port": "5000",
					"path": [
						"wl",
						"create"
					]
				}
			},
			"response": []
		},
		{
			"name": "Get All Log Entries",
			"protocolProfileBehavior": {
				"disableBodyPruning": true
			},
			"request": {
				"method": "GET",
				"header": [
					{
						"key": "Authorization",
						"value": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MTQsImlhdCI6MTYxNDcxOTMzNCwiZXhwIjoxNjE0ODA1NzM0fQ.KgbyJgOGlJB8m0DQwHzzmMJMKlYrAmVfDwvQElZE-H4",
						"type": "text"
					}
				],
				"body": {
					"mode": "raw",
					"raw": "{\n    \"log\": {\n        \"description\": \"test\",\n        \"definition\": \"test\",\n        \"result\": \"test\"\n    }\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "http://localhost:5000/wl/mine",
					"protocol": "http",
					"host": [
						"localhost"
					],
					"port": "5000",
					"path": [
						"wl",
						"mine"
					]
				}
			},
			"response": []
		}
	]
}
