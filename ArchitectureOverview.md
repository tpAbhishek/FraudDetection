
## Trade-Offs
Fraud detection systems require balancing high recall, which catches more fraud but increases false positives, against precise, low-recall models. System trade-offs involve choosing between real-time processing for instant detection or batch processing for lower costs, as well as managing API latency versus feature complexity.

---

## Key Architecture Decisions

### Event-Driven Processing

Used Azure Service Bus to decouple customer transactions from fraud processing, ensuring minimal impact on business applications while improving scalability and resilience.

---

### API-First Integration

Designed standard REST APIs for communication between frontend applications, core systems, fraud services, and CRM, enabling reusable and maintainable integrations.

---

### Configurable Rules Engine

Separated fraud rules from application logic, allowing business teams to adjust thresholds and matching criteria without requiring major code changes.

---

### Automated Case Management

Implemented event-based integration with Microsoft Dynamics 365 CRM, automatically creating fraud investigation cases whenever configured thresholds were exceeded.
