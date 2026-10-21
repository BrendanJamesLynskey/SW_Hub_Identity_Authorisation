# Identity & Authorisation — Series Hub

Who is the user, and what may they (or their workload) do? A primer, seven decks on identity and federation, and three on authorisation, from password hashing to service meshes and gateways.

**Live index:** https://brendanjameslynskey.github.io/SW_Hub_Identity_Authorisation/

**Who this is for.** Engineers who build sign-in, single sign-on or service-to-service security, and anyone who has met the pieces over the years and wants them in order. No prior identity experience assumed.

**How to use it.** Start with the Primer, then read Identity & Access for who is the user and Authorisation for what may they do. Each deck is a self-contained Reveal.js presentation with a Markdown version.

## The reading order

### Part 1: Start here

The map of the field: history, threats, standards and the reading roadmap.

| # | Title | Description |
| --- | --- | --- |
| 01 | [Identity & Authorisation — A Primer](https://brendanjameslynskey.github.io/Identity_and_Authorisation_Primer/) ([md](https://github.com/BrendanJamesLynskey/Identity_and_Authorisation_Primer/blob/main/presentation.md)) | The gateway deck: why these problems exist, the four eras (mainframe, web, mobile and cloud, agent and wallet), the AuthN and AuthZ maps, the standards bodies, threats and their defences, build or buy, the regulatory backdrop, and a reading roadmap to the decks below |

### Part 2: Identity & Access

Who is the user, and how do they prove it to other systems? Authentication primitives, then the federation stacks that carry identity.

| # | Title | Description |
| --- | --- | --- |
| 02 | [Authentication Methods](https://brendanjameslynskey.github.io/Authentication_Methods/) ([md](https://github.com/BrendanJamesLynskey/Authentication_Methods/blob/main/presentation.md)) | Establishing who the user is: Argon2id hashing and NIST 800-63B policy, credential stuffing, factor classes and the AAL ladder, TOTP/HOTP, SMS, email and push trade-offs, WebAuthn, FIDO2 and passkeys, attestation, account recovery and risk-based auth |
| 03 | [OAuth — A Gentle Primer (Part 0)](https://brendanjameslynskey.github.io/OAuth_Primer/) ([md](https://github.com/BrendanJamesLynskey/OAuth_Primer/blob/main/presentation.md)) | No RFCs, no code: the valet-key mental model, AuthN against AuthZ, the password-sharing problem, "Sign in with Google" walked through, tokens, scopes and the MCP angle. Read first if delegated auth is new |
| 04 | [Introduction to OAuth (Part 1)](https://brendanjameslynskey.github.io/Introduction_to_OAuth/) ([md](https://github.com/BrendanJamesLynskey/Introduction_to_OAuth/blob/main/presentation.md)) | Interactive presentation on OAuth — purpose, history, OAuth 1.0a → 2.0 → 2.1, all grant types, PKCE, OpenID Connect, JWTs, DPoP/mTLS, BCP 240 attacks & defences, library and flow selection |
| 05 | [OAuth for MCP Servers (Part 2)](https://brendanjameslynskey.github.io/OAuth_for_MCP/) ([md](https://github.com/BrendanJamesLynskey/OAuth_for_MCP/blob/main/presentation.md)) | OAuth for the Model Context Protocol: the MCP authorisation profile, Resource Indicators, DPoP, the Docker MCP Gateway as an OAuth broker, and a tour of commercial and open-source identity providers |
| 06 | [Introduction to OpenID Connect](https://brendanjameslynskey.github.io/Introduction_to_OpenID_Connect/) ([repo](https://github.com/BrendanJamesLynskey/Introduction_to_OpenID_Connect)) | OIDC foundations: the ID token on top of OAuth, JWT validation, discovery and JWKS rotation, UserInfo, response types, logout, CIBA, OpenID Federation, FAPI 2.0, real-world provider quirks and workload OIDC for CI/CD |
| 07 | [Advanced OpenID Connect](https://brendanjameslynskey.github.io/Advanced_OpenID_Connect/) ([md](https://github.com/BrendanJamesLynskey/Advanced_OpenID_Connect/blob/main/presentation.md)) | The deep end: validation edge cases, PAR / JAR / JARM, FAPI 2.0, sender-constrained tokens, Token Exchange, OpenID Federation trust chains, eIDAS 2.0 and the EUDI wallet stack (SIOPv2, OpenID4VCI, OpenID4VP, ISO mDL) and migration playbooks |
| 08 | [SAML 2.0 & SCIM](https://brendanjameslynskey.github.io/SAML_and_SCIM/) ([md](https://github.com/BrendanJamesLynskey/SAML_and_SCIM/blob/main/presentation.md)) | The parallel enterprise stack: SAML roles, metadata, SSO flows, bindings and assertion validation, SAML attacks and defences, SAML against OIDC, SCIM 2.0 provisioning and group sync, IdP quirks and a B2B enterprise-readiness checklist |

### Part 3: Authorisation

What may the user or workload do, and where is it enforced? Foundations, then east-west service-to-service, then north-south at the edge.

| # | Title | Description |
| --- | --- | --- |
| 09 | [Authorization Models](https://brendanjameslynskey.github.io/Authorization_Models/) ([md](https://github.com/BrendanJamesLynskey/Authorization_Models/blob/main/presentation.md)) | The decision layer: PEP/PDP/PAP/PIP, the DAC → MAC → RBAC → ABAC → ReBAC arc, Cedar, Zanzibar and relationship tuples, policy-as-code engines compared (OPA, Cedar, OpenFGA, SpiceDB, Casbin), caching, audit and migration |
| 10 | [Workload Identity & Service-Mesh AuthZ](https://brendanjameslynskey.github.io/Workload_Identity_AuthZ/) ([md](https://github.com/BrendanJamesLynskey/Workload_Identity_AuthZ/blob/main/presentation.md)) | East-west authorisation: SPIFFE and SPIRE, service-mesh AuthZ in Istio, Linkerd and Cilium, mTLS at scale, cloud workload identity (IRSA, GCP and Azure), Kubernetes projected tokens, and workload identity for AI agents and MCP servers |
| 11 | [Edge & Gateway AuthZ](https://brendanjameslynskey.github.io/Edge_and_Gateway_AuthZ/) ([md](https://github.com/BrendanJamesLynskey/Edge_and_Gateway_AuthZ/blob/main/presentation.md)) | North-south authorisation: JWT against introspection at the edge, Envoy `ext_authz`, API-gateway authorisers, Cloudflare Access, rate limits as policy, Token Exchange at the edge, GraphQL and webhook patterns, and the MCP Gateway as the AI-era edge |

## Related

- [Introduction to Web Authentication](https://brendanjameslynskey.github.io/Introduction_to_Web_Authentication/) — Sessions, cookies, JWTs and CSRF in a web app (Web Development hub)
- [Introduction to Passport.js](https://brendanjameslynskey.github.io/Introduction_to_Passport_js/) — Login strategies for Express (Web Development hub)
- [Cloud *aaS 05: Cloud Security](https://brendanjameslynskey.github.io/Cloud_aaS_05_Cloud_Security/) — IAM across AWS, GCP and Azure, secrets and zero trust
- [Security Engineering: interview preparation](https://github.com/BrendanJamesLynskey/Interview_Security_Engineering) — Questions and answers on application, network and infrastructure security

## Where this fits

Part of the [Software](https://github.com/BrendanJamesLynskey/Software) index, which keeps a short entry for every item listed here. 11 entries; the descriptions are taken from that index, some shortened.
