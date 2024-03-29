# Tableside: API Deploy

The production repo for Tableside's API.

## Local Setup

1. Clone this repo
2. Ensure Docker is installed
3. Generate a [Personal Access Token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens). Note that it must be the **classic** token
4. Create a docker configuration file at `.docker/config.json` with the following format:
```json
{
  "auths": {
    "ghcr.io": {
      "auth": "<YOUR-USERNAME>:<YOUR-GITHUB-PERSONAL-ACCESS-TOKEN>"
    }
  }
}
```
5. Create a `.env` file based on the `sample.env` file available. Generate your usernames and passwords.
6. Run `docker compose up -d`
7. Ensure all services start correctly.
8. Send all requests to `localhost:9080`
