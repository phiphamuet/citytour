# Citytour

simple API document of Citytour Project.

## Bus Collection [/api/busses]
### Create a Bus[POST]

 + Request(application/json)
{
    "name": "khongcanbiet2",
    "id": "ABCDEFG2"
}
 + Response 200
	{
    "status": "success",
    "message": "Bus created.",
    "data": {
        "id": "ABCDEFG2"
    }
}
 + Response 409
{
    "status": "error",
    "message": "Bus name already existed",
    "data": {
        "name": "khongcanbiet2"
    }
}
Or 
	{
    "status": "error",
    "message": "Bus id already existed",
    "data": {
        "id": "ABCDEFG2"
    }
}





## Bus Collection [/api/busses/{id}/status]

### Update Bus State [PUT]

+ Request (application/json)
	{
    "latitude": 21.2225894,
    "longitude": 106.3860107,
    "clients": [{
        "id": "1",
        "left": {
            "language": "DE",
            "plugged": true
        },
        "right": {
            "language": "EN",
            "plugged": false
        }
    }, {
        "id": "2",
        "left": {
            "language": "DE",
            "plugged": true
        },
        "right": {
            "language": "EN",
            "plugged": false
        }
    }]
}

+ Response 200 (application/json)

      	{
    "status": "success",
    "message": "Status updated!"
}


## Request Playlist [/api/playlists?{limit}&{skip}&{search}]
### Get List Playlist [GET]

+ Parameters

    + limit(optional, number, `2`)
    + skip(optional, number, `0`)
    + search(optional, string, ``)

+ Response 200 (application/json)

        	{
    "status": "success",
    "message": "Request accept.",
    "data": [{
        "tracks": [{
            "file_name": "track 001.mp3",
            "display_name": "Willkommen",
            "language": [
                "english",
                "french",
                "german"
            ],
            "lat": 51.0504999,
            "address": "Postpl., 01067 Dresden, Deutschland",
            "long": 13.732293199999958,
            "radius": 50,
            "max_playing_time": 13,
            "id": 61
        }, {
            "file_name": "track 002.mp3",
            "display_name": "Postplatz 2",
            "language": [
                "english",
                "french",
                "german"
            ],
            "lat": null,
            "address": null,
            "long": null,
            "radius": 50,
            "max_playing_time": 13,
            "id": 62
        }, {
            "file_name": "track 005.mp3",
            "display_name": "Altmarkt 5",
            "language": [
                "english",
                "french",
                "german"
            ],
            "lat": null,
            "address": null,
            "long": null,
            "radius": 50,
            "max_playing_time": 9,
            "id": 65
        }, {
            "file_name": "track 006.mp3",
            "display_name": "Zwinger 6",
            "language": [
                "english",
                "french",
                "german"
            ],
            "lat": null,
            "address": null,
            "long": null,
            "radius": 50,
            "max_playing_time": 9,
            "id": 66
        }, {
            "file_name": "track 014.mp3",
            "display_name": "Waldschlösschenbrücke 14",
            "language": [
                "english",
                "french",
                "german"
            ],
            "lat": null,
            "address": null,
            "long": null,
            "radius": 50,
            "max_playing_time": 76,
            "id": 74
        }, {
            "file_name": "track 012.mp3",
            "display_name": "Schillerplatz 12",
            "language": [
                "english",
                "french",
                "german"
            ],
            "lat": 51.052293,
            "address": "Schillerpl., Dresden, Deutschland",
            "long": 13.807849199999964,
            "radius": 50,
            "max_playing_time": 20,
            "id": 72
        }, {
            "file_name": "track 009.mp3",
            "display_name": "Grünes Gewölbe 9",
            "language": [
                "english",
                "french",
                "german"
            ],
            "lat": null,
            "address": null,
            "long": null,
            "radius": 50,
            "max_playing_time": 4,
            "id": 69
        }, {
            "file_name": "track 015.mp3",
            "display_name": "Neustadt 15",
            "language": [
                "english",
                "french",
                "german"
            ],
            "lat": null,
            "address": null,
            "long": null,
            "radius": 50,
            "max_playing_time": 28,
            "id": 75
        }],
        "name": "Mario Playlist",
        "description": "Just for testing",
        "id": 23,
        "createdAt": "2016-11-02T20:27:41.000Z",
        "updatedAt": "2016-11-02T20:27:41.000Z",
        "gpsAutoPlayPossible": false,
        "noTracks": 8
    }, {
        "tracks": [{
            "file_name": "track 001.mp3",
            "display_name": "Willkommen",
            "language": [
                "english",
                "french",
                "german"
            ],
            "lat": 51.0504999,
            "address": "Postpl., 01067 Dresden, Deutschland",
            "long": 13.732293199999958,
            "radius": 50,
            "max_playing_time": 13,
            "id": 61
        }, {
            "file_name": "track 002.mp3",
            "display_name": "Postplatz 2",
            "language": [
                "english",
                "french",
                "german"
            ],
            "lat": null,
            "address": null,
            "long": null,
            "radius": 50,
            "max_playing_time": 13,
            "id": 62
        }, {
            "file_name": "track 005.mp3",
            "display_name": "Altmarkt 5",
            "language": [
                "english",
                "french",
                "german"
            ],
            "lat": null,
            "address": null,
            "long": null,
            "radius": 50,
            "max_playing_time": 9,
            "id": 65
        }, {
            "file_name": "track 014.mp3",
            "display_name": "Waldschlösschenbrücke 14",
            "language": [
                "english",
                "french",
                "german"
            ],
            "lat": null,
            "address": null,
            "long": null,
            "radius": 50,
            "max_playing_time": 76,
            "id": 74
        }, {
            "file_name": "track 012.mp3",
            "display_name": "Schillerplatz 12",
            "language": [
                "english",
                "french",
                "german"
            ],
            "lat": 51.052293,
            "address": "Schillerpl., Dresden, Deutschland",
            "long": 13.807849199999964,
            "radius": 50,
            "max_playing_time": 20,
            "id": 72
        }, {
            "file_name": "track 013.mp3",
            "display_name": "Blasewitz 13",
            "language": [
                "english",
                "french",
                "german"
            ],
            "lat": 52.5488862,
            "address": "Reinickendorfer Str., 13347 Berlin, Deutschland",
            "long": 13.368825399999992,
            "radius": 50,
            "max_playing_time": 133,
            "id": 73
        }, {
            "file_name": "track 008.mp3",
            "display_name": "Großer Garten 8",
            "language": [
                "english",
                "french",
                "german"
            ],
            "lat": null,
            "address": null,
            "long": null,
            "radius": 50,
            "max_playing_time": 34,
            "id": 68
        }],
        "name": "Mario Playlist 2",
        "description": "just for testing",
        "id": 24,
        "createdAt": "2016-11-02T20:28:52.000Z",
        "updatedAt": "2016-11-03T07:56:18.000Z",
        "gpsAutoPlayPossible": false,
        "noTracks": 7
    }],
    "total": 23
}


