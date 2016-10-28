FORMAT: 1A
HOST: http://citytours.savvycom.vn/

# Citytour

simple API document of Citytour Project.

## Bus Collection [/api/bus/updatestatus]

### Update Bus State [POST]

+ Request (application/json)

        {
            "bus_name": "Katarina Bus",
            "lat": 21.2225894,
            "long": 105.2860107,
            "no_tourist": 40
        }
+ Response 200 (application/json)

        {
            "status": "success",
            "message": "Status updated",
            "data": {
                "id": 1,
                "lat": 21.2225894,
                "long": 105.2860107,
                "no_tourist": 40,
                "bus_id": 31,
                "createdAt": "2016-10-28T11:14:56.460Z",
                "updatedAt": "2016-10-28T11:14:56.460Z"
            }
        }
## Request Playlist [/api/playlist/get?{limit}&{skip}&{search}]
### Get List Playlist [GET]

+ Parameters

    + limit(optional, number, `2`)
    + skip(optional, number, `0`)
    + search(optional, string, ``)
    
+ Response 200 (application/json)

        {
            "status": "success",
            "message": "Request accept.",
            "recordsFiltered": 2,
            "recordsTotal": 5,
            "data": [
                {
                    "tracks": [],
                    "name": "demaciaworld",
                    "autoplay": false,
                    "no_tracks": 0,
                    "description": null,
                    "id": 4,
                    "createdAt": "2016-10-27T10:20:30.000Z",
                    "updatedAt": "2016-10-27T10:20:30.000Z"
                },
                {
                    "tracks": [
                        {
                            "file_name": "track003.mp3",
                            "display_name": "track003.mp3",
                            "language": [
                                "german"
                            ],
                            "lat": null,
                            "address": null,
                            "long": null,
                            "radius": 50,
                            "max_playing_time": null,
                            "id": 4
                        }
                    ],
                    "name": "NewState",
                    "autoplay": false,
                    "no_tracks": 1,
                    "description": "Bigbig world",
                    "id": 3,
                    "createdAt": "2016-10-27T10:19:15.000Z",
                    "updatedAt": "2016-10-28T09:13:43.000Z"
                }
            ]
        }
## Request Message [/api/message/get?{limit}&{skip}&{search}]
### Get List Message [GET]
+ Parameters

    + limit(optional, number, `2`)
    + skip(optional, number, `0`)
    + search(optional, string, ``)
+ Response 200 (application/json)

        {
            "status": "success",
            "message": "Request success",
            "recordsFiltered": 2,
            "recordsTotal": 2,
            "data": [
                {
                    "language": "german",
                    "content": "<p>so suck&nbsp;</p>\n",
                    "title": "google now",
                    "image": null,
                    "status": true,
                    "message_id": null,
                    "id": 5,
                    "createdAt": "2016-10-27T11:04:04.000Z",
                    "updatedAt": "2016-10-27T11:04:04.000Z",
                    "childs": []
                },
                {
                    "language": "german",
                    "content": "<p>gaugau</p>\n",
                    "title": "demaciaworld",
                    "image": null,
                    "status": true,
                    "message_id": null,
                    "id": 2,
                    "createdAt": "2016-10-27T10:28:57.000Z",
                    "updatedAt": "2016-10-28T07:56:01.000Z",
                    "childs": [
                        {
                            "language": "english",
                            "content": "<p>Hello every body! Nice to meet you in Berline tour today. Say something....</p>\n",
                            "title": "welcome to berline tour",
                            "image": null,
                            "status": null,
                            "message_id": 2,
                            "id": 10,
                            "createdAt": "2016-10-28T11:48:07.000Z",
                            "updatedAt": "2016-10-28T11:48:07.000Z"
                        }
                    ]
                }
            ]
        }
