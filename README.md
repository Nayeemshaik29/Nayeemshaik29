<!-- ===================== HEADER ===================== -->
<div align="center">

<img src="assets/hero-card.svg" width="100%" alt="Shaik Nayeem Basha, Java backend engineer. Weaving microservices, catching every bug. Spring Boot, Kafka, security. Open to Java backend roles in Hyderabad and Pune."/>

<img src="assets/hero-roles.svg" width="720" alt="Rotating summary: Java 25 and Spring Boot 4 backend engineer, event-driven microservices with Kafka, Spring Cloud and Resilience4j, security-first with SC-200 and CEH, Associate Software Engineer at LTM"/>

<br/>

<a href="https://nayeem-shaik.vercel.app"><img alt="Portfolio" src="https://img.shields.io/badge/Portfolio-c1121f?style=for-the-badge&logo=astro&logoColor=white"/></a>
<a href="https://www.linkedin.com/in/nayeem-shaik29/"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-1d4ed8?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
<a href="mailto:bashanayeem79@gmail.com"><img alt="Email" src="https://img.shields.io/badge/Email-c1121f?style=for-the-badge&logo=gmail&logoColor=white"/></a>
<a href="https://leetcode.com/u/ShaikNayeemBasha/"><img alt="LeetCode" src="https://img.shields.io/badge/LeetCode-1d4ed8?style=for-the-badge&logo=leetcode&logoColor=black"/></a>
<img src="https://komarev.com/ghpvc/?username=Nayeemshaik29&color=1f6feb" alt="profile views"/>

<br/>

<sub><a href="#about">About</a> · <a href="#stack">Stack</a> · <a href="#experience">Experience</a> · <a href="#softlaunch">SoftLaunch</a> · <a href="#projects">Projects</a> · <a href="#certs">Certifications</a> · <a href="#connect">Connect</a></sub>

</div>

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

<a id="about"></a>

## 🕷️ About Me

<div align="center">
<img src="assets/card-about.svg" width="100%" alt="About: backend engineer with a security mindset. Builds scalable REST APIs and event-driven microservices with Spring Boot, Spring Cloud and Kafka, with SC-200 and CEH background. Associate Software Engineer at LTM in Hyderabad, building SoftLaunch, KL University alumnus. 3 microservice platforms, 6 certifications, 8.85 CGPA."/>
</div>

<br/>

<div align="center">
<img src="assets/id-badge-card.svg" width="100%" alt="ID badge for Shaik Nayeem Basha, backend engineer in Hyderabad, cleared with SC-200 and CEH, open to roles. Dashboard: 38 public repositories, 3 microservice platforms, 6 certifications, 6 services in SoftLaunch, plus latest builds and stack by layer."/>
</div>

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

<a id="stack"></a>

## 🕸️ Tech Stack

<div align="center">

<img src="assets/card-tools.svg" width="100%" alt="Tools I build with: Java, Spring Boot, Spring Security, Spring Cloud, Hibernate, Maven, Apache Kafka, Redis, PostgreSQL, MySQL, MongoDB, ELK Stack, Docker, AWS, GitHub Actions, Git, GitHub, Linux, JWT, JUnit 5, Postman, Burp Suite, Wireshark and React."/>

<br/><br/>

<img src="assets/card-stack.svg" width="100%" alt="Tech stack. Backend: Java, Spring Boot, Spring Cloud, Spring Security, JPA and Hibernate, REST APIs. Messaging and resilience: Apache Kafka, Resilience4j, Eureka, API Gateway, OpenFeign. Data: PostgreSQL, MySQL, MongoDB, Redis. DevOps and observability: Docker, GitHub Actions, AWS EC2, Zipkin, ELK. Security: JWT, BCrypt, Microsoft Sentinel, Burp Suite, Nmap, Wireshark. Testing and tools: JUnit, Mockito, Postman, Maven, Git."/>

</div>

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

<a id="experience"></a>

## 🕷️ Experience

<div align="center">
<img src="assets/card-experience.svg" width="100%" alt="Experience. Associate Software Engineer at LTM, Hyderabad, February 2026 to present: develops backend features and REST APIs with Java and Spring Boot, builds SoftLaunch, writes SQL and debugs, takes part in code reviews. Java Full Stack Trainee at Student Tribe, Hyderabad, January to October 2025: built backend modules with Spring Boot, JPA, Hibernate and MySQL, developed and tested REST APIs, applied OOP and Git workflows."/>
</div>

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

<a id="softlaunch"></a>

## 🕸️ Spotlight: [SoftLaunch](https://github.com/Nayeemshaik29/softlaunch) 💘

<div align="center">
<a href="https://github.com/Nayeemshaik29/softlaunch"><img src="assets/card-softlaunch.svg" width="100%" alt="Spotlight: SoftLaunch, a cloud-native dating platform built as Spring Boot 4 microservices, in active development, 5 of 10 roadmap phases done. Stack: Java 25, Spring Boot 4.1, Spring Cloud, Kafka 4, PostgreSQL 17, Redis 7. Highlights: gateway security, race-safe matching, reliable events with idempotent consumers, retries and a dead-letter topic."/></a>
</div>