## Request Message [/api/messages?{limit}&{skip}&{search}]
### Get List Message [GET]
+ Parameters

    + limit(optional, number, `3`)
    + skip(optional, number, `0`)
    + search(optional, string, ``)
+ Response 200 (application/json)

        	{
    "status": "success",
    "message": "Request accept.",
    "data": [{
        "language": "german",
        "content": "<p>aaaah</p>\n",
        "title": "mess1",
        "image": null,
        "status": true,
        "message_id": null,
        "id": 2,
        "createdAt": "2016-10-28T08:27:14.000Z",
        "updatedAt": "2016-10-28T08:27:14.000Z",
        "childs": []
    }, {
        "language": "german",
        "content": "<p>xdfffffffffffffffds</p>\n",
        "title": "image",
        "image": null,
        "status": false,
        "message_id": null,
        "id": 6,
        "createdAt": "2016-11-01T02:31:51.000Z",
        "updatedAt": "2016-11-01T02:31:51.000Z",
        "childs": []
    }, {
        "language": "german",
        "content": "<html>\n<head>\n\t<title></title>\n</head>\n<body>\n<p>csadcd</p>\n\n<p><img alt=\"\" src=\"data:image/png;base64,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\" style=\"height:100px; margin:0px; width:100px\" /></p>\n</body>\n</html>\n",
        "title": "picture",
        "image": null,
        "status": false,
        "message_id": null,
        "id": 8,
        "createdAt": "2016-11-02T01:51:44.000Z",
        "updatedAt": "2016-11-02T01:52:31.000Z",
        "childs": []
    }],
    "total": 3
}




