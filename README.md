# Request Journey Atlas

An interactive, single-page guide that follows one **"Place order"** click through every layer of an
**Angular + Java Spring Boot microservices** e-commerce application, from the browser to the database and back.

**Live site:** https://anilkaushik1211.github.io/web-request-journey-atlas/

## What's inside

- **Animated story mode for everyone.** A letter travels from your laptop through the Wi-Fi router, the internet
  provider's tower and the DNS phonebook, gets locked by TLS, passes the CDN branch, a police officer (WAF),
  a traffic cop (load balancer), reception (API gateway), a fuse box (circuit breaker), the order clerk
  (Spring Boot service), a quick shelf (Redis) and a vault (database), then a Kafka announcement, and races back.
  Tick "Send a suspicious letter" to watch the guard stop an attack. No coding knowledge needed.
- **"In plain words"** analogy on every one of the 36 layers.
- **Engineer's console**: a live simulator that animates the request layer by layer, with 8 scenarios: happy path, CORS rejected,
  WAF block, expired JWT with silent refresh, rate limit, circuit breaker open, duplicate click (idempotency),
  and optimistic-lock stock conflict.
- **36 layers in 8 phases**: Client (Angular), Network (DNS, TCP, TLS, HTTP/2), Edge (CDN, WAF, ALB, Nginx/Ingress),
  Platform (OAuth2/JWT, API gateway, discovery, Resilience4j, service mesh), Service (Tomcat, Spring Security,
  Spring MVC, transactions, inter-service calls), Data (Redis, JPA/Hibernate, PostgreSQL, Kafka + outbox + saga,
  payment webhooks), Return trip, and Always-on (observability, config, Kubernetes, CI/CD, OWASP).
- For every layer: why it exists, what it does step by step, how the HTTP request looks at that point,
  a deep dive, copyable code (Angular, Spring Boot, YAML, Nginx, Kubernetes, SQL), common mistakes,
  interview questions and key terms.
- "You are here" tracking while scrolling, `j` / `k` keyboard navigation, progress ticks, cheat sheet and glossary.

## Run it

It is one static file with no build step. Open `index.html` in a browser, or serve the folder:

```bash
npx serve .
# or
python3 -m http.server 8000
```

To publish with GitHub Pages: Settings → Pages → Deploy from branch → `main` / root.

Domains (`shop.example.com`, `api.example.com`) and latency numbers are illustrative.