<div align="center">

<a href="https://github.com/Nayeemshaik29/softlaunch"><img alt="View SoftLaunch repository" src="https://img.shields.io/badge/View_Repository-c1121f?style=for-the-badge&logo=github&logoColor=white"/></a>

</div>

### 🏗️ Architecture

```mermaid
%%{init: {'theme':'base','themeVariables':{'primaryColor':'#0d1117','primaryBorderColor':'#e63946','primaryTextColor':'#e6edf3','lineColor':'#3b82f6','secondaryColor':'#0d1117','tertiaryColor':'#0d1117','clusterBkg':'#0d1117'}}}%%
flowchart LR
    C["📱 Client"] -->|HTTP + JWT| GW["🚪 API Gateway<br/>JWT filter · X-User-Id"]
    GW --> US["👤 User Service"]
    GW --> MS["💞 Match Service"]
    GW --> NS["🔔 Notification Service"]
    REG["🧭 Eureka"] -.- GW
    CFG["⚙️ Config Server"] -.- GW
    US --- UDB[("user_db")]
    MS --- MDB[("match_db")]
    MS --- RD[("Redis<br/>swipe quotas")]
    NS --- NDB[("notification_db")]
    MS -.->|"OpenFeign + Resilience4j"| US
    MS -->|match.created| K{{"Kafka (KRaft)"}}
    K --> NS
    K -.->|failures| DLT{{"DLT topics"}}
```

### ⚙️ Engineering Highlights

| Area | What I built | Why it matters |
|:--|:--|:--|
| 🔐 **Gateway security** | Global JWT filter that forwards `X-User-Id` and **strips client-supplied headers** | Stops identity spoofing; `/internal/**` routes are never exposed |
| ⏱️ **Auth hardening** | **Constant-time login** with a dummy hash check for unknown emails | Blocks timing-based user enumeration |
| 💞 **Race-safe matching** | Matches stored as a **sorted user pair** with a unique DB constraint | A↔B and B↔A can never create duplicate matches |
| 🚦 **Rate limiting** | **Redis `INCR` + TTL** daily swipe quota | Returns `429` when the quota runs out, and scales across instances |
| 🛡️ **Fault tolerance** | **OpenFeign + Resilience4j** circuit breaker and time limiter | Match Service keeps working when User Service is slow |
| 📨 **Event-driven** | Kafka `match.created` events with **idempotent consumers, retries and DLT** | No lost or duplicate notifications |
| 🧾 **Clean APIs** | **RFC 9457 `ProblemDetail`** errors, Bean Validation, a custom `@Adult` validator | Consistent errors and 18+ enforcement at the edge |
| 🗃️ **Data ownership** | **Database per service** (PostgreSQL 17) | Services stay independent and deploy separately |

<details>
<summary><b>🗺️ Roadmap: 5 of 10 phases done</b></summary>
<br/>

| Phase | Scope | Status |
|:--:|:--|:--:|
| 1 | Eureka, Config Server, API Gateway | ✅ |
| 2 | User Service: signup/login, BCrypt, JWT, rich profiles | ✅ |
| 3 | Gateway security: JWT filter, header anti-spoofing | ✅ |
| 4 | Match Service: swipes, matching, Redis quota, Feign + circuit breaker | ✅ |
| 5 | Kafka events, Notification Service, idempotency, retries + DLT | ✅ |
| 6 | Discovery: Redis GEO nearby feed + gRPC | 📋 |
| 7 | Chat: WebSocket/STOMP, MongoDB, disappearing messages | 📋 |
| 8 | Verification (18+ KYC mock) and safety (report/block) | 📋 |
| 9 | Observability: Zipkin, Prometheus, Grafana | 📋 |
| 10 | AI assistant: openers and scam detection (Ollama + pgvector) | 📋 |

</details>

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

<a id="projects"></a>

## 🕷️ More Projects

<div align="center">
<img src="assets/card-projects.svg" width="100%" alt="More projects. Skillora: professional networking platform with 6 microservices, handles 1,000+ requests per minute, Kafka at 5,000 events per second cut notification latency from 3 seconds to 500 milliseconds. BookingBlock: hotel booking platform, 8 REST APIs, 100+ listings under 150 ms, 200+ payments at 99.5 percent success. CI/CD Playground: git push to a live container on AWS EC2 with no manual steps. CredResolve: expense-sharing backend with groups, splits and balances."/>
</div>

<div align="center">

