URL to create a user [POST] : https://asia-south1-mimetic-maxim-371511.cloudfunctions.net/userservice/api/v2/users/createUserForOrganization [staging url]

Request body : 

{
    "phoneNumber": {
        "countryCode": "+91",
        "number": "9137333463"
    }, 
    "organization": "GOODGLAMMGROUP",
    "apiKey": "shared api key encrypted using a public key"
}

Response : 

{
    "status": 200,
    "message": "Logged in successfully.",
    "data": {
        "accessToken": "accessTokenValue",
        "refreshToken": "refreshTokenValue",
        "expires_in": "2024-08-21T09:54:59.656Z",
        "user": {
            "id": "b297600e-9fbe-4ad8-a35a-6dfd9ab59534",
            "role": "patient",
            "phone_number": {
                "number": "2398292323",
                "countryCode": "+91"
            },
            "organization": "GOODGLAMMGROUP",
            "language_preference": "en",
            "is_verified": true,
            "last_logged_in": "2024-08-21T09:51:59.281Z",
            "active": true,
            "modified_date": "2024-08-21T09:51:59.311Z",
            "created_date": "2024-08-21T09:51:59.311Z",
            "ip": null,
            "location_info": null,
            "email": null,
            "date_of_birth": null,
            "gender": null,
            "device_tokens": null,
            "first_name": null,
            "last_name": null,
            "display_name": null,
            "address_list": null,
            "created_by": null,
            "colour_code": null,
            "social_id": null,
            "picture": null,
            "profile": null
        }
    }
}

Need to send userId, refreshToken, accessToken (returned from this API call) and action="external_embed" while sending a message to the flutter app. 

