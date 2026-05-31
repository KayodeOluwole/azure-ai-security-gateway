# AI Threat Model

## System Overview

The Azure AI Security Gateway provides secure access to Azure AI Foundry models through Azure API Management (APIM).

## Architecture

User/Application
↓
Entra ID
↓
JWT Authentication
↓
Azure API Management
↓
Prompt Injection Controls
↓
DLP Controls
↓
Azure Key Vault
↓
Private Endpoint
↓
Phi-4 Model
↓
Sentinel Monitoring

---

## Trust Boundaries

### Boundary 1 – Internet to APIM

Threats:

* Prompt Injection
* Denial of Service
* Credential Abuse

Controls:

* JWT Validation
* Rate Limiting
* APIM Security Policies

### Boundary 2 – APIM to Azure AI

Threats:

* Unauthorized Backend Access

Controls:

* Private Endpoint
* Private DNS

### Boundary 3 – APIM to Key Vault

Threats:

* Secret Theft

Controls:

* Managed Identity
* RBAC

---

## STRIDE Analysis

### Spoofing

Risk:

* Stolen JWT Tokens

Mitigation:

* JWT Validation
* Entra ID

### Tampering

Risk:

* Prompt Manipulation

Mitigation:

* Prompt Injection Controls

### Repudiation

Risk:

* User Denial of Activity

Mitigation:

* Sentinel Logging

### Information Disclosure

Risk:

* Secret Leakage

Mitigation:

* DLP Controls
* Key Vault

### Denial of Service

Risk:

* AI Cost Exhaustion

Mitigation:

* Rate Limiting

### Elevation of Privilege

Risk:

* Unauthorized Secret Access

Mitigation:

* Managed Identity
* RBAC
