# Week 1 Evidence Index

Screenshots extracted from the supplied project report and organized for repository use. Screenshots containing password values or password hashes have been redacted in this copy.

## Deployment and configuration

| Screenshot | What it documents |
|---|---|
| `screenshots/01-clone-wazuh-docker-repository.png` | Cloning the Wazuh Docker repository. |
| `screenshots/02-generate-certificates.png` | Certificate-generation step. |
| `screenshots/03-start-wazuh-docker-services.png` | Starting the Docker Compose deployment. |
| `screenshots/04-check-running-containers.png` | Checking running containers. |
| `screenshots/05-certificate-or-setup-terminal-output.png` | Additional terminal output from setup. |
| `screenshots/06-internal-users-config-redacted.png` | Internal user configuration with hash redacted. |
| `screenshots/07-docker-compose-password-config-redacted.png` | Compose environment configuration with secrets redacted. |
| `screenshots/08-dashboard-password-config-redacted.png` | Dashboard environment configuration with secrets redacted. |
| `screenshots/09-agent-installation-terminal.png` | Endpoint/agent installation terminal output. |
| `screenshots/10-wazuh-dashboard-overview.png` | Wazuh dashboard view. |
| `screenshots/11-windows-sysmon-setup.png` | Windows Sysmon setup page/step. |
| `screenshots/12-windows-agent-installation-terminal.png` | Windows agent installation terminal output. |
| `screenshots/13-windows-sysmon-install-output.png` | Windows setup output. |
| `screenshots/14-wazuh-events-dashboard.png` | Dashboard event view. |

## Event-generation and validation

| Screenshot | Test activity |
|---|---|
| `screenshots/15-ssh-brute-force-test.png` | SSH authentication-failure test activity. |
| `screenshots/16-ssh-brute-force-events.png` | Dashboard evidence related to SSH brute-force activity. |
| `screenshots/17-sudo-command-test.png` | Running a command with `sudo`. |
| `screenshots/18-sudo-command-events.png` | Dashboard event evidence related to the `sudo` activity. |
| `screenshots/19-create-linux-user-test.png` | Creating a Linux user. |
| `screenshots/20-new-user-events.png` | Dashboard evidence related to user creation. |
| `screenshots/21-failed-windows-logon-events.png` | Failed Windows logon event view. |
| `screenshots/22-windows-process-creation-events.png` | Windows process creation (`cmd`) event view. |

## Evidence quality notes

- The filenames describe the likely activity based on the report sequence; verify each event's timestamp, rule ID, and fields in the live dashboard before using the screenshot as formal detection proof.
- Keep a short note for each test with the endpoint, timestamp/time zone, expected result, observed result, and relevant rule ID.
- Never commit passwords, API credentials, private keys, or unredacted secret-bearing screenshots.
