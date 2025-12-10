# Repo-Scraper

A prototype solution to skim through all public repositories of an organization and get all updated `README.md` files.

## Setup

### ... locally for development and testing purposes

- Clone this repository to your local workstation.
- Create a folder called `secrets` in your local working directory.
- Create a GitHub **Personal access token**. A **Fine-grained token** with **Read-only access to public repositories** is recommended.
- Store the token as plain text in `secrets/github.pat`.
- Copy `env-template` to `.env`.
- In the `.env` file, enter the value for `GITHUB_ORG`. This will be the Organization whose public repositories are getting scraped. Non-organizations won't work.
- Run `docker compose up --build`.

The API is now up and running at `http://localhost:8080/docs`.  
Explore the fetched `README.md` files in the Docker volume `repo-scraper_repos_data`.
