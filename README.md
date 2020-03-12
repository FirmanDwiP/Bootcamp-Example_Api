# example-api

FORMAT: 1A
HOST:  https://private-7bc5e7-examplefirman.apiary-mock.com

# Ecommerce API

 E-commerce Api dokumen

## Categories Collection [/categories{?page}{?limit}]
### List Categories [GET]
Daftar Kategori

+ Parameters
    + page : 1 (number) - optional
    + limit : 10 (number) - optional

+ Response 200 (application/json)

        {
            "data":[
                {
                    "id": 1,
                    "name": "TAS",
                    "icon": "tas.png",
                },
                {
                    "id": 2,
                    "name": "BUKU",
                    "icon": "buku.png",
                },
                {
                    "id": 3,
                    "name": "SEPATU",
                    "icon": "sepatu.png",
                    "created_at": "7843731823",
                    "updated_at": "7843731823"
                }

            ],
            "meta": {
                "total": 50,
                "page": 1,
                "limit":10
                
            }
        }

### Create a New Category [POST]
Menambah Kategori

+ Request (application/json)

        {
            "name": "JAM",
            "icon": "jam.png"
        }

+ Response 201 (application/json)

    + Headers

            Location: /categories/8

    + Body

            {
                "name": "JAM",
                "icon": "jam.png",
            }

### Update Category [PUT /{id}]
Merubah kategori ID

+ Parameters
    + id (number) - ID of category must integer

+ Request (application/json)

        {
            "name": "JAM",
            "icon": "jam.png"
        }

+ Response 204 (application/json)


### Detail Category [GET /{id}]
Mendapatkan Detail ID

+ Parameters
    + id: 1 (number) - ID of category must integer

+ Response 200 (application/json)

        {
            "name": "JAM",
            "icon": "jam.png",
        }

### Delete Category [DELETE /{id}]
Hapus kategori

+ Parameters
    + id (number) - ID of category must integer

+ Response 204 (application/json)

