

\# LMS Technical Benchmark Comparison



\*\*Date:\*\* October 29, 2026  

\*\*Platforms:\*\* Moodle, Forma LMS, Open edX (Tutor), Canvas LMS



| Criteria | Moodle | Forma LMS | Open edX (Tutor) | Canvas LMS |

|---|---|---|---|---|

| Self-hosted | Yes | Yes | Yes | Yes |

| Deployment approach | Docker Compose | Custom Docker Compose | Tutor / Docker | Custom deployment |

| Local deployment tested | Yes | Yes | No | No |

| Admin login tested | Yes | Yes | No | No |

| Course creation tested | Yes | Yes | No | No |

| Student enrollment tested | Yes | Yes | No | No |

| Student login tested | Yes | Yes | No | No |

| Initial RAM (app + DB) | 455.9 MiB | 279.5 MiB | Not measured | Not measured |

| RAM after activity | Not measured comparably | 285.9 MiB | Not measured | Not measured |

| SCORM | Plugin support | SCORM 1.2 / 2004 | Requires additional integration | Requires external integration |

| xAPI / cmi5 | Requires integration | Requires verification | Requires integration | Requires integration |

| REST APIs | Available | Requires verification | Available | Available |

| SSO / authentication | Plugins / OAuth2 | LDAP / AD options | Configurable | OAuth2 / SAML options |

| Backup / restore | Database + Moodle data | Database + application files | Tutor-managed services and volumes | Database + application storage |

| Setup complexity | Moderate | Moderate | High | High |

| Local deployment issues | Image manifest issue | Missing Composer dependencies; PHP warnings | Not tested | Not tested |



