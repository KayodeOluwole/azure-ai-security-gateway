# AI Security Risk Register

| ID     | Risk                      | Likelihood | Impact   | Mitigation                     |
| ------ | ------------------------- | ---------- | -------- | ------------------------------ |
| AI-001 | Prompt Injection          | High       | High     | APIM Prompt Controls           |
| AI-002 | Sensitive Data Disclosure | High       | High     | DLP Controls                   |
| AI-003 | Credential Exposure       | Medium     | Critical | Credential Protection Policies |
| AI-004 | Unauthorized Access       | Medium     | High     | JWT Authentication             |
| AI-005 | Secret Theft              | Medium     | Critical | Key Vault + Managed Identity   |
| AI-006 | AI Service DoS            | Medium     | High     | Rate Limiting                  |
| AI-007 | Source Code Exposure      | Medium     | High     | Source Code Protection Rules   |
| AI-008 | Backend Exposure          | Medium     | High     | Private Endpoint               |

## Residual Risks

The following risks remain partially mitigated:

* Indirect Prompt Injection
* RAG Poisoning
* Agent Tool Abuse
* Excessive Token Consumption

## Future Enhancements

* Azure AI Content Safety
* Agent Security Controls
* RAG Security Validation
* Advanced Sentinel Analytics
