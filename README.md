# Mini Project - Multi-Container Application with Kubernetes Persistent Storage (Local Setup)

## Project Overview
This project deploys a multi-container application (Node.js API and MongoDB) to a Minikube cluster on WSL Ubuntu, using PersistentVolume for data persistence. It manages Kubernetes nodes and automates deployment with GitHub Actions. Builds on previous Minikube projects (Jul 08, 2025).

## Setup
- Initiated on Jul 09, 2025, 11:12 AM CAT.
- Used WSL Ubuntu, VS Code, and Git Bash in `C:\Users\Abraham\Documents\Workspace\Minikube_Setup`.
- System: 2 CPUs, 2GB free memory, 20GB free disk space.

## Execution Steps
1. **Set Up Node.js API**:
   - Created Node.js API with MongoDB integration.
   - Built and loaded `ecommerce-api` image into Minikube.
   - [Screenshot: `ecommerce_api_image_load_output_local.png` - Shows image build and load.]
2. **Set Up MongoDB**:
   - Configured PersistentVolume and PersistentVolumeClaim for MongoDB.
   - Deployed MongoDB with a service.
3. **Deploy Application**:
   - Applied Kubernetes resources for MongoDB and API.
   - Verified pods and services.
   - [Screenshot: `multi_container_app_output_local.png` - Shows API output.]
4. **Node Management**:
   - Inspected nodes with `kubectl get nodes` and `kubectl describe node minikube`.
   - Stopped and restarted Minikube.
   - [Screenshot: `kubectl_node_output_local.png` - Shows node details.]
   - [Screenshot: `minikube_stop_start_output_local.png` - Shows stop and start output.]
5. **Side Hustle Task**:
   - Automated deployment with GitHub Actions.
   - Pushed to `https://github.com/westgrin/minikube-setup`.
   - [Screenshot: `github_actions_multi_container_run_local.png` - Shows workflow run.]

## Learning Summary
This project advanced my Kubernetes skills by deploying a multi-container application with persistent storage. It reinforced node management and automation, aligning with my DevOps goals (June 16, 2025) for production-like deployments.

## Tools Used
- **WSL Ubuntu Terminal**: For Minikube, Docker, and kubectl commands.
- **VS Code**: For editing code and `README.md`.
- **Git Bash**: For GitHub operations.
- **GitHub Actions**: For deployment automation.
- **Minikube**: For local Kubernetes cluster.
- **Docker**: For containerization.

## Project Deliverables
- **Documentation**: This `README.md` with steps and learning summary.
- **Screenshots**:
  - `ecommerce_api_image_load_output_local.png`
  - `multi_container_app_output_local.png`
  - `kubectl_node_output_local.png`
  - `minikube_stop_start_output_local.png`
  - `github_actions_multi_container_run_local.png`
- **Script Link**: [GitHub Repository](https://github.com/westgrin/minikube-setup)

## Local Development Instructions
1. Clone repository: `git clone https://github.com/westgrin/minikube-setup.git`
2. Start Minikube: `minikube start --driver=docker`
3. Load image: `minikube image load ecommerce-api`
4. Deploy app: `kubectl apply -f multi-container-app/*.yaml`
5. Access app: `minikube service ecommerce-api-service --url`
6. Previous project README: [README_nodes.md](README_nodes.md)

## Troubleshooting
- Ensured `ecommerce-api` image was loaded with `minikube image load ecommerce-api`.
- Verified MongoDB connectivity with service name `mongodb-service`.
- Set DNS to `8.8.8.8` for network issues.
- Restarted Minikube with `minikube stop` and `minikube start` if needed.

## Conclusion
This project successfully deployed a multi-container application with persistent storage, managed Kubernetes nodes, and automated deployment, enhancing my skills for advanced Kubernetes scenarios.