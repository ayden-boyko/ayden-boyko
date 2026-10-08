# Ayden Boyko

Software engineer (RIT '26, B.S. Software Engineering) based in San Francisco. I build full-stack products, backend systems, and AI-agent tooling, and I like shipping things I can actually use.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?logo=linkedin&logoColor=white)](https://linkedin.com/in/ayden-boyko-ajb)
[![Website](https://img.shields.io/badge/Website-ayden--boyko--website.vercel.app-black)](https://ayden-boyko-website.vercel.app/)
[![Email](https://img.shields.io/badge/Email-aydenboyko@gmail.com-red?logo=gmail&logoColor=white)](mailto:aydenboyko@gmail.com)

## Featured Projects

### Words of Perio: voice-driven dental charting
**React · Tauri · AWS Lambda · Cognito · PostgreSQL (RDS) · Moonshine STT**
Built at a dentist's request as a cheaper alternative to commercial voice-charting software. The dentist calls out findings and the chart fills in hands-free, so the assistant is free to help other patients. Speech-to-text runs on-device (Moonshine), so patient audio never reaches third-party servers. Charts export to PDF for the practice's patient database. It's in user testing at the practice, and I'm rebuilding the client in Tauri from their feedback.
[Live demo](https://words-of-perio.vercel.app/) · *Source is private; happy to walk through the code on a call.*

### AI Smart-Home Security Pipeline
**Python · Qwen3-VL · smolagents · DeepSeek · WebRTC · Raspberry Pi**
A local alternative to cloud camera vendors. An OpenCV motion gate skips idle footage before any model runs. Flagged frames go to Qwen3-VL for structured JSON classification, and a smolagents triage agent decides urgency, deduplicates alerts, and routes notifications.
[Repo](https://github.com/ayden-boyko/home-sec)

### Piranid: Go microservices on a Raspberry Pi Kubernetes cluster
**Go · K3s · gRPC · RabbitMQ · OpenTelemetry · Grafana/Tempo/Loki/Prometheus**
A K3s cluster (Pi 4B control plane, four Pi Zero 2W workers on a Cluster HAT) running Go microservices under 512MB–1GB of RAM per node. The goal was to work through service design, inter-service communication and observability under real hardware limits.
- **Auth service:** OAuth 2.0 authorization code flow with mandatory PKCE, RS256 JWTs, and a JWKS endpoint. Only the auth service holds a signing key, so a compromised service can verify tokens but not mint them.
- **Event queue and notifications:** an HTTP RabbitMQ administration API and a gRPC email/SMS delivery service with a queue consumer.
- **Observability:** OpenTelemetry traces, logs and metrics into Tempo, Loki, Prometheus and Grafana.
- **Quality:** 135 tests passing, `go vet` clean, race detector in CI.
[Repo](https://github.com/ayden-boyko/Piranid) · [Architecture docs](https://github.com/ayden-boyko/Piranid/tree/main/docs)

## Experience Highlights
- **Bespin Global (Platform Service Intern):** built a Claude + MCP + Cypress E2E testing agent that cut test time 73% (2m30s → 40s). Shipped an email campaign platform (Spring Boot, React) used by Sales and Marketing. Found a Go goroutine-pool bottleneck and cut send time from 30 min to 30 sec.
- **Maynooth University (Software Research Intern):** owned a React Native canine gait-analysis app with AI pose estimation, from prototype to limited release with Irish vet practices. Wrote the C++ camera layer on the Luxonis stack.
- **RIT (Software Engineering Intern):** applied TDD to a platform used by 1,000+ students and cut recorded bugs from 34 to 6 across two releases.

## Stack
**Languages:** Python, TypeScript, Go, Java, C++, SQL
**Frontend:** React, React Native, Next.js, Tauri
**Backend/Infra:** Node, Spring Boot, Flask, PostgreSQL, AWS (Lambda, Cognito, RDS), K3s, Docker, RabbitMQ, gRPC, GitHub Actions
**AI:** Claude API, MCP, smolagents, agentic workflows

## Earlier Work
- [MyChat](https://github.com/ayden-boyko/MyChat): real-time chat app (MongoDB, Express, React, Node, WebSockets) with rooms, DMs and message history.

Outside of code: rock climbing, cooking, and reading.
