# 🚀 Anime Proxy

A high-performance, edge-ready M3U8 and binary proxy designed for seamless anime streaming. Built with [Hono](https://hono.dev/) and optimized for deployment on Vercel Edge, Railway, and Cloudflare Workers.

## 🌟 Features

- **M3U8 Rewriting**: Automatically rewrites HLS manifests to proxy segments and sub-manifests.
- **CORS Enabled**: Seamlessly handle cross-origin requests for streaming players.
- **Edge-Ready**: Optimized for Vercel Edge Runtime and Cloudflare Workers.
- **Relative Path Support**: Intelligent cookie-based redirection for relative segment paths.
- **Watch Order Scraper**: Built-in API to fetch anime watch orders using Chiaki.site.
- **Multi-Platform Support**: Ready to deploy on Vercel, Railway, and Cloudflare.

## 🚀 One-Click Deploy

Deploy your own instance of Anime Proxy with a single click:

[![Deploy on Railway](https://railway.app/button.svg)](https://railway.app/new/template?template=https://github.com/Vertixx01/anime-proxy)
[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/Vertixx01/anime-proxy)
[![Deploy to Cloudflare Workers](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/Vertixx01/anime-proxy)

## 🛠️ Usage

### Proxy a Stream
To proxy an M3U8 or any media file, use the `url` query parameter:
```text
GET /api?url=https://example.com/playlist.m3u8
```

### Info & Metadata
Get detailed project metadata and endpoint documentation:
```text
GET /api/info
```

### Status & Health
Check the service status (available as HTML badge or JSON):
```text
GET /api/status [Accept: application/json]
```

### Optional Parameters
- `origin`: Override the `Origin` and `Referer` headers for the upstream request.
- `headers`: Pass a JSON-encoded object for custom headers.
- `debug=1`: Enable debug information in the response (for manifests).

### Watch Order API
Fetch the recommended watch order for an anime using its AniList ID:
```text
GET /api/watch-order?id=12345
```

## 📦 Local Development

Ensure you have [Bun](https://bun.sh/) installed:

1. Clone the repository:
   ```bash
   git clone https://github.com/Vertixx01/anime-proxy.git
   cd anime-proxy
   ```

2. Install dependencies:
   ```bash
   bun install
   ```

3. Start the development server:
   ```bash
   bun run dev
   ```

## 📜 License
MIT
