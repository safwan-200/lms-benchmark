\# LMS Benchmarking – Final Recommendation



\*\*Prepared by:\*\* Safwan Hussain  

\*\*Date:\*\* October 29, 2026  

\*\*Project:\*\* Self-Hosted LMS Evaluation



\## 1. Objective



The goal of this project was to evaluate self-hosted Learning Management Systems (LMS) for deployment, resource efficiency, ease of administration, and suitability for internal training. Moodle, Forma LMS, Open edX, and Canvas were included in the comparison, with hands-on Docker deployments completed for Moodle and Forma LMS.



\## 2. Deployment and Testing Results



Both Moodle and Forma LMS were successfully deployed locally using Docker Compose on a Windows machine with 16 GB RAM and approximately 7.6 GiB allocated to Docker.



The following functionality was verified on both platforms:



\- Administrator login and course creation

\- Student account creation and enrollment

\- Student login and access to the assigned course



A sample course, \*\*Introduction to DevOps (DEVOPS101)\*\*, was created on both systems.



\### Resource Usage



| Metric | Moodle | Forma LMS |

|---|---:|---:|

| Application RAM | 265.1 MiB | 92.2 MiB |

| Database RAM | 190.8 MiB | 193.4 MiB |

| Combined RAM | 455.9 MiB | 285.6 MiB |

| Basic functionality | Passed | Passed |



These measurements represent idle snapshots rather than controlled load testing. Forma LMS used approximately 37% less RAM in the recorded samples.



\## 3. Deployment Challenges



\*\*Moodle:\*\* The original Docker image reference produced a manifest error. Deployment succeeded after switching to an alternative Moodle image.



\*\*Forma LMS:\*\* Additional manual setup was required, including Composer dependency installation and web-based configuration. PHP deprecation warnings and autoloading warnings were observed during setup and testing, although the tested functionality worked.



\## 4. Recommendation



\*\*Moodle is the recommended starting point for the internal training LMS.\*\*



Both platforms passed the basic functional tests, and Forma LMS demonstrated lower idle memory usage. However, Moodle offered a more straightforward setup in this test and did not exhibit the same visible PHP compatibility warnings encountered with Forma LMS.



Forma LMS remains a viable alternative where low idle resource consumption is a priority, provided its compatibility warnings are investigated and resolved.



\## 5. Next Steps



Before making a production deployment decision, the team should:



\- Run controlled concurrent-user and activity-based performance tests.

\- Verify SCORM/xAPI requirements and API integrations.

\- Test backup, restore, authentication, and role permissions.

\- Confirm deployment security, maintenance, and upgrade requirements.



\*\*Conclusion:\*\* Moodle is the provisional recommendation based on the completed local testing. Production suitability requires further validation.

