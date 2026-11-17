# commons-security-audit

1. Problem statement: Compliance frameworks (SOC2, ISO 27001) require tamper-evident, immutable audit trails for every security-relevant action (login, PII access, permission change).

2. Concepts and terminology: Immutable Audit Log, Non-repudiation, Structured JSON Audit Event, Cryptographic Hash Chaining.

3. Available technologies / algorithms: Logback, JSON structural encoders, HMAC-SHA256 log signing, Kafka / Elasticsearch appenders.

4. When to use what: Use across all services to record who did what, when, and from where for forensic and compliance reporting.

5. Java APIs and dependencies: SLF4J, Logback, Jackson ObjectMapper.

6. AWS equivalents: AWS CloudTrail, Amazon CloudWatch Logs Insights.

7. Architecture patterns: Event-Sourced Auditing, Asynchronous Log Shipping, Write-Once-Read-Many (WORM) storage pattern.

8. Security considerations: Audit logs must never contain plaintext secrets or full unmasked PII tokens.

9. Implementation examples: Spring AOP audit interceptor capturing method execution arguments, user principal, and timestamp into a signed JSON event.

10. References and further reading: CIS Benchmark Security Logging Guidelines.
