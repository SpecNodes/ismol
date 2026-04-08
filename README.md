# KopiLink — URL Shortener

<img width="864" height="965" alt="Pasted image 20260408193311" src="https://github.com/user-attachments/assets/2cf82d91-8bfc-43fe-b9d4-bca837dc5801" />


A Telegram bot named KopiLink that shortens URLs, stores them in Airtable with user and URL IDs, and tracks clicks. Stored links are accessible only to the submitting user.

## Prerequisites

- Docker
- Telegram account (bot token)
- Airtable account (API key and Base)

## Quick start

1. Install Docker  
    Follow Docker’s instructions: [https://docs.docker.com/engine/install/](https://docs.docker.com/engine/install/)
    
2. Import workflow into n8n  
    n8n → Workflows → Import → paste workflow.json
    
3. Set credentials in n8n
    
    - Telegram: Bot Token
    - Airtable: API Key / Personal Access Token, Base ID
    
4. Activate workflow in n8n
    

## Configuration notes

- Airtable schema (recommended):
    - Table: Links
    - Fields:
        - id (autonumber) — unique URL id
        - user_id (number) — Telegram user ID
        - URL (long Text) (URL sent by user)
        - clicks (number) — default 0
    
- Telegram bot behavior:
    
    - Accepts a message containing a URL → 
    - Supports Inline buttons for: /readall (list user’s links), /delete , /read (sends specific link), /create, /update → (uses callback queries)
