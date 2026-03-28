# CrewAI Product Research API

Backend API for AI-powered product research and dropshipping analysis.

## Deployment

Deployed on Render.com as a Python web service.

## Environment Variables

Set these in Render dashboard:

| Variable | Description | Required |
|----------|-------------|----------|
| `OPENAI_API_KEY` | OpenAI API key | Yes |
| `API_KEY` | Secret API key for authentication | Yes |
| `SERPER_API_KEY` | Serper.dev API for web search | Optional |

## API Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/api/v1/research` | POST | Start product research |
| `/api/v1/status/{run_id}` | GET | Check research status |
| `/health` | GET | Health check |
| `/docs` | GET | Interactive API docs |

## Usage Example

```bash
# Start research
curl -X POST https://your-api.onrender.com/api/v1/research \
  -H "Content-Type: application/json" \
  -d '{"product_name": "LED desk lamp"}'

# Check status
curl https://your-api.onrender.com/api/v1/status/{run_id}
