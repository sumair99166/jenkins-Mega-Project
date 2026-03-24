💭 **DevSecOps Thought**

“In DevSecOps, the real issue is often hidden beyond the pipeline — true debugging starts at the system level.”

While working on my **DevSecOps project**, I faced a Jenkins pipeline issue where it was stuck on:
➡️ *"Waiting for next available executor"*

After investigation, I found the root cause was 🚨 **Low Disk Space**, which forced the Jenkins node offline.

🔧 **Commands I used to debug & fix:**

* `df -h` (check disk space)
* `du -ah / | sort -rh | head -20` (find large files)
* `docker system prune -a -f` (clean Docker)
* `rm -rf ~/.cache/trivy` (remove Trivy cache)
* `sudo systemctl restart jenkins` (restart service)

🛠️ **Tools used in this DevSecOps project:**

* **SonarQube** – Code quality & security analysis
* **OWASP Dependency-Check** – Dependency vulnerability scanning
* **Trivy** – Container/image security scanning
* **Docker** – Containerization & deployment

⚠️ Due to infrastructure limitations and cost constraints, the final stage (Docker Compose build) could not be completed. However, it was a minor step compared to the overall pipeline.

✅ Successfully executed and validated major stages including **SonarQube analysis, OWASP scanning, and Trivy security checks**, gaining strong hands-on experience in real-world DevSecOps workflows.

🙏 Special thanks to **@Shubham** for guidance and support throughout the project.

#DevSecOps #DevOps #Jenkins #CI_CD #Docker #Trivy #SonarQube #OWASP #Debugging #Learning
