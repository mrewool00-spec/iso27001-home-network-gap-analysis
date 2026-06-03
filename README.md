# ISO/IEC 27001:2022 Internal Audit & Cybersecurity Gap Analysis

## Executive Summary
This Governance, Risk, and Compliance (GRC) portfolio project demonstrates a comprehensive, real-world internal audit and defensive engineering lifecycle. Using the **ISO/IEC 27001:2022** international standard control framework, a rigorous security assessment was executed on a network infrastructure hosting critical academic and personal data assets. By identifying architectural vulnerabilities, masking operational evidence, and constructing a strategic Risk Treatment Plan, this project demonstrates the ability to translate technical flaws into actionable, risk-aware business decisions.

---

## 1. Project Scope & Environment
The assessment boundary encompasses all hardware components, networking infrastructure, cloud interfaces, and operational data pools under active management within the environment.

* **In-Scope Boundaries**: Local routing equipment, personal and academic endpoints, cloud storage backends, and critical data stores.
* **Out-of-Scope Boundaries**: Internet Service Provider (ISP) core physical routing networks and third-party employer-managed technical infrastructure.

### Hardware Asset Inventory
The network environment supports seven core technical assets categorized by operational ownership profiles:


| Asset ID | Device Type | Operating System | Network Connection | User Profile |
| :--- | :--- | :--- | :--- | :--- |
| **HW-01** | Network Gateway | Proprietary Firmware | Broadband (Fiber) | System Admin |
| **HW-02** | Desktop PC | Windows 11 | Ethernet | User 1 (Student) |
| **HW-03** | Laptop 1 | Windows 11 | Wireless (Production) | User 1 (Student) |
| **HW-04** | Laptop 2 | Windows 11 | Wireless (Production) | User 2 |
| **HW-05** | Tablet | Android | Wireless (Production) | User 2 |
| **HW-06** | Mobile Phone 1 | iOS | Wireless (Production) | User 1 |
| **HW-07** | Mobile Phone 2 | iOS | Wireless (Production) | User 2 |

### Data Classification Inventory
Critical data structures are classified by sensitivity levels to ensure the targeted deployment of technical safeguards:


| Data ID | Data Category | Storage Location | Sensitivity | Associated Hardware |
| :--- | :--- | :--- | :--- | :--- |
| **DT-01** | Passwords & Credentials | Local Encrypted Vault | Critical | HW-02, HW-03, HW-04, HW-06, HW-07 |
| **DT-02** | Financial & Tax Records | Localized / Cloud Storage | High | HW-02, HW-03, HW-04 |
| **DT-03** | Academic Records & Research | Student Information Portal | High | HW-02, HW-03 |
| **DT-04** | Personal Photos & Media | Secondary Cloud Storage Backup | Medium | HW-05, HW-06, HW-07 |

---

## 2. ISO 27001 Audit Findings & Gap Analysis
The infrastructure was audited against specific controls from Annex A of the ISO/IEC 27001:2022 framework.


| Control ID | ISO 27001 Control Name | Current Operational Finding | Compliance Status | Risk / Threat Exposure |
| :--- | :--- | :--- | :--- | :--- |
| **A.8.20** | Network Security | Primary Wi-Fi network utilizes modern encryption protocols with a unique, non-default pre-shared key. | **Compliant** | Low risk of unauthorized wireless over-the-air packet snooping. |
| **A.5.15** | Access Control | Local gateway administrative portal panel relies entirely on factory default hardware access credentials. | **Non-Compliant** | High risk; local network intruders can modify settings or disable defensive layers if they compromise the subnet. |
| **A.8.22** | Network Segregation | The isolated guest wireless network capability is currently disabled. Guest devices and critical endpoints share a local broadcasting space. | **Non-Compliant** | High risk of lateral movement; compromised visitor hardware can scan, target, and exploit academic endpoints. |

---

## 3. Strategic Risk Treatment & Remediation Plan
To minimize risk exposure while ensuring continuous academic and residential uptime, the following remediation roadmap was engineered:


| Control ID | Risk Level | Strategy | Proposed Action Plan (Remediation Steps) | Timeline |
| :--- | :--- | :--- | :--- | :--- |
| **A.5.15** | **High** | Mitigate | Log into the local gateway administrative portal, navigate to the credential configuration menu, change the factory access code to a unique 16+ character password, and securely store it in a digital vault. | Immediate |
| **A.8.22** | **High** | Mitigate | Access the gateway administration panel, toggle the isolated guest broadcast network to enabled, assign it a unique secure password, and migrate all untrusted hardware to this segment to ring-fence core environments. | Within 7 Days |
| **A.8.9** | **Medium** | Mitigate | Access the local gateway administration dashboard, navigate to the device tracking table history, and trigger a manual cache flush to remove all historical inactive guest connections from routing memory. | Within 24 Hours |

### Operational Timeline Justification
While Network Segregation (**A.8.22**) represents a High Risk, its remediation target is set for a 7-day window due to an operational dependency: the administrative portal page access credentials (**A.5.15**) must be changed and hardened first. Furthermore, provisioning a new guest broadcast network requires a scheduled maintenance window to ensure household academic operations experience zero service disruption.

---

## 4. Professional Evidence Handling & Data Sanitization
In alignment with enterprise Operational Security (OPSEC) frameworks and data privacy regulations, all raw technical evidence was subjected to rigorous sanitization protocols prior to public portfolio publication. 

* **SSID Masking**: Real wireless identifiers were fully redacted using solid opaque masking blocks to prevent geographic location mapping via open-source telemetry databases.
* **Hardware Asset Redaction**: Unique hostnames and device identifiers were entirely masked to shield internal infrastructure layouts from potential discovery scanning.
