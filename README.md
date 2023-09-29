# rbxserversapi
API Documentation
Quicklaunch Endpoint
Endpoint
GET /quicklaunch/{placeid}
Description
This endpoint retrieves the quick launch URL for a given place ID. The quick launch URL allows users to join a private server for a specific game.
Parameters
**placeid** (str): The ID of the game's place.
Response
200 OK: Returns the quick launch URL in the response body.
500 Internal Server Error: Returns an error message if an error occurs.
Example
**Request:**
``json
GET /quicklaunch/12345
``
``json
Response:
{
  "quicklaunch_url": "https://www.roblox.com/games/12345/GameName?privateServerLinkCode=ABCDE"
}
``
Games Endpoint
Endpoint
GET /games/{placeid}
Description
This endpoint retrieves game data for a given place ID. It fetches the game data from the "rbxservers.xyz" API.
Parameters
**placeid** (str): The ID of the game's place.
Response
200 OK: Returns the game data in the response body.
500 Internal Server Error: Returns an error message if an error occurs.
Example
**Request:**
``json
GET /games/12345
``
``json
Response:
{
  "background": "https://tr.rbxcdn.com/f2af6825817e1c0926f7dc808d4e7763/768/432/Image/Png",
  "blacklisted": false,
  "name": "Break In 2 (SECRET ENDING)",
  "placeid": 13864661000,
  "servercount": 56,
  "servers": [
    {
      "created": "24 / 09 / 23",
      "flags": {
        "robot": true
      },
      "id": "80f4ad25-9e6a-4085-8418-bfb49eca139e",
      "lastupdate": "1 minute ago",
      "name": "Unnamed Server 9289",
      "votes": {
        "negative": 0,
        "positive": 0
      }
    },
    {
      "created": "28 / 09 / 23",
      "flags": {
        "robot": true
      },
      "id": "a997ccfa-e0fc-4490-8a84-632a5e20e7df",
      "lastupdate": "40 minutes ago",
      "name": "Unnamed Server 6434",
      "votes": {
        "negative": 0,
        "positive": 0
      }
    }
  ],
  "thumbnail": "https://tr.rbxcdn.com/9afcce74b5d4a652f0583cee17a4fbb7/512/512/Image/Png"
}
``
Servers Endpoint
Endpoint
GET /servers/{serverId}
Description
This endpoint retrieves server data for a given server ID. It fetches the server data from the "rbxservers.xyz" API.
Parameters
**serverId** (str): The ID of the server.
Response
200 OK: Returns the server data in the response body.
500 Internal Server Error: Returns an error message if an error occurs.
Example
**Request:**
``json
GET /servers/0a5909fa-3224-4479-9f19-362d19655a16
``
``json
Response:
{
  "creator": null,
  "game": {
    "background": "https://tr.rbxcdn.com/f2af6825817e1c0926f7dc808d4e7763/768/432/Image/Png",
    "name": "Break In 2 (SECRET ENDING)",
    "placeid": 13864661000,
    "thumbnail": "https://tr.rbxcdn.com/9afcce74b5d4a652f0583cee17a4fbb7/512/512/Image/Png"
  },
  "server-awaitingmoderation": false,
  "server-created": 1695694500,
  "server-description": "No description provided.",
  "server-flags": {
    "robot": true
  },
  "server-isvalid": true,
  "server-lastchecked": 1695986115,
  "server-linkcode": "44290708073161174401707097642960",
  "server-name": "Unnamed Server 2410",
  "server-nextcheck": 1695986415,
  "server-uuid": "0a5909fa-3224-4479-9f19-362d19655a16",
  "success": true
}
``
