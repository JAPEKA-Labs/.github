# JAPEKA

## Nami

| Type  | Name       | Content        | Proxy Status |
| ----- | ---------- | -------------- | ------------ |
| A     | namifi.app | 213.136.84.118 | Proxied      |
| CNAME | www        | namifi.app     | Proxied      |
| CNAME | app        | namifi.app     | Proxied      |
| CNAME | app_stage  | namifi.app     | Proxied      |
| CNAME | app_test   | namifi.app     | Proxied      |

- [Nami landing page](https://nami.wdsui.com/)

### **Environments**

- **[Namifi Application - Testing Environment](https://app_test.wdsui.com/):**  
  This environment is linked to the `testing` branch. Developers merge their changes into this branch, triggering an automated Jenkins job that builds, tests, and deploys the application to the testing environment. This stage is used to validate new features and fixes.

- **[Namifi Application - Staging Environment](https://app_stage.wdsui.com/):**  
  After successful testing, changes are merged into the `stage` branch. Jenkins automatically pulls updates, runs tests, builds the application, and deploys it to the staging environment. This stage serves as a pre-production environment for final validation.

- **[Namifi Application - Production Environment](https://app.wdsui.com/):**  
  Once changes are validated in staging, they are merged into the `main` branch. Jenkins pulls updates, builds, tests the application, and deploys it to the production environment. This environment hosts the live version of the application used by end-users.

### **Workflow**

1. **Development:**  
   Developers create and merge changes into the `testing` branch.
2. **Testing:**  
   Jenkins triggers a job upon detecting updates in the `testing` branch:
   - Pulls the latest changes.
   - Runs automated tests.
   - Builds and deploys the application to the testing environment.
3. **Staging:**  
   Once testing is complete, changes are merged into the `stage` branch. Jenkins:
   - Pulls updates from the `stage` branch.
   - Runs automated tests.
   - Builds and deploys the application to the staging environment.
4. **Production:**  
   After staging validation, changes are merged into the `main` branch. Jenkins:
   - Pulls the latest updates.
   - Runs automated tests.
   - Builds the application.
   - Deploys it to the production environment, making it available to end-users.

## JAPEKA

| Type  | Name       | Content        | Proxy Status |
| ----- | ---------- | -------------- | ------------ |
| A     | japeka.dev | 213.136.84.118 | Proxied      |
| CNAME | www        | japeka.dev     | Proxied      |

- [JAPEKA landing page](https://japeka.wdsui.com/)

## Tools

| Type  | Name       | Content    | Proxy Status |
| ----- | ---------- | ---------- | ------------ |
| CNAME | jenkins    | japeka.dev | Proxied      |
| CNAME | portainer  | japeka.dev | Proxied      |
| CNAME | grafana    | japeka.dev | Proxied      |
| CNAME | traefik    | japeka.dev | Proxied      |

### **Monitoring and Observability**

- **[Grafana](https://grafana.wdsui.com/):** Visualizes data with dashboards, helping monitor system performance and analyze metrics.
- **[Traefik](https://traefik.wdsui.com/):** Analyzes HTTP and HTTPS routing, reverse proxying, load balancing for services.

### **Continuous Integration and Deployment (CI/CD)**

- **[Jenkins](https://jenkins.wdsui.com/):** Automates build, test, and deployment pipelines, ensuring reliable and efficient software delivery.

### **Infrastructure Management**

- **[Portainer](https://portainer.wdsui.com/):** Simplifies managing and monitoring Docker containers and environments with an easy-to-use interface.


### **Certificate Management**

- **Let’s Encrypt (via Traefik):** Provides free SSL/TLS certificates for secure communication. Traefik automates the renewal and deployment of these certificates across services.

### **Diagrams**

- **[Pipelines](https://www.canva.com/design/DAGY6IJYK8s/nhincDTcJW88-1kWshHJvQ/edit?utm_content=DAGY6IJYK8s&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)**

- **[Infrastructure](https://www.canva.com/design/DAGYVGrdGWU/9pD1LdOSnNCuBnW64zptig/edit?utm_content=DAGYVGrdGWU&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)**

- **[Load Balancer](https://www.canva.com/design/DAGaCzoek0I/AmtssFzy26DtFLw4gyPhYQ/edit?utm_content=DAGaCzoek0I&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)**

- **[Notifications System](https://www.canva.com/design/DAGaC9iAfuo/TzJoR2fiD6Qsht2vq22cQw/edit?utm_content=DAGaC9iAfuo&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)**
