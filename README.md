### QuickLaunch Endpoint

**Endpoint:** `GET /quicklaunch/{placeid}`

**Description:** This endpoint retrieves the Quick Launch URL for a given place ID. The Quick Launch URL allows users to join a private server for a specific game.

**Parameters:**
- `placeid` (str): The ID of the game's place.

**Response:**
- `200 OK`: Returns the Quick Launch URL in the response body.
- `500 Internal Server Error`: Returns an error message if an error occurs.

**Example Request:**
`GET /quicklaunch/12345`

**Example Response:**
```json
{
  "quicklaunch_url": "https://www.roblox.com/games/12345/gamename?privateserverlinkcode=abcde"
}
```
