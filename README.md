\# LMS Benchmark — Deployment and Comparison



\*\*Prepared by:\*\* Safwan Hussain  

\*\*Date:\*\* October 29, 2026



\## Overview



This project compares four open-source Learning Management Systems: Moodle, Forma LMS, Open edX, and Canvas LMS.



\## Hands-On Testing



Moodle and Forma LMS were deployed locally using Docker Compose.



Both deployments were tested for:



\- Administrator access

\- Course creation

\- Student account creation

\- Student enrollment and course access

\- Basic CPU and RAM utilization



\### Resource Measurements



| Platform | Application RAM | Database RAM | Total RAM |

|---|---:|---:|---:|

| Moodle | \~265–306 MiB | \~191 MiB | \~456–497 MiB |

| Forma LMS | \~86–92 MiB | \~193 MiB | \~279–286 MiB |



These figures are snapshots from local testing, not controlled load benchmarks.



\## Deployment



The `moodle` and `forma` folders contain Docker Compose configurations.



Before deployment, configure the following environment variables:



\- `DB\_ROOT\_PASSWORD`

\- `DB\_PASSWORD`

\- `MOODLE\_ADMIN\_PASSWORD` (Moodle only)



Forma LMS also requires application installation and configuration through its web installer.



\## Known Issues



Moodle initially encountered a Docker image manifest issue, which was resolved using an alternative image.



Forma LMS displayed PHP deprecation warnings during testing, although installation and basic course functionality worked.



\## Remaining Work



\- Controlled load testing

\- Additional benchmarking and validation

\- Review and refinement of the final recommendation



\## Included Documents



\- `LMS\_Comparison.md` — technical comparison matrix

\- `LMS\_Recommendation.md` — recommendation and rationale

\- `moodle/compose.yaml` — Moodle configuration

\- `forma/compose.yaml` — Forma LMS configuration

