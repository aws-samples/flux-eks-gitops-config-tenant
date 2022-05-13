# Managing tenant configuration with GitOps using Flux 

This is a tenant GitOps configuration sample repository for Flux, related to the project [flux-eks-gitops-config](https://github.com/aws-samples/flux-eks-gitops-config).

Tenants are on-boarded on Kubernetes clusters by platform administrators, who are in charge of creating a Namespace, setting appropriate quotas, creating a Service Account and RBAC with permissions restricted to the Namespace for Flux to sync configuration and a GitRepository CR pointing to the tenant repository (this one).

The tenant repository is owned by a development team and stores the Kubernetes manifests, [Kustomizations](https://fluxcd.io/docs/components/kustomize/api/) and [HelmReleases](https://fluxcd.io/docs/components/helm/helmreleases/) Custom Resources to deploy the application(s) on the Kubernetes clusters. For each tenant, there's a Kustomization on the platform team repository pointing to a tenant repository, branch and path. 

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.

