# Awesome Agent Security [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of resources for AI agent identity, authorization, coordination, and security.

As AI agents move from demos to production, securing them becomes critical. This list covers tools, frameworks, papers, standards, and best practices for making AI agents trustworthy.

**Contributions welcome!** See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

## Contents

- [Identity and Authentication](#identity-and-authentication)
- [Authorization and Policy](#authorization-and-policy)
- [Agent Coordination](#agent-coordination)
- [Sandboxed Execution](#sandboxed-execution)
- [Security Monitoring](#security-monitoring)
- [Standards and Protocols](#standards-and-protocols)
- [Papers and Research](#papers-and-research)
- [Incidents and Case Studies](#incidents-and-case-studies)
- [Talks and Presentations](#talks-and-presentations)
- [Books and Guides](#books-and-guides)

---

## Identity and Authentication

*Tools and platforms for giving AI agents verifiable identities.*

- [Authora Identity](https://authora.dev) - Cryptographic agent identities (Ed25519), RBAC, delegation chains (RFC 8693), MCP authorization, policy engines, approval workflows, audit logging. SDKs in TypeScript, Python, Rust, Go.
- [Permit.io](https://permit.io) - Fine-grained authorization with agentic identity support. Intent-based identity, MCP gateway, built on OPA/OPAL.
- [Oso](https://osohq.com) - Authorization framework with Polar policy language. Agent Security product with scope/watch/enforce/audit.
- [SPIFFE/SPIRE](https://spiffe.io) - Secure Production Identity Framework for Everyone. Workload identity standard applicable to agent systems.
- [Sigstore](https://sigstore.dev) - Keyless signing for software artifacts. Applicable to agent action signing.

## Authorization and Policy

*Frameworks for controlling what AI agents can do.*

- [OPA (Open Policy Agent)](https://openpolicyagent.org) - General-purpose policy engine using Rego language. Widely used for infrastructure policy, adaptable for agent authorization.
- [Cedar](https://www.cedarpolicy.com) - Policy language by AWS for fine-grained authorization. Used in Amazon Verified Permissions.
- [Casbin](https://casbin.org) - Authorization library supporting ACL, RBAC, ABAC models. Implementations in Go, Java, Node.js, Python.
- [OpenFGA](https://openfga.dev) - Fine-grained authorization inspired by Google Zanzibar. Good for relationship-based agent permissions.
- [Cerbos](https://cerbos.dev) - Access control with YAML policies. API-first, self-hosted.

## Agent Coordination

*Tools for coordinating multiple AI agents working together.*

- [AgentSync](https://authora.dev/products/agentsync) - File-level locking, sprint management, messaging, and coordination for AI coding agents on shared codebases.
- [LangGraph](https://github.com/langchain-ai/langgraph) - Framework for building stateful, multi-agent applications with LangChain.
- [CrewAI](https://github.com/crewAIInc/crewAI) - Framework for orchestrating autonomous AI agents with role-based task execution.
- [AutoGen](https://github.com/microsoft/autogen) - Microsoft's framework for building multi-agent conversational systems.
- [OpenHands](https://github.com/All-Hands-AI/OpenHands) - Platform for AI software development agents.

## Sandboxed Execution

*Secure environments for running AI agent code.*

- [AgentNet](https://authora.dev/products/agentnet) - Task execution marketplace with sandboxed workers, encrypted vault, Security Intelligence Platform (SIP).
- [E2B](https://e2b.dev) - Open-source sandboxed execution using Firecracker microVMs. Code interpretation and data analysis.
- [Modal](https://modal.com) - Cloud infrastructure for AI with sandboxed containers, GPU scaling, and batch processing.
- [Daytona](https://daytona.io) - Secure infrastructure for running AI-generated code with isolated environments.
- [Fly.io Machines](https://fly.io/docs/machines/) - Lightweight VMs for running untrusted workloads at the edge.

## Security Monitoring

*Detecting and responding to AI agent threats.*

- [Authora SIP](https://authora.dev/security) - Security Intelligence Platform with 36 detection rules, 8 SIEM export connectors (Splunk, Datadog, PagerDuty), SOAR callback API, OCSF/CEF compliance.
- [Caldera](https://caldera.mitre.org) - Automated adversary emulation by MITRE. Adaptable for testing agent security.
- [Falco](https://falco.org) - Cloud-native runtime security. Detects anomalous behavior in containers running agents.
- [Wiz](https://wiz.io) - Cloud security platform with AI workload protection.

## Standards and Protocols

*Standards relevant to AI agent security.*

- [MCP (Model Context Protocol)](https://modelcontextprotocol.io) - Protocol for AI model-tool interaction. Defines how agents access external tools and data.
- [RFC 8693 - OAuth 2.0 Token Exchange](https://tools.ietf.org/html/rfc8693) - Standard for delegated access. Foundation for user-to-agent and agent-to-agent delegation.
- [OCSF (Open Cybersecurity Schema Framework)](https://schema.ocsf.io) - Standardized security event format. Used by SIP for SIEM integration.
- [NIST AI Risk Management Framework](https://www.nist.gov/artificial-intelligence/ai-risk-management-framework) - Guidelines for managing AI risks including agent autonomy.
- [OWASP Top 10 for LLM Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/) - Security risks for LLM-based systems including prompt injection and insecure tool use.
- [Ed25519](https://ed25519.cr.yp.to) - High-speed, high-security digital signature scheme used for agent identity.

## Papers and Research

*Academic and industry research on AI agent security.*

- [Toolformer: Language Models Can Teach Themselves to Use Tools](https://arxiv.org/abs/2302.04761) - Foundational paper on LLM tool use.
- [ReAct: Synergizing Reasoning and Acting in Language Models](https://arxiv.org/abs/2210.03629) - Reasoning + acting paradigm for agents.
- [The Landscape of Emerging AI Agent Architectures](https://arxiv.org/abs/2404.11584) - Survey of multi-agent system architectures.
- [Prompt Injection Attacks Against LLM-Integrated Applications](https://arxiv.org/abs/2306.05499) - Security analysis of prompt injection in agent systems.
- [Not What You've Signed Up For: Compromising Real-World LLM-Integrated Applications](https://arxiv.org/abs/2302.12173) - Real-world attack vectors on LLM tool-calling systems.

## Incidents and Case Studies

*Real-world security incidents involving AI agents.*

- [LiteLLM Supply Chain Attack (2025)](https://www.wiz.io/blog/litellm-supply-chain-attack) - Compromised dependency in widely-used LLM proxy.
- [29 Million Secrets Leaked on GitHub (2024)](https://blog.gitguardian.com/secrets-leaks-2024-report/) - AI coding tools accelerating secret exposure.
- [ChatGPT Plugin Permission Escalation](https://embracethered.com/blog/posts/2023/chatgpt-plugin-vulns/) - Demonstration of cross-plugin attacks via shared context.

## Talks and Presentations

- [Simon Willison - Prompt Injection and AI Security](https://simonwillison.net/tags/security/) - Ongoing coverage of LLM security issues.
- [OWASP AppSec - LLM Security](https://owasp.org/www-project-top-10-for-large-language-model-applications/) - Community presentations on LLM application security.

## Books and Guides

- [LLM Security Guide](https://llmsecurity.net) - Comprehensive guide to securing LLM applications.
- [Anthropic's Responsible Scaling Policy](https://www.anthropic.com/index/anthropics-responsible-scaling-policy) - Framework for safely deploying capable AI systems.

---

## Contributing

Contributions are welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

## License

[![CC0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

This list is released under CC0. You can copy, modify, and distribute it without asking permission.
