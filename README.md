# Elal Habeeb 26 — Event Gallery

An event photo and video gallery for **Al Nahda Educational Services**, at **Nesto Mia Mall**.

## Docker

```bash
docker compose up -d --build
```

Visit http://localhost:8080.

Or build manually:

```bash
docker build -t elal-habeeb-gallery .
docker run --rm -p 8080:80 elal-habeeb-gallery
```

## Current limitations

This is a **front-end demonstration**. Files added using the upload form are saved in the organizer's **own browser IndexedDB**, not uploaded to the container or published for other visitors. Downloads are available only in the browser where the files were added. Browser storage quotas apply and clearing site data deletes these files.

For a public shared gallery, connect a server-side upload API, persistent object storage (e.g. Cloudflare R2 / S3), database metadata, and organizer authentication. Never expose a public unauthenticated upload endpoint.
