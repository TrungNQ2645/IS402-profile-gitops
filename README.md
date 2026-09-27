# IS402 Profile GitOps

Kubernetes desired state for the `IS402-profile` frontend.

- `apps/profile` keeps the OpenStack/Magnum service on load balancer port 80.
- `apps/profile-k3s` reuses the same Deployment and exposes the Service on port
  8088 for the resource constrained ARM64 fallback lab, where Apache already
  owns host port 80.

The deployment image starts as a placeholder. The application repository workflow replaces the single `image:` field with the tested GHCR image digest before pushing this repository's `main` branch.

Do not commit kubeconfig files, passwords, PATs, registry credentials, or plaintext Kubernetes Secrets here.
