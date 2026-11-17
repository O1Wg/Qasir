# Qasir
A URL shortener with click analytics. 


## What it does
- Turns a long URL into a short 7-character code, or a custom alias you pick
- Redirects visitors fast, with Redis keeping the hot links in memory
- Records every click: time, referrer, country and device
- Shows stats per link: clicks per day, unique visitors, top referrers
- Lets users manage their links with an account or an API key
- Expires links on a date and blocks abuse with rate limits

## Stack
- Language: Python 3.12
- API: FastAPI + Pydantic
- Database: PostgreSQL 16, SQLAlchemy 2, Alembic migrations
- Cache & queue: Redis 7: cache, rate-limit counters, Streams
- Worker: Python process in a Redis consumer group
- Infra: Docker Compose, Nginx
- Quality: pytest, Ruff, GitHub Actions
