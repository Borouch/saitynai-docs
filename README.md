# Schema


# Routes
## Entries

#### Index

GET `api/entries`

**response**
```json
    "entries": [
        {
            "id": 1,
            "entry_template_id": 1,
            "user_id": 1,
            "created_at": "2022-12-13T21:05:38.000000Z",
            "updated_at": "2022-12-13T21:05:38.000000Z",
            "header_input": {
                "id": 1,
                "name": "Sushi",
                "description": null,
                "form_template_id": 1,
                "entry_id": 1,
                "created_at": "2022-12-13T21:05:38.000000Z",
                "updated_at": "2022-12-13T21:05:38.000000Z",
                "form_template": {
                    "id": 1,
                    "name": "Food",
                    "order": 0,
                    "form_type": "Header",
                    "item_type_id": null,
                    "entry_template_id": 1,
                    "created_at": "2022-12-13T21:04:34.000000Z",
                    "updated_at": "2022-12-13T21:04:34.000000Z"
                }
            },
            "multi_select_inputs": [
                {
                    "id": 1,
                    "form_template_id": 3,
                    "entry_id": 1,
                    "created_at": "2022-12-13T21:05:38.000000Z",
                    "updated_at": "2022-12-13T21:05:38.000000Z",
                    "form_template": {
                        "id": 3,
                        "name": "Ingredients",
                        "order": 2,
                        "form_type": "MultiSelect",
                        "item_type_id": 1,
                        "entry_template_id": 1,
                        "created_at": "2022-12-13T21:04:34.000000Z",
                        "updated_at": "2022-12-13T21:04:34.000000Z"
                    },
                    "selected_items": [
                        {
                            "id": 1,
                            "multi_select_input_id": 1,
                            "item_id": 1,
                            "user_id": 1,
                            "content_entry_id": null,
                            "created_at": "2022-12-13T21:05:38.000000Z",
                            "updated_at": "2022-12-13T21:05:38.000000Z",
                            "item": {
                                "id": 1,
                                "name": "Rice",
                                "item_type_id": 1,
                                "is_public": 0,
                                "created_at": "2022-12-13T21:05:38.000000Z",
                                "updated_at": "2022-12-13T21:05:38.000000Z"
                            }
                        }
                    ]
                }
            ],
            "text_inputs": [],
            "entry_template": {
                "id": 1,
                "name": "Food",
                "user_id": 1,
                "created_at": "2022-12-13T21:04:34.000000Z",
                "updated_at": "2022-12-13T21:04:34.000000Z"
            },
            "rating_inputs": [],
            "multi_datetime_inputs": [
                {
                    "id": 1,
                    "at": "2022-12-13T05:40:00.000000Z",
                    "from": "2022-12-13T05:40:00.000000Z",
                    "to": "2022-12-13T05:40:00.000000Z",
                    "mode": "point",
                    "form_template_id": 2,
                    "entry_id": 1,
                    "created_at": "2022-12-13T21:05:38.000000Z",
                    "updated_at": "2022-12-13T21:05:38.000000Z",
                    "form_template": {
                        "id": 2,
                        "name": "Time",
                        "order": 1,
                        "form_type": "MultiDatetime",
                        "item_type_id": null,
                        "entry_template_id": 1,
                        "created_at": "2022-12-13T21:04:34.000000Z",
                        "updated_at": "2022-12-13T21:04:34.000000Z"
                    }
                }
            ]
        },
```

#### Show

GET `api/entries/{id}`

