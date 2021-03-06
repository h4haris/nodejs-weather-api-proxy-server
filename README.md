# Node API Proxy Server

Server used for hiding API keys, rate limiting and caching. 

This uses the [OpenWeather API](https://openweathermap.org/api) but can be easily use as a boilerplate for any public API.

### Rate Limiting
- Limit no. of request to server within span of time. 
- E.g. in 10 mins only 50 requests can be fulfilled.
- This will stop people from spamming API endpoint.

### Caching
- Cache API response for no. of minutes before recalling API.

## Usage

### Install dependencies

```bash
npm install
```

### Run on http://localhost:5002

```bash
npm run dev
```

### Add public API info

Rename **.env.example** to **.env** and edit the values

If the public API URL is **https://api.openweathermap.org/data/2.5/weather?q={city}&appid={APIkey}**

- API_BASE_URL = "https://api.openweathermap.org/data/2.5/weather"
- API_KEY_NAME = "appid"
- API_KEY_VALUE = "YOUR API KEY"

You can add on any other query params as needed when hitting the /api endpoint such as https://yourdomain/api?q=detroit without having to add your key in the client

- Add new routes as you see fit
- Change rate limiting and caching to desired values

## Reference
See [Here](https://youtu.be/ZGymN8aFsv4)


