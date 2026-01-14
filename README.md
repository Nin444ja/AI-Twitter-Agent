Here is the **same content with all emojis removed**.
Nothing else has been changed.

---

# AI Twitter Bot

An intelligent Twitter bot powered by **Gemini 2.5 Flash**, **LangGraph**, and **FastAPI**. Automatically generates and posts high-quality tweets with adaptive scheduling and comprehensive monitoring.

## Key Features

* **AI-Powered Content**: Uses Gemini 2.5 Flash with LangGraph workflow orchestration
* **Smart Scheduling**: Adaptive timing with performance-based adjustments (1-6 hours)
* **Real-time Dashboard**: Web interface for monitoring and control
* **Vercel Ready**: Optimized for serverless deployment with automatic cron jobs
* **Robust Error Handling**: Comprehensive retry logic and graceful degradation
* **Analytics**: Performance tracking and success rate monitoring

## Complete Documentation

For detailed setup instructions, deployment guides, API documentation, and advanced configuration, visit our comprehensive documentation:

**Complete Project Documentation**
[https://docs.google.com/document/d/1Gllc127UGPR7H2VsLTIDzKoPkcAl3aZYFwYluvnXItM/edit?usp=sharing](https://docs.google.com/document/d/1Gllc127UGPR7H2VsLTIDzKoPkcAl3aZYFwYluvnXItM/edit?usp=sharing)

## Quick Start

### 1. Prerequisites

* Python 3.8+
* Twitter Developer Account: [https://developer.x.com](https://developer.x.com)
* Google AI API Key: [https://ai.google.dev](https://ai.google.dev)

### 2. Setup

```bash
# Clone and install
git clone <your-repo-url>
cd twitter-bot
pip install -r requirements.txt

# Configure environment
cp .env.example .env
# Edit .env with your API keys
```

### 3. Run

```bash
# Development
python src/main.py --mode dev

# Production  
python src/main.py --mode prod

# Test setup
python src/main.py --mode test
```

Visit `http://localhost:8000` for the dashboard.

## Deploy to Vercel

1. **Deploy**: Connect your GitHub repo to [https://vercel.com](https://vercel.com)
2. **Environment Variables**: Add your API keys in Vercel dashboard
3. **Cron Jobs**: Automatically configured for every 3 hours

**Available Endpoints After Deployment:**

* `/` - Dashboard interface
* `/health` - Health check with component status
* `/api/trigger-tweet` - Manual tweet trigger
* `/api/cron/tweet` - Automated cron endpoint
* `/api/external/tweet` - External cron services support
* `/api/ping` - Simple uptime monitoring

## Environment Variables

```env
# Required
GEMINI_API_KEY=your_gemini_api_key
TWITTER_API_KEY=your_twitter_api_key
TWITTER_API_SECRET=your_twitter_api_secret
TWITTER_ACCESS_TOKEN=your_access_token
TWITTER_ACCESS_SECRET=your_access_secret

# Optional
BOT_STYLE=witty, tech-savvy, conversational
MIN_INTERVAL_HOURS=1
MAX_INTERVAL_HOURS=6
```

## Architecture

```
┌─────────────┐    ┌─────────────────┐    ┌─────────────┐
│ Vercel Cron │───▶│ LangGraph       │───▶│ Twitter API │
│ Every 3hrs  │    │ Workflow        │    │ Posting     │
└─────────────┘    │ ┌─────────────┐ │    └─────────────┘
                   │ │Context      │ │           │
                   │ │Analysis     │ │           ▼
                   │ └─────────────┘ │    ┌─────────────┐
                   │ ┌─────────────┐ │    │ Dashboard   │
                   │ │Tweet        │ │    │ Monitoring  │
                   │ │Generation   │ │    │ Analytics   │
                   │ └─────────────┘ │    └─────────────┘
                   │ ┌─────────────┐ │
                   │ │Validation & │ │
                   │ │Enhancement  │ │
                   │ └─────────────┘ │
                   └─────────────────┘
                          │
                          ▼
                   ┌─────────────────┐
                   │ Gemini 2.5      │
                   │ Flash AI        │
                   └─────────────────┘
```

## Technology Stack

* **AI Framework**: LangGraph + LangChain
* **AI Model**: Google Gemini 2.5 Flash
* **Web Framework**: FastAPI + TailwindCSS
* **Scheduling**: APScheduler with intelligent timing
* **Twitter API**: Tweepy with v1.1 & v2 support
* **Deployment**: Vercel serverless functions
* **Monitoring**: Real-time dashboard with analytics

## Features Deep Dive

### LangGraph Workflow

* **Context Analysis**: Time-based content optimization
* **Smart Generation**: Multi-model fallback system
* **Quality Validation**: Length, style, and duplicate checking
* **Content Enhancement**: Style improvement pipeline
* **Error Recovery**: Comprehensive retry mechanisms

### Intelligent Scheduling

* **Adaptive Timing**: Performance-based interval adjustments
* **Optimal Hours**: Posting during peak engagement times
* **Daily Limits**: Configurable tweet frequency controls
* **Rate Limiting**: Twitter API compliance

### Monitoring & Analytics

* **Real-time Dashboard**: Live status and controls
* **Performance Metrics**: Success rates and response times
* **Error Tracking**: Categorized failure analysis
* **Health Checks**: Component status monitoring

## Troubleshooting

### Common Issues

* **Missing API Keys**: Check environment variables in deployment
* **Rate Limits**: Monitor Twitter API usage and adjust intervals
* **Generation Errors**: Verify Gemini API key and quota
* **Deployment Issues**: Check Vercel function logs

### Support

* Check the complete documentation for detailed guides
* Review function logs in Vercel dashboard
* Test individual components locally first

## License

MIT License - see LICENSE file for details.

---

**Ready to deploy? Check out the complete setup guide for step-by-step instructions.**

LinkedIn:
[https://www.linkedin.com/in/mohammed-saif-anwar-ali-5ba848255/](https://www.linkedin.com/in/mohammed-saif-anwar-ali-5ba848255/)

---

If you want, I can also:

* Convert this into a **GitHub README.md**
* Make a **LinkedIn project post**
* Prepare a **resume-friendly project summary**
