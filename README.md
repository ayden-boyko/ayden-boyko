# Ayden Boyko

Software engineer (RIT '26, B.S. Software Engineering) based in San Francisco. I build full-stack products, backend systems, and AI-agent tooling, and I like shipping things people actually use.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?logo=linkedin&logoColor=white)](https://linkedin.com/in/ayden-boyko-ajb)
[![Website](https://img.shields.io/badge/Website-ayden--boyko--website.vercel.app-black)](https://ayden-boyko-website.vercel.app/)
[![Email](https://img.shields.io/badge/Email-aydenboyko@gmail.com-red?logo=gmail&logoColor=white)](mailto:aydenboyko@gmail.com)

## Featured Projects

### Words of Perio: voice-driven dental charting  
*[July 2026] – present*  

[![Live Demo](https://img.shields.io/badge/Live_Demo-words--of--perio.vercel.app-2ea44f)](https://words-of-perio.vercel.app/)
![Source](https://img.shields.io/badge/Source-private-lightgrey)
![Status](https://img.shields.io/badge/Status-in_user_testing-blue)
![React](https://img.shields.io/badge/React-20232A?logo=react&logoColor=61DAFB)
![Tauri](https://img.shields.io/badge/Tauri-24C8D8?logo=tauri&logoColor=white)
![AWS](https://img.shields.io/badge/AWS_Lambda_·_Cognito_·_RDS-232F3E?logo=amazonaws&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)

Built at a dentist's request as a cheaper alternative to commercial voice-charting software. The dentist calls out findings and the chart fills in hands-free, so the assistant is free to help other patients. Speech-to-text runs on-device (Moonshine), so patient audio never reaches third-party servers. Charts export to PDF for the practice's patient database. It's in user testing at the practice, and I'm rebuilding the client in Tauri from their feedback.
*Source is private; happy to walk through the code on a call.*

### Piranid: Go microservices on a Raspberry Pi Kubernetes cluster  
*[Aug 2025] – [Aug 2026]*  

[![Repo](https://img.shields.io/badge/Repo-Piranid-181717?logo=github)](https://github.com/ayden-boyko/Piranid)
[![Docs](https://img.shields.io/badge/Docs-architecture-blue)](https://github.com/ayden-boyko/Piranid/tree/main/docs)
![Last Commit](https://img.shields.io/github/last-commit/ayden-boyko/Piranid)
![Go](https://img.shields.io/badge/Go-00ADD8?logo=go&logoColor=white)
![Kubernetes](https://img.shields.io/badge/K3s-326CE5?logo=kubernetes&logoColor=white)
![gRPC](https://img.shields.io/badge/gRPC-244c5a?logo=grpc&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?logo=rabbitmq&logoColor=white)
![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-425CC7?logo=opentelemetry&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?logo=grafana&logoColor=white)
![Raspberry Pi](https://img.shields.io/badge/Raspberry_Pi-A22846?logo=raspberrypi&logoColor=white)

A K3s cluster (Pi 4B control plane, four Pi Zero 2W workers on a Cluster HAT) running Go microservices under 512MB–1GB of RAM per node. The goal was to work through service design, inter-service communication and observability under real hardware limits.
- **Auth service:** OAuth 2.0 authorization code flow with mandatory PKCE, RS256 JWTs, and a JWKS endpoint. Only the auth service holds a signing key, so a compromised service can verify tokens but not mint them.
- **Event queue and notifications:** an HTTP RabbitMQ administration API and a gRPC email/SMS delivery service with a queue consumer.
- **Observability:** OpenTelemetry traces, logs and metrics into Tempo, Loki, Prometheus and Grafana.
- **Quality:** 135 tests passing, `go vet` clean, race-detector tested.

### Twitch-Canvas: collaborative charity stream canvas (senior capstone)  
*Jan 2026 – Aug 2026*  

![Team](https://img.shields.io/badge/Team-5_engineers-blue)
![Role](https://img.shields.io/badge/Role-charity_partner_lead-orange)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?logo=rabbitmq&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?logo=githubactions&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana_·_Tempo-F46800?logo=grafana&logoColor=white)

Five-engineer capstone, and I was the sole point of contact with the charity partner. I built the RabbitMQ messagcing layer (ordering guarantees, retries) and the CI/CD test stack, including headless Krita and merge-blocking E2E tests. The Grafana/Tempo dashboards I set up exposed a live-stream race condition.

### AI Smart-Home Security Pipeline  
*[July 2026] - present*  

[![Repo](https://img.shields.io/badge/Repo-home--sec-181717?logo=github)](https://github.com/ayden-boyko/home-sec)
![Last Commit](https://img.shields.io/github/last-commit/ayden-boyko/home-sec)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?logo=opencv&logoColor=white)
![WebRTC](https://img.shields.io/badge/WebRTC-333333?logo=webrtc&logoColor=white)
![Raspberry Pi](https://img.shields.io/badge/Raspberry_Pi-A22846?logo=raspberrypi&logoColor=white)
![smolagents](https://img.shields.io/badge/smolagents_·_Qwen3--VL_·_DeepSeek-FFD21E?logo=huggingface&logoColor=black)

A local alternative to cloud camera vendors. An OpenCV motion gate skips idle footage before any model runs. Flagged frames go to Qwen3-VL for structured JSON classification, and a smolagents triage agent decides urgency, deduplicates alerts, and routes notifications.

## Languages

[![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=ayden-boyko&layout=compact&hide_border=true&langs_count=8&hide=html,css,c,makefile)](https://github.com/ayden-boyko?tab=repositories)

*Based on my public repositories only. Production work at Bespin Global (Java, Go) and my private dental project (TypeScript) aren't included.*

## Experience
- **Bespin Global, Platform Service Intern** (May 2025 – Aug 2025): built a Claude + MCP + Cypress E2E testing agent that cut test time 73% (2m30s → 40s). Shipped an email campaign platform (Spring Boot, React) used by Sales and Marketing. Found a Go goroutine-pool bottleneck and cut send time from 30 min to 30 sec.
- **Maynooth University, Software Research Intern** (Sep 2025 – Nov 2025): owned a React Native canine gait-analysis app with AI pose estimation, from prototype to limited release with Irish vet practices. Wrote the C++ camera layer on the Luxonis stack.
- **Rochester Institute of Technology, Software Engineering Intern** (Jan 2025 – May 2025): applied TDD to a platform used by 1,000+ students and cut recorded bugs from 34 to 6 across two releases.

## Stack
**Languages:** Python, TypeScript, Go, Java, C++, SQL  
**Frontend:** React, React Native, Next.js, Tauri  
**Backend/Infra:** Node, Spring Boot, Flask, PostgreSQL, AWS (Lambda, Cognito, RDS), K3s, Docker, RabbitMQ, gRPC, GitHub Actions  
**AI:** Claude API, MCP, smolagents, agentic workflows  

## Earlier Work  
- [MyChat](https://github.com/ayden-boyko/MyChat) (*[Mon YYYY]*): real-time chat app (MongoDB, Express, React, Node, WebSockets) with rooms, DMs and message history.

Outside of code: rock climbing, cooking, and reading.
