# Capuzzella CLI

Command-line interface for the [Capuzzella](https://capuzzella.com) AI-Powered Website Builder.

Manage pages, publishing, scheduling, API keys, AI providers, email, and custom domains — all from your terminal.

## Requirements

- Node.js 18+

## Install

```bash
npm install -g capuzzella
```

## Setup

Set your API key and server URL:

```bash
export CAPUZZELLA_API_KEY=cap_...
export CAPUZZELLA_URL=https://your-instance.capuzzella.com
```

`CAPUZZELLA_URL` defaults to `http://localhost:3000` if not set.

## Usage

```
capuzzella <command> [options]
```

### Identity

```bash
capuzzella whoami
```

### Pages

```bash
capuzzella pages list
capuzzella pages get index.html
capuzzella pages save blog/post.html --file ./post.html
capuzzella pages delete blog/old.html
```

### Publishing

```bash
capuzzella publish all
capuzzella publish index.html
capuzzella unpublish index.html
capuzzella status index.html
```

### Scheduling

```bash
capuzzella schedule list
capuzzella schedule list all
capuzzella schedule add index.html --at 2026-04-01T09:00:00Z
capuzzella schedule get 1
capuzzella schedule cancel 1
```

### API Keys

```bash
capuzzella keys list
capuzzella keys create --name "CI Deploy" --role editor
capuzzella keys revoke 3
capuzzella keys delete 3
capuzzella keys audit 3
```

### AI Provider

```bash
capuzzella ai-provider get
capuzzella ai-provider set --provider anthropic --model claude-sonnet-4-20250514 --api-key sk-...
```

### Transactional Email

```bash
capuzzella email get
capuzzella email set --domain example.com --contact-email hello@example.com --api-key re_...
capuzzella email remove
```

### Custom Domains

```bash
capuzzella domains list
capuzzella domains add example.com
capuzzella domains delete <domain-id>
```

## License

See [LICENSE.md](LICENSE.md).