**Response:**
[[#Entries#Index]]

#### Create

POST `api/entries`

**Body**
```json
{
    "entry_template_id": 1,
    "header_input": {
        "name": "Sushi",
        "description": "",
        "form_template_id": 1
    },
    "text_input": [],
    "rating_input": [],
    "multi_select_input": [
        {
            "selected_items": [
                {
                    "item": {
                        "id": null,
                        "item_type_id": 1,
                        "name": "Rice"
                    },
                    "id": null,
                    "content_entry": null
                }
            ],
            "form_template_id": 3
        }
    ],
    "multi_datetime_input": [
        {
            "at": "2022-12-13 05:40",
            "from": "2022-12-13 05:40",
            "to": "2022-12-13 05:40",
            "mode": "point",
            "form_template_id": 2
        }
    ]
}
```

**Response**
Success: 200
```json
{
    "entry": {
        "id": 8,
        "entry_template_id": 1,
        "inputs": {
            "header": {
                "entry_id": 8,
                "name": "Sushi",
                "description": null,
                "form_template_id": 1,
                "updated_at": "2022-12-16T12:04:18.000000Z",
                "created_at": "2022-12-16T12:04:18.000000Z",
                "id": 7
            },
            "rating": null,
            "text": null,
            "multi_datetime": [
                {
                    "entry_id": 8,
                    "at": "2022-12-13T05:40:00.000000Z",
                    "from": "2022-12-13T05:40:00.000000Z",
                    "to": "2022-12-13T05:40:00.000000Z",
                    "mode": "point",
                    "form_template_id": 2,
                    "updated_at": "2022-12-16T12:04:18.000000Z",
                    "created_at": "2022-12-16T12:04:18.000000Z",
                    "id": 7
                }
            ],
            "multi_select": [
                {
                    "entry_id": 8,
                    "form_template_id": 3,
                    "updated_at": "2022-12-16T12:04:18.000000Z",
                    "created_at": "2022-12-16T12:04:18.000000Z",
                    "id": 7,
                    "selected_items": [
                        {
                            "item_id": 5,
                            "multi_select_input_id": 7,
                            "content_entry_id": null,
                            "user_id": 1,
                            "updated_at": "2022-12-16T12:04:18.000000Z",
                            "created_at": "2022-12-16T12:04:18.000000Z",
                            "id": 5
                        }
                    ]
                }
            ]
        }
    }
}
```

#### Update

PUT  `api/entries/{id}`
**Response**
Success: 200
```json
{
    "entry_template_id": 1,
    "header_input": {
        "name": "Sushi",
        "description": "",
        "form_template_id": 1
    },
    "text_input": [],
    "rating_input": [],
    "multi_select_input": [
        {
            "selected_items": [
                {
                    "item": {
                        "id": null,
                        "item_type_id": 1,
                        "name": "Rice"
                    },
                    "id": null,
                    "content_entry": null
                }
            ],
            "form_template_id": 3
        }
    ],
    "multi_datetime_input": [
        {
            "at": "2022-12-13 05:40",
            "from": "2022-12-13 05:40",
            "to": "2022-12-13 05:40",
            "mode": "point",
            "form_template_id": 2
        }
    ]
}
```

#### Delete

DELETE `api/entries/{id}`

**Response**

Success: 200
```json
{
	"message": "Deleted succesfuly"
}
```

## Entry templates

#### Index

GET `api/entry-templates`

**response**
code:200
```json
{
    "entry-templates": [
        {
            "id": 1,
            "name": "Food",
            "user_id": 1,
            "form_templates": [
                {
                    "id": 1,
                    "name": "Food",
                    "order": 0,
                    "form_type": "Header",
                    "item_type_id": null
                },
                {
                    "id": 2,
                    "name": "Time",
                    "order": 1,
                    "form_type": "MultiDatetime",
                    "item_type_id": null
                },
                {
                    "id": 3,
                    "name": "Ingredients",
                    "order": 2,
                    "form_type": "MultiSelect",
                    "item_type_id": 1
                },
                {
                    "id": 4,
                    "name": "Quantity",
                    "order": 3,
                    "form_type": "Quantity",
                    "item_type_id": null
                }
            ]
        },
        {
            "id": 2,
            "name": "Symptom",
            "user_id": 1,
            "form_templates": [
                {
                    "id": 5,
                    "name": "Symptom",
                    "order": 0,
                    "form_type": "Header",
                    "item_type_id": null
                },
                {
                    "id": 6,
                    "name": "Time",
                    "order": 1,
                    "form_type": "MultiDatetime",
                    "item_type_id": null
                },
                {
                    "id": 7,
                    "name": "Symptoms",
                    "order": 2,
                    "form_type": "MultiSelect",
                    "item_type_id": 2
                },
                {
                    "id": 8,
                    "name": "Intensity",
                    "order": 3,
                    "form_type": "Rating",
                    "item_type_id": null
                }
            ]
        }
    ],
}
```

#### Show

GET `api/entries/{id}`

**Response:**
[[#Entry templates#Index]]
```json
{
    "entry-template": [
        {
            "id": 1,
            "name": "Food",
            "user_id": 1,
            "form_templates": [
                {
                    "id": 1,
                    "name": "Food",
                    "order": 0,
                    "form_type": "Header",
                    "item_type_id": null
                },
                {
                    "id": 2,
                    "name": "Time",
                    "order": 1,
                    "form_type": "MultiDatetime",
                    "item_type_id": null
                },
                {
                    "id": 3,
                    "name": "Ingredients",
                    "order": 2,
                    "form_type": "MultiSelect",
                    "item_type_id": 1
                },
                {
                    "id": 4,
                    "name": "Quantity",
                    "order": 3,
                    "form_type": "Quantity",
                    "item_type_id": null
                }
            ]
        },
    ],
}
```

#### Create

POST `api/entry-templates`

``
**Body**
```json
"entry_template": {
            "id": 1,
            "name": "Food",
            "user_id": 1,
            "form_templates": [
                {
                    "id": 1,
                    "name": "Food",
                    "order": 0,
                    "form_type": "Header",
                    "item_type_id": null
                },
                {
                    "id": 2,
                    "name": "Time",
                    "order": 1,
                    "form_type": "MultiDatetime",
                    "item_type_id": null
                },
                {
                    "id": 3,
                    "name": "Ingredients",
                    "order": 2,
                    "form_type": "MultiSelect",
                    "item_type_id": 1
                },
                {
                    "id": 4,
                    "name": "Quantity",
                    "order": 3,
                    "form_type": "Quantity",
                    "item_type_id": null
                }
            ]
        },
```
**Response**
Success: 200
```json
"entry_template": {
            "id": 1,
            "name": "Food",
            "user_id": 1,
            "form_templates": [
                {
                    "id": 1,
                    "name": "Food",
                    "order": 0,
                    "form_type": "Header",
                    "item_type_id": null
                },
                {
                    "id": 2,
                    "name": "Time",
                    "order": 1,
                    "form_type": "MultiDatetime",
                    "item_type_id": null
                },
                {
                    "id": 3,
                    "name": "Ingredients",
                    "order": 2,
                    "form_type": "MultiSelect",
                    "item_type_id": 1
                },
                {
                    "id": 4,
                    "name": "Quantity",
                    "order": 3,
                    "form_type": "Quantity",
                    "item_type_id": null
                }
            ]
        },
```

#### Update

PUT  `api/entry-templates/{id}`

**body**:
```json
"entry-template": [
        {
            "id": 1,
            "name": "Food",
            "user_id": 1,
            "form_templates": [
                {
                    "id": 1,
                    "name": "Food",
                    "order": 0,
                    "form_type": "Header",
                    "item_type_id": null
                },
                {
                    "id": 2,
                    "name": "Time",
                    "order": 1,
                    "form_type": "MultiDatetime",
                    "item_type_id": null
                },
                {
                    "id": 3,
                    "name": "Ingredients",
                    "order": 2,
                    "form_type": "MultiSelect",
                    "item_type_id": 1
                },
                {
                    "id": 4,
                    "name": "Quantity",
                    "order": 3,
                    "form_type": "Quantity",
                    "item_type_id": null
                }
            ]
        },
```
**Response**
Success: 200
```json
"entry-template": [
        {
            "id": 1,
            "name": "Food",
            "user_id": 1,
            "form_templates": [
                {
                    "id": 1,
                    "name": "Food",
                    "order": 0,
                    "form_type": "Header",
                    "item_type_id": null
                },
                {
                    "id": 2,
                    "name": "Time",
                    "order": 1,
                    "form_type": "MultiDatetime",
                    "item_type_id": null
                },
                {
                    "id": 3,
                    "name": "Ingredients",
                    "order": 2,
                    "form_type": "MultiSelect",
                    "item_type_id": 1
                },
                {
                    "id": 4,
                    "name": "Quantity",
                    "order": 3,
                    "form_type": "Quantity",
                    "item_type_id": null
                }
            ]
        },
```

#### Delete

DELETE `api/entry-template/{id}`

**Response**

Success: 200
```json
{
	"message": "Deleted succesfuly"
}
```

## Items
#### Index

GET `api/items/{item_type_id}`

**response**
code:200
```json
{
    "items": [
        {
            "id": 1,
            "name": "Rice",
            "item_type_id": 1,
            "is_public": 0,
            "created_at": "2022-12-16T12:22:31.000000Z",
            "updated_at": "2022-12-16T12:22:31.000000Z"
        },
        {
            "id": 2,
            "name": "Tuna",
            "item_type_id": 1,
            "is_public": 0,
            "created_at": "2022-12-16T12:22:31.000000Z",
            "updated_at": "2022-12-16T12:22:31.000000Z"
        },
        {
            "id": 3,
            "name": "Soy sauce",
            "item_type_id": 1,
            "is_public": 0,
            "created_at": "2022-12-16T12:22:31.000000Z",
            "updated_at": "2022-12-16T12:22:31.000000Z"
        }
    ]
}
```

#### Show

GET `api/items/{item_type_id}/{id}`

**Response:**
```json
{
    "item": 
        {
            "id": 1,
            "name": "Rice",
            "item_type_id": 1,
            "is_public": 0,
            "created_at": "2022-12-16T12:22:31.000000Z",
            "updated_at": "2022-12-16T12:22:31.000000Z"
        }
    
}
```

#### Create

POST `api/items`

``
**Body**
```json
{
    "item": 
        {
            "id": 1,
            "name": "Rice",
            "item_type_id": 1,
            "is_public": 0,
            "created_at": "2022-12-16T12:22:31.000000Z",
            "updated_at": "2022-12-16T12:22:31.000000Z"
        }
    
}
```
**Response**
Success: 200
```json
{
    "item": 
        {
            "id": 1,
            "name": "Rice",
            "item_type_id": 1,
            "is_public": 0,
            "created_at": "2022-12-16T12:22:31.000000Z",
            "updated_at": "2022-12-16T12:22:31.000000Z"
        }
    
}
```

#### Update

PUT  `api/items/{item_type_id}/{id}`

**body**:
```json
{
    "item": 
        {
            "id": 1,
            "name": "Rice",
            "item_type_id": 1,
            "is_public": 0,
            "created_at": "2022-12-16T12:22:31.000000Z",
            "updated_at": "2022-12-16T12:22:31.000000Z"
        }
    
}
```
**Response**
Success: 200
```json
{
    "item": 
        {
            "id": 1,
            "name": "Rice",
            "item_type_id": 1,
            "is_public": 0,
            "created_at": "2022-12-16T12:22:31.000000Z",
            "updated_at": "2022-12-16T12:22:31.000000Z"
        }
    
}
```

#### Delete

**ROLE**: ADMIN

DELETE `api/items/{id}`

**Response**

Success: 200
```json
{
	"message": "Deleted succesfuly"
}
```


## Selected items
#### index

GET `api/selected-items`

**Response**

Success: 200

```json
"selected_items": [
	{
		"id": 1,
		"multi_select_input_id": 1,
		"item_id": 1,
		"user_id": 1,
		"content_entry_id": null,
		"created_at": "2022-12-13T21:05:38.000000Z",
		"updated_at": "2022-12-13T21:05:38.000000Z",
		"item": {
			"id": 1,
			"name": "Rice",
			"item_type_id": 1,
			"is_public": 0,
			"created_at": "2022-12-13T21:05:38.000000Z",
			"updated_at": "2022-12-13T21:05:38.000000Z"
		}
	}
]
```

#### Show

GET `api/selected-items/{id}`

**Response**
Success: 200
```json
"selected_item": 
	{
		"id": 1,
		"multi_select_input_id": 1,
		"item_id": 1,
		"user_id": 1,
		"content_entry_id": null,
		"created_at": "2022-12-13T21:05:38.000000Z",
		"updated_at": "2022-12-13T21:05:38.000000Z",
		"item": {
			"id": 1,
			"name": "Rice",
			"item_type_id": 1,
			"is_public": 0,
			"created_at": "2022-12-13T21:05:38.000000Z",
			"updated_at": "2022-12-13T21:05:38.000000Z"
		}
	}

```

#### Create

CREATE `api/selected-items`

**Body**

```json
"selected_items": 
	{
		"multi_select_input_id": 1,
		"item_id": 1,
		"user_id": 1,
		"content_entry_id": null,
		"item": {
			"id": 1,
		}
	}

```

**Response**

```json
"selected_item": 
	{
		"id": 1,
		"multi_select_input_id": 1,
		"item_id": 1,
		"user_id": 1,
		"content_entry_id": null,
		"created_at": "2022-12-13T21:05:38.000000Z",
		"updated_at": "2022-12-13T21:05:38.000000Z",
		"item": {
			"id": 1,
			"name": "Rice",
			"item_type_id": 1,
			"is_public": 0,
			"created_at": "2022-12-13T21:05:38.000000Z",
			"updated_at": "2022-12-13T21:05:38.000000Z"
		}
	}
```

#### Delete


DELETE `api/selected-items/{id}`

**Response**

Success: 200
```json
{
	"message": "Deleted succesfuly"
}
```

## Form templates

#### Index
GET `api/form-templates`

```json
"form_templates": [
	{
		"id": 1,
		"name": "Food",
		"order": 0,
		"form_type": "Header",
		"item_type_id": null
	},
	{
		"id": 2,
		"name": "Time",
		"order": 1,
		"form_type": "MultiDatetime",
		"item_type_id": null
	},
]
```

#### Show
GET `api/form-templates/{id}`

```json
"form_template": 
{
	"id": 1,
	"name": "Food",
	"order": 0,
	"form_type": "Header",
	"item_type_id": null
}
```

#### Create
CREATE `api/form-templates`

**Body**
```json
"form_templates": [
	{
		"name": "Food",
		"order": 0,
		"form_type": "Header",
		"item_type_id": null
	},
	{
		"name": "Time",
		"order": 1,
		"form_type": "MultiDatetime",
		"item_type_id": null
	},
```

**Response**
```json
"form_templates": [
	{
		"id": 1,
		"name": "Food",
		"order": 0,
		"form_type": "Header",
		"item_type_id": null
	},
	{
		"id": 2,
		"name": "Time",
		"order": 1,
		"form_type": "MultiDatetime",
		"item_type_id": null
	},
```
#### Delete

DELETE `api/form-templates`
**Response**

Success: 200
```json
{
	"message": "Deleted succesfuly"
}
```