<a href="https://github.com/Nayeemshaik29/Skillora"><img alt="Skillora repository" src="https://img.shields.io/badge/Skillora-c1121f?style=for-the-badge&logo=github&logoColor=white"/></a>
<a href="https://github.com/Nayeemshaik29/BookingBlock"><img alt="BookingBlock repository" src="https://img.shields.io/badge/BookingBlock-1d4ed8?style=for-the-badge&logo=github&logoColor=white"/></a>
<a href="https://github.com/Nayeemshaik29/ci-cd-playground"><img alt="CI/CD Playground repository" src="https://img.shields.io/badge/CI/CD_Playground-c1121f?style=for-the-badge&logo=github&logoColor=white"/></a>
<a href="https://github.com/Nayeemshaik29/CredResolve-Assignment"><img alt="CredResolve repository" src="https://img.shields.io/badge/CredResolve-1d4ed8?style=for-the-badge&logo=github&logoColor=white"/></a>

</div>

<details>
<summary><b>📚 Learning and reference repos (click to expand)</b></summary>
<br/>

| Repo | What's inside |
|:--|:--|
| 🗃️ [Database-Optimization](https://github.com/Nayeemshaik29/Database-Optimization) | 18 techniques (indexing, partitioning, sharding, replication) with diagrams |
| 🧠 [Interview-DSA-Playbook](https://github.com/Nayeemshaik29/Interview-DSA-Playbook) | Pattern-based Java DSA prep with dry runs and complexity analysis |
| 🎨 [Design_Patterns](https://github.com/Nayeemshaik29/Design_Patterns) | Design patterns in Java using real-world scenarios |
| 📨 [kafka-learning-spring-boot](https://github.com/Nayeemshaik29/kafka-learning-spring-boot) | Kafka producer and consumer exchanging location events |
| 🧱 [object-oriented-programming](https://github.com/Nayeemshaik29/object-oriented-programming) | OOP guide from beginner to expert, interview-focused |

</details>

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

<a id="certs"></a>

## 🕸️ Certifications

<div align="center">
<img src="assets/card-certs.svg" width="100%" alt="Certifications: Microsoft Security Operations Analyst Associate SC-200, EC-Council Certified Ethical Hacker v12, Microsoft SC-900, Microsoft AI Business Professional, AWS Certified Cloud Practitioner, Anthropic Claude Code 101."/>
</div>

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

## 🕷️ GitHub Activity

<div align="center">
<img src="assets/card-activity.svg" width="100%" alt="GitHub activity: streak and contribution graph below."/>
</div>

<div align="center">

<img alt="GitHub contribution streak stats" height="165" src="https://streak-stats.demolab.com?user=Nayeemshaik29&hide_border=true&background=0d1117&ring=e63946&fire=3b82f6&currStreakNum=e6edf3&sideNums=e6edf3&currStreakLabel=e63946&sideLabels=3b82f6&dates=8b98b3" />

<img alt="GitHub contribution activity graph" width="100%" src="https://github-readme-activity-graph.vercel.app/graph?username=Nayeemshaik29&bg_color=0d1117&color=ffffff&line=e63946&point=3b82f6&area=true&area_color=1d4ed8&hide_border=true" />

### 🧠 LeetCode
<img alt="LeetCode profile card with solved-problem heatmap" src="https://leetcard.jacoblin.cool/ShaikNayeemBasha?theme=dark&font=Fira%20Code&ext=heatmap" />

</div>

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

<a id="connect"></a>

## 🕸️ Let's Connect

<div align="center">
<a href="https://nayeem-shaik.vercel.app"><img src="assets/card-connect.svg" width="100%" alt="Let&#x27;s connect. Email bashanayeem79@gmail.com, LinkedIn nayeem-shaik29, portfolio nayeem-shaik.vercel.app, LeetCode ShaikNayeemBasha. Open to Java backend roles, microservices and event-driven systems, and freelance work."/></a>
</div>

<div align="center">

<a href="https://nayeem-shaik.vercel.app/freelance"><img alt="Freelance services: ATS resumes, LinkedIn makeovers, backend APIs" src="https://img.shields.io/badge/Freelance_services-1d4ed8?style=for-the-badge&logo=astro&logoColor=white"/></a>

<a href="https://www.linkedin.com/in/nayeem-shaik29/"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-c1121f?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
<a href="mailto:bashanayeem79@gmail.com"><img alt="Gmail" src="https://img.shields.io/badge/Gmail-1d4ed8?style=for-the-badge&logo=gmail&logoColor=white"/></a>
<a href="https://leetcode.com/u/ShaikNayeemBasha/"><img alt="LeetCode" src="https://img.shields.io/badge/LeetCode-c1121f?style=for-the-badge&logo=leetcode&logoColor=black"/></a>
<a href="https://discord.gg/nayeem2756"><img alt="Discord" src="https://img.shields.io/badge/Discord-1d4ed8?style=for-the-badge&logo=discord&logoColor=white"/></a>

</div>

<img alt="Thanks for visiting footer wave" src="https://capsule-render.vercel.app/api?type=waving&color=0:c1121f,50:1d4ed8,100:0d1117&height=120&section=footer&text=Thanks%20for%20visiting!&fontSize=24&fontColor=ffffff&fontAlignY=70" width="100%"/>
