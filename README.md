# 🧠 AI Policy Copilot

An AI-powered web application that helps businesses automatically generate, manage, and audit AI usage policies with compliance support for GDPR, ISO/IEC 42001, and other frameworks.

## 🚀 Features

### 📝 AI Policy Generator
- Generate comprehensive AI usage policies based on company information
- Industry-specific policy templates
- Compliance framework integration (GDPR, ISO 42001, NIST AI RMF, etc.)
- Professional, executive-ready policy documents

### 🔍 AI Tools Audit
- Upload or manually enter AI tools for risk assessment
- Automated compliance gap analysis
- Risk mitigation recommendations
- Policy alignment suggestions

### 📋 Policy Library
- Version control and change tracking
- Policy history and diff views
- Export capabilities (PDF, DOCX, TXT)
- Search and filter functionality

### 🛡️ Compliance Support
- GDPR compliance mapping
- ISO/IEC 42001 framework integration
- NIST AI Risk Management Framework
- EU AI Act compliance
- HIPAA and CCPA support

## 🏗️ Architecture

```
ai-policy-copilot/
├── backend/                 # FastAPI backend with LangChain
│   ├── main.py             # Main API application
│   ├── endpoints/          # API endpoint modules
│   ├── models/            # Database models
│   └── services/          # Business logic services
├── ui/                     # Streamlit frontend
│   ├── main.py            # Main Streamlit app
│   └── pages/             # Page modules
├── data/                   # Sample policies and templates
├── db/                     # Database configuration
├── auth/                   # Firebase authentication
├── terraform/              # Infrastructure as Code
│   ├── main.tf            # Main Terraform configuration
│   └── variables.tf       # Terraform variables
├── requirements.txt        # Backend dependencies
├── ui/requirements.txt     # Frontend dependencies
├── deploy.sh              # Deployment script
└── README.md              # This file
```

## 🛠️ Tech Stack

- **Backend**: FastAPI (Python)
- **LLM Engine**: LangChain + OpenAI GPT-4
- **Frontend**: Streamlit
- **Database**: PostgreSQL + pgvector
- **Authentication**: Firebase Auth
- **Infrastructure**: Terraform + DigitalOcean
- **Hosting**: DigitalOcean Droplets

## 🚀 Quick Start

### Prerequisites

1. **Python 3.8+**
2. **OpenAI API Key**
3. **PostgreSQL** (optional, SQLite for development)
4. **Terraform** (for production deployment)

### Local Development

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd ai-policy-copilot
   ```

2. **Set up environment variables**
   ```bash
   cp env.example .env
   # Edit .env with your OpenAI API key and other settings
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   pip install -r ui/requirements.txt
   ```

4. **Run the application**
   ```bash
   ./deploy.sh
   ```

5. **Access the application**
   - 🌐 Backend API: http://localhost:8000
   - 🎨 Streamlit UI: http://localhost:8501
   - 📚 API Docs: http://localhost:8000/docs

### Production Deployment

1. **Set up Terraform**
   ```bash
   cd terraform
   terraform init
   ```

2. **Configure DigitalOcean token**
   ```bash
   export TF_VAR_do_token="your_digitalocean_token"
   ```

3. **Deploy infrastructure**
   ```bash
   terraform plan
   terraform apply
   ```

4. **Deploy application**
   ```bash
   # SSH to the droplet and deploy the application
   ssh root@<droplet_ip>
   ```

## 📋 API Endpoints

### Policy Management
- `POST /api/policies/generate` - Generate new AI policy
- `GET /api/policies/{policy_id}` - Retrieve specific policy
- `GET /api/policies` - List all policies

### Audit Services
- `POST /api/audit` - Audit AI tools for risks and compliance

### Health Check
- `GET /api/health` - Application health status

## 🔧 Configuration

### Environment Variables

```bash
# OpenAI Configuration
OPENAI_API_KEY=your_openai_api_key_here

# Database Configuration
DATABASE_URL=postgresql://username:password@localhost:5432/policy_copilot

# Firebase Configuration (for authentication)
FIREBASE_API_KEY=your_firebase_api_key
FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
FIREBASE_PROJECT_ID=your_project_id

# Application Configuration
ENVIRONMENT=development
DEBUG=true
SECRET_KEY=your_secret_key_here
```

## 🏢 Premium Features (Techvisory Branding)

The open-source version includes basic functionality. Premium features include:

- **Custom Branding**: Techvisory-branded interface
- **Enterprise Templates**: Industry-specific policy templates
- **Audit API**: RESTful API for internal audit teams
- **White-labeled Portal**: Custom domain and branding
- **Advanced Analytics**: Policy usage analytics and insights

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines

- Follow PEP 8 for Python code
- Add tests for new features
- Update documentation for API changes
- Use conventional commits for commit messages

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

- **Documentation**: [Wiki](link-to-wiki)
- **Issues**: [GitHub Issues](link-to-issues)
- **Discussions**: [GitHub Discussions](link-to-discussions)
- **Email**: support@techvisory.ai

## 🗺️ Roadmap

### Phase 1 (Current)
- ✅ Basic policy generation
- ✅ AI tools audit
- ✅ Policy library
- ✅ Compliance framework integration

### Phase 2 (Q2 2024)
- 🔄 Advanced policy templates
- 🔄 Multi-language support
- 🔄 Integration with HR systems
- 🔄 Advanced analytics dashboard

### Phase 3 (Q3 2024)
- 📋 Real-time compliance monitoring
- 📋 Automated policy updates
- 📋 Advanced risk scoring
- 📋 Enterprise SSO integration

## 🙏 Acknowledgments

- OpenAI for GPT-4 API
- LangChain for LLM orchestration
- Streamlit for the web interface
- FastAPI for the backend framework
- DigitalOcean for hosting infrastructure

---

**Built with ❤️ by the Techvisory team**

For enterprise inquiries: enterprise@techvisory.ai 