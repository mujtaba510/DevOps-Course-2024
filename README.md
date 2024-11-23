# DevOps-Course-FALL-2024

This repository contains a detailed walkthrough of the concepts and technologies I learned during the **DevOps Course FALL-2024**, taught by **@Saim Safdar**.

## Technologies and Tools

- **Version Control**: GitHub
- **Containerization**: 
  - Docker
  - Podman
- **Orchestration**: 
  - Kubernetes
  - Istio
- **Cloud Services**: 
  - ECS/EKS
- **Infrastructure as Code (IaC)**: 
  - Terraform
  - Pulumi
- **Policy as Code**: Kyverno
- **Serverless Frameworks**: Knative
- **Networking**: Ingress

## Blog 1

### Integrating Docker Compose CI/CD Pipelines for Automated Deployments

1. **Docker Compose Overview**:
   - Docker Compose is an orchestration tool for managing multi-container Docker applications. It uses a YAML file to define services, networks, and volumes, making it ideal for single-host setups.

2. **Importance in CI/CD**:
   - Docker Compose ensures consistent environments across development, testing, and production, reducing issues like "it works on my machine" by running the app in the same environment throughout the pipeline.

3. **Setting Up a CI/CD Pipeline**:
   - **Step 1**: Test Docker Compose locally with a `docker-compose.yml` file, which defines services like web and Redis.
   - **Step 2**: Integrate Docker Compose with CI tools like GitHub Actions for automated builds and tests, including Docker image build, service startup, and running tests (e.g., using pytest).
   - **Step 3**: Automate deployment by adding a deployment job to push Docker images to a registry and use `docker-compose up -d` to deploy to production.

4. **Monitoring and Rollbacks**:
   - After deployment, monitor the application using tools like Prometheus or Grafana. For rollbacks, the pipeline can deploy the previous Docker image in case of failure.

5. **Conclusion**:
   - Automating deployments with Docker Compose in CI/CD pipelines enhances reliability, reduces human errors, and saves time, allowing developers to focus more on coding.

## Blog 2

### Kubernetes K9s: The Ultimate Tool for Managing Kubernetes Clusters

1. **Introduction to K9s**:
   - K9s is an open-source, terminal-based UI tool designed to simplify Kubernetes cluster management. It provides real-time monitoring and an interactive, visual experience for managing Kubernetes resources directly in the terminal.

2. **Key Features**:
   - **Interactive Terminal UI**: Manage Kubernetes resources without leaving the terminal.
   - **Real-time Monitoring**: Get live updates on the status of your pods and deployments.
   - **Shell Access to Pods**: Access pods directly for troubleshooting.
   - **Resource Management**: Filter, sort, and manage pods, services, and deployments.
   - **Log Viewing**: View detailed logs for pods and containers.

3. **Installation**:
   - Install K9s by running `curl -sS https://webinstall.dev/k9s | bash`, verify installation with `k9s version`, and launch with `k9s`.

4. **Basic Commands**:
   - View pods: `:pods`
   - Switch namespace: `:ns <namespace_name>`
   - View logs for a pod: `l <pod_name>`

5. **Advanced Features**:
   - **Filtering and Sorting**: Filter resources by namespace, label, or type.
   - **Interactive Logs and Shell Access**: View logs and run commands inside pods directly.
   - **Custom Plugins**: Extend functionality with custom plugins by modifying the `~/.k9s/plugins.yml` file.

6. **Conclusion**:
   - K9s simplifies Kubernetes cluster management, offering a more efficient and intuitive interface compared to traditional CLI tools. It's essential for developers looking to streamline cluster management and troubleshooting tasks.

## Blog 3

### Automating Testing and Deployment with GitHub Actions

1. **What is GitHub Actions?**
   - GitHub Actions is a DevOps tool integrated into GitHub repositories, enabling automated workflows such as CI, CD, and testing using YAML files. Workflows can be triggered by events like push, pull requests, or issues.

2. **Why Use GitHub Actions?**
   - **Integrated with GitHub**: No need for external CI/CD tools.
   - **Free for Public Repositories**: GitHub offers free runners for public projects.
   - **Extensible**: Easily integrate testing frameworks or deployment services.
   - **Parallel Execution**: Run multiple workflows simultaneously for faster CI/CD.

3. **Setting Up GitHub Actions:**
   - **Create a GitHub Repository**: Ensure your project is hosted on GitHub.
   - **Create a Workflow File**: Define workflows in the `.github/workflows` directory using YAML.
   - **Define Workflow**: Example for automating testing and deployment (for a Node.js app).
     - **Test Job**: Install dependencies and run tests.
     - **Deploy Job**: Deploy only if tests pass.

4. **Setting Up Deployment:**
   - Deploy to cloud platforms like AWS, Azure, or Google Cloud, or use FTP/SFTP.
   - Example: Deploying to AWS Lambda using GitHub Actions.

5. **Add Secrets for Security**:
   - Use GitHub Secrets to securely store sensitive information like API keys.

6. **Running and Monitoring the Workflow:**
   - GitHub Actions will trigger workflows on push or pull requests.
   - Check the status and logs in the Actions tab of your repository.

7. **Best Practices:**
   - Cache dependencies for faster builds, test across multiple environments, limit access to secrets, and use matrix builds for various configurations.
   - Implement fast tests and deploy only when tests pass.

8. **Conclusion**:
   - GitHub Actions helps automate testing and deployment, improving efficiency, reducing human error, and enhancing productivity in development workflows. It is highly configurable for various project sizes and requirements.

## Contacts

### Platforms

- **Medium**:  
  Explore my articles and insights:  
  [Visit Medium Profile](https://medium.com/@gmujtaba1218)

- **GitHub**:  
  Discover my projects, contributions, and open-source work:  
  [Visit GitHub Profile](https://github.com/mujtaba510)

- **LinkedIn**:  
  Get a glimpse of my accomplishments:  
  [Visit LinkedIn Profile](https://www.linkedin.com/in/ghulam-mujtaba-16544230a)

## Resume

To view my detailed resume, click here:  
[View Resume](https://drive.google.com/file/d/1V3V76w6Q3MjGN-GhUVdgawAH3lRRbqBY/view?usp=drive_link)
