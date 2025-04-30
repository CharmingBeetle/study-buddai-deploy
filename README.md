# Deployment Central 🛠️

## Demo
[![Canva Video](https://img.shields.io/badge/▶-Watch%20Demo-blue)](https://www.canva.com/design/DAGk-OYPdDw/WaVbKaRpJ0vBj3ri2hu7AA/watch?utm_content=DAGk-OYPdDw&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=hf649f59812)

## 📂 Folder Structure
```
study_buddAI/
├── Study_BuddAI_FE/
├── Study_BuddAI_BE/
└── study-buddai-deploy/  # This repo
```

## 🚢 Full Stack Launch
```bash
# First time setup
chmod 600 .env.docker

# Start everything
docker-compose up --build
```

## 🔄 Update Workflow
1. Make changes in FE/BE repos
2. Rebuild affected services:
   ```bash
   docker-compose up --build frontend
   ```

## 🚨 Disaster Recovery
**Reset everything**:
```bash
docker-compose down -v --rmi all
rm -rf mysql-data/
```

## 🌍 Production Checklist
- [ ] Update `.env.docker` with real secrets
- [ ] Set `NODE_ENV=production` in backend
- [ ] Configure HTTPS in nginx