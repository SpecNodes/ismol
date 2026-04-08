
A small project using N8N where a user can create, read, update and delete URLs, mimicking a URL shortener. 

A telegram bot is used to dispatch commands to manage the URLs and an N8N webhook redirects the user to the actual URL.

![72](https://img.shields.io/badge/n8n-EA4B71.svg?style=for-the-badge&logo=n8n&logoColor=white)![](https://img.shields.io/badge/Docker-2496ED.svg?style=for-the-badge&logo=Docker&logoColor=white)

<img width="1019" height="730" alt="Pasted image 20260408231726" src="https://github.com/user-attachments/assets/9d9762aa-0931-4b6f-99ef-e7f57afa0cff" />

## Getting Started

### Prerequisites

- Must have [Docker](https://www.docker.com/products/docker-desktop/) installed in your system to host N8N.
- Airtable and access token to manage records.
- Telegram account to create and manage bot.
### Usage

1. Clone or download the repository.
   `git clone https://github.com/iy4h/KopiLink/tree/main?tab=readme-ov-file`
2. Run `docker compose up`
## Commands

| Command   | Description                                                        | Example                    |
| --------- | ------------------------------------------------------------------ | -------------------------- |
| /create   | Creates a new record in Airtable and returns the ID of the record. | /create https://github.com |
| /read     | Reads a record in Airtable linked to the user                      | /read 1                    |
| /read-all | Reads all records in Airtable linked to the user                   |                            |
| /update   | Updates the record in Airtable linked to the user                  |                            |
| /delete   | Deletes the record in Airtable linked to the user                  |                            |
## License

Distributed under the Unlicense License. See `LICENSE.txt` for more information.
