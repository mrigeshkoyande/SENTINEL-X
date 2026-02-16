<div align="center">

# 🛡️ SENTINEL-X

### Autonomous AI Security Agent Platform for Real-Time Threat Detection & Response

![Version](https://img.shields.io/badge/version-2.0-blue.svg)
![Python](https://img.shields.io/badge/python-3.9+-green.svg)
![Next.js](https://img.shields.io/badge/Next.js-14-black.svg)
![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Status](https://img.shields.io/badge/status-production-green.svg)

**[Features](#-key-features)** •
**[Quick Start](#-quick-start)** •
**[Architecture](#-architecture)** •
**[Documentation](#-documentation)** •
**[Demo](#-live-demo)**

---

</div>

## 🎯 Overview

**SENTINEL-X** is an enterprise-grade, autonomous AI security platform that revolutionizes cybersecurity operations. Powered by a multi-agent AI system, it provides real-time threat detection, root cause analysis, and automated response capabilities—all through a stunning, professional dashboard.

### Why SENTINEL-X?

- **🤖 Autonomous Operations**: 5 specialized AI agents work collaboratively to detect, analyze, and respond to threats without human intervention
- **⚡ Real-Time Detection**: Sub-second threat detection with continuous monitoring and adaptive learning
- **🧠 Intelligent Analysis**: Advanced root cause analysis and threat intelligence correlation
- **🎨 Professional Dashboard**: Enterprise-grade SOC interface with real-time visualizations
- **🔄 Self-Learning**: Continuously improves detection accuracy through machine learning
- **🌐 Cloud-Ready**: Terraform configurations for AWS deployment

---

## ✨ Key Features

### 🔍 Multi-Agent AI System

Five specialized AI agents powered by Google's Gemini API work in harmony:

| Agent | Purpose | Capabilities |
|-------|---------|-------------|
| **🛡️ Detection Agent** | First line of defense | Analyzes logs in real-time, identifies anomalies, assigns severity |
| **🔎 Intelligence Agent** | Threat enrichment | Correlates with threat databases, provides context and IOCs |
| **🧬 Root Cause Agent** | Deep analysis | Traces attack chains, identifies entry points and vulnerabilities |
| **⚡ Response Agent** | Automated mitigation | Executes countermeasures, blocks IPs, isolates systems |
| **📚 Learning Agent** | Continuous improvement | Analyzes outcomes, updates detection rules, improves accuracy |

### 📊 Professional Dashboard

Built with Next.js 14 and React, featuring:

- **8 Specialized Pages**: Overview, Threats, Events, Agents, Attack Map, Analytics, Reports, Settings
- **Real-Time Updates**: WebSocket-powered live data streaming
- **Interactive Visualizations**: Attack graphs, network maps, threat timelines
- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile
- **Dark Theme**: Cybersecurity-focused aesthetic with neon accents

### 🎯 Core Capabilities

- ✅ **Real-Time Log Analysis**: Process thousands of events per second
- ✅ **Automated Threat Response**: Block, isolate, and mitigate threats automatically
- ✅ **Attack Simulation**: Built-in scenarios for testing and training
- ✅ **Threat Intelligence**: Integration with global threat databases
- ✅ **Event Bus Architecture**: Scalable, asynchronous event processing
- ✅ **API-First Design**: RESTful and WebSocket APIs for integrations
- ✅ **Comprehensive Logging**: Detailed audit trails and forensic data

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────────┐
│                    SENTINEL-X ARCHITECTURE                      │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  ┌──────────────────┐         ┌──────────────────┐            │
│  │  Next.js Frontend │◄────────►│  FastAPI Backend │            │
│  │   (Port 3000)    │ WebSocket│   (Port 8000)   │            │
│  └──────────────────┘         └──────────────────┘            │
│           │                            │                        │
│           │                            ▼                        │
│           │                   ┌─────────────────┐              │
│           │                   │   Event Bus     │              │
│           │                   │  (Pub/Sub)      │              │
│           │                   └─────────────────┘              │
│           │                            │                        │
│           │                            ▼                        │
│           │          ┌─────────────────────────────────┐       │
│           │          │     AI Agent Swarm              │       │
│           │          ├─────────────────────────────────┤       │
│           │          │  Detection → Intel → RootCause  │       │
│           │          │       ↓                ↓        │       │
│           │          │     Response ← Learning         │       │
│           │          └─────────────────────────────────┘       │
│           │                            │                        │
│           ▼                            ▼                        │
│  ┌──────────────────┐         ┌──────────────────┐            │
│  │   User Actions   │         │  Security Tools  │            │
│  │  - View Threats  │         │  - Log Query     │            │
│  │  - Investigations│         │  - Threat Intel  │            │
│  │  - Reports       │         │  - Network Ctrl  │            │
│  └──────────────────┘         └──────────────────┘            │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

---

## 🚀 Quick Start

### Prerequisites

- Python 3.9+
- Node.js 18+
- Google Gemini API Key ([Get one here](https://makersuite.google.com/app/apikey))

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/SENTINEL-X.git
   cd SENTINEL-X
   ```

2. **Set up the backend**
   ```bash
   # Install Python dependencies
   pip install -r requirements.txt
   
   # Configure environment
   echo "GOOGLE_API_KEY=your_api_key_here" > .env
   ```

3. **Set up the dashboard**
   ```bash
   cd dashboard
   npm install
   ```

4. **Launch SENTINEL-X**
   
   **Terminal 1 - Backend:**
   ```bash
   python api/server.py
   ```
   
   **Terminal 2 - Frontend:**
   ```bash
   cd dashboard
   npm run dev
   ```

5. **Access the dashboard**
   ```
   🌐 Open: http://localhost:3000
   ```

### Run Attack Simulation

Test the system with built-in attack scenarios:

```bash
python main.py
```

---

## 📁 Project Structure

```
SENTINEL-X/
├── agents/                 # AI Agent implementations
│   ├── detection_agent/    # Threat detection
│   ├── intel_agent/        # Threat intelligence
│   ├── root_cause_agent/   # RCA analysis
│   ├── response_agent/     # Automated response
│   └── learning_agent/     # Machine learning
├── api/                    # FastAPI server
├── dashboard/              # Next.js frontend
│   ├── app/               # Pages and routing
│   ├── components/        # React components
│   └── lib/               # Utilities
├── memory/                 # Event bus system
├── simulator/              # Attack scenarios
├── tools/                  # Security tools
├── terraform/              # Cloud deployment
├── main.py                 # Agent orchestration
└── requirements.txt        # Python dependencies
```

---

## 📚 Documentation

Comprehensive documentation is available:

| Document | Description |
|----------|-------------|
| [Architecture Guide](ARCHITECTURE.md) | System architecture and design |
| [Dashboard Guide](DASHBOARD_GUIDE.md) | Dashboard features and usage |
| [Button Reference](dashboard/BUTTON_REFERENCE.md) | Complete button mapping |
| [Style Guide](dashboard/STYLE_GUIDE.md) | UI design system |
| [Quick Start](dashboard/QUICKSTART.md) | Dashboard quick start |
| [Deployment Guide](DEPLOYMENT_COMPLETE.md) | Production deployment |
| [API Documentation](api/README.md) | API endpoints and usage |

---

## 🎨 Live Demo

### Dashboard Screenshots

**Main Overview**
```
┌─────────────────────────────────────────────────────────┐
│ ⚡ SENTINEL-X   Status: ACTIVE   14:23:45              │
├─────────────────────────────────────────────────────────┤
│  📊 Threats: 42    📋 Events: 1,247    🤖 Agents: 5   │
│                                                         │
│  [Attack Vector Graph]  [Agent Reasoning Panel]        │
│  [Threat Monitor]       [Live Log Feed]                │
│  [System Status]        [Network Map]                  │
└─────────────────────────────────────────────────────────┘
```

**Key Features:**
- 🎯 Real-time threat monitoring with color-coded severity
- 📈 Interactive attack vector graphs and analytics
- 🗺️ Geographic attack distribution maps
- 🤖 AI agent reasoning visibility
- 📊 Performance metrics and system health
- 🔔 Live event stream with filtering

---

## 🛠️ Technology Stack

### Backend
- **Python 3.9+** - Core language
- **FastAPI** - High-performance web framework
- **Google Gemini API** - AI/ML capabilities
- **WebSockets** - Real-time communication
- **AsyncIO** - Asynchronous operations

### Frontend
- **Next.js 14** - React framework
- **TypeScript** - Type safety
- **Tailwind CSS** - Styling
- **Shadcn/ui** - Component library
- **Lucide Icons** - Icon system

### Infrastructure
- **Terraform** - Infrastructure as Code
- **AWS** - Cloud platform
- **Docker** - Containerization

---

## 🔧 Configuration

### Environment Variables

Create a `.env` file:

```env
# Required
GOOGLE_API_KEY=your_gemini_api_key

# Optional
API_PORT=8000
DASHBOARD_PORT=3000
LOG_LEVEL=INFO
ENABLE_SIMULATION=true
```

### Dashboard Settings

Configure via the Settings page or `dashboard/.env.local`:

```env
NEXT_PUBLIC_API_URL=http://localhost:8000
NEXT_PUBLIC_WS_URL=ws://localhost:8000/ws
```

---

## 🧪 Testing

### Run Attack Simulations

```bash
# Brute force attack
python main.py

# Custom scenario
python simulator/attack_scenarios.py
```

### Test Agent System

```python
from agents.detection_agent.agent import ThreatDetectionAgent

agent = ThreatDetectionAgent()
result = await agent.analyze_log(log_data)
```

---

## 🚢 Deployment

### Quick Deploy to AWS

```bash
cd terraform
terraform init
terraform plan
terraform apply
```

See [DEPLOYMENT_COMPLETE.md](DEPLOYMENT_COMPLETE.md) for detailed instructions.

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- **Google Gemini** for powering the AI agents
- **Vercel** for Next.js framework
- **FastAPI** for the excellent Python framework
- The open-source cybersecurity community

---

## 📬 Contact

**Project Maintainer**: Mrigesh Koyande

- 🐙 GitHub: [@yourusername](https://github.com/yourusername)
- 📧 Email: your.email@example.com
- 🐦 Twitter: [@yourhandle](https://twitter.com/yourhandle)

---

<div align="center">

### ⭐ Star us on GitHub — it motivates us a lot!

**Built with ❤️ for the cybersecurity community**

[Report Bug](https://github.com/yourusername/SENTINEL-X/issues) •
[Request Feature](https://github.com/yourusername/SENTINEL-X/issues) •
[Documentation](ARCHITECTURE.md)

</div>