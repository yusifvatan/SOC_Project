# Wazuh Security Monitoring Lab

A hands-on lab for deploying Wazuh with Docker, enrolling Linux and Windows endpoints, and validating that security events appear in the Wazuh dashboard.

> **Project status:** Week 1 evidence documented. Later weeks can be added as the lab grows.

## Goals

- Deploy the Wazuh platform using Docker Compose.
- Configure the initial credentials and certificates.
- Connect a Linux web server and a Windows endpoint to Wazuh.
- Install Sysmon on Windows to provide additional endpoint telemetry.
- Generate test activity and confirm that relevant events are searchable in the dashboard.

## Repository layout

```text
.
├── README.md
├── architecture/
│   └── README.md
├── evidence/
│   └── week-01/
│       ├── README.md
│       └── screenshots/
├── reports/
│   └── week-01/
│       └── README.md
└── configs/
    └── examples/
```

- **`architecture/`** — high-level lab topology and component responsibilities.
- **`evidence/week-01/screenshots/`** — screenshots from setup and event-validation activities. Password-bearing screenshots have been redacted.
- **`evidence/week-01/README.md`** — quick index of the evidence.
- **`reports/week-01/README.md`** — Week 1 work log, validation notes, and limitations.
- **`configs/examples/`** — safe, sanitized configuration examples can be added here. Do not commit real secrets or full environment files.

## High-level workflow

1. Deploy the Wazuh components with Docker Compose.
2. Generate or configure the certificates and update the required credentials.
3. Start the services and verify their status.
4. Install and enroll endpoint agents.
5. Install Sysmon on Windows.
6. Generate controlled test activity.
7. Search for the resulting events in the Wazuh dashboard and save evidence.

See [Architecture](architecture/README.md) and the [Week 1 report](reports/week-01/README.md).

## Evidence captured in Week 1

- Wazuh Docker setup and service startup
- Credential configuration steps (sensitive values redacted)
- Dashboard access
- Linux/Windows endpoint setup
- SSH brute-force test activity
- A command run with `sudo`
- Linux user creation
- Failed Windows logon
- Windows process creation (`cmd`)

The screenshots document the activities shown in the original report. They do not by themselves prove that every detection rule or alert is correctly tuned.

## Reproducing the lab

The original report describes a Docker-based Wazuh deployment and endpoint setup, but does not include every prerequisite, host address, full configuration file, or exact command for every step. Use the official Wazuh documentation and adapt the commands to your environment.

- Wazuh documentation: https://documentation.wazuh.com/
- Wazuh Docker deployment: https://documentation.wazuh.com/current/deployment-options/docker/index.html

Do not publish credentials, API keys, private keys, certificates containing private material, internal IP details you consider sensitive, or unredacted configuration files. Use placeholders in examples and rotate any credential that was exposed in a public repository.

## Roadmap

- [x] Document initial Docker deployment and dashboard setup
- [x] Record endpoint setup and sample event validation
- [ ] Add sanitized deployment configuration examples
- [ ] Add a repeatable validation checklist for each event
- [ ] Add Week 2 and later reports as work continues
- [ ] Document alert/rule IDs and relevant fields where verified

## Disclaimer

This repository documents a learning lab. Run brute-force simulations and other test activity only on systems you own or are explicitly authorized to assess.
