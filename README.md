# IS402 Profile GitOps

Kubernetes desired state for the `IS402-profile` frontend.

The deployment image starts as a placeholder. The application repository workflow replaces the single `image:` field with the tested GHCR image digest before pushing this repository's `main` branch.

Do not commit kubeconfig files, passwords, PATs, registry credentials, or plaintext Kubernetes Secrets here.
