# Preliminaries

Make sure you've created a Spotify app. Visit this [site](https://developer.spotify.com/documentation/web-api) to learn more.

## Access Token

You can generate a token by passing in a client_id and client_secret, or by generating a token and passing it using the steps below.

### Generate via curl

If you prefer to generate your own token, execute this command on your terminal.

```bash
curl -X POST "https://accounts.spotify.com/api/token" \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "grant_type=client_credentials&client_id=your-client-id&client_secret=your-client-secret"
```

# MindsDB example commands

-- Create a model that registers Spotify data AI Tables

```sql
CREATE DATABASE my_spotify
With
ENGINE = 'spotify',
PARAMETERS = {
"Bearer": "", --- Spotify bearer TOKEN
};
```

-- Check model status