# Managing tenant configuration with GitOps using Flux 

This is a tenant GitOps configuration sample repository for Flux, related to the project [flux-eks-gitops-config](https://github.com/aws-samples/flux-eks-gitops-config).

Tenants are on-boarded on Kubernetes clusters by platform administrators, who are in charge of creating a *Namespace* for the tenant, setting appropriate quotas, creating a *ServiceAccount* and RBAC with permissions restricted to the Namespace and a [GitRepository](https://fluxcd.io/docs/components/source/gitrepositories/) *Custom Resource* pointing to the tenant repository (this one). Flux impersonates the aforementioned *ServiceAccount* to reconcile resources from the tenant repository, so the platform administrator can limit permissions of the tenant to create resources in the cluster. See the [tenant folder](https://github.com/aws-samples/flux-eks-gitops-config/tree/main/tenants/base/podinfo-team) on the flux-eks-gitops-config repository for more details.

This repository is owned by a development team and stores the Kubernetes manifests, [Kustomizations](https://fluxcd.io/docs/components/kustomize/api/) and [HelmReleases](https://fluxcd.io/docs/components/helm/helmreleases/) *Custom Resources* to deploy the application(s) on the Kubernetes clusters. For each tenant, there's a Kustomization on the platform team repository pointing to a tenant repository, branch and path. 

For more information, check the [flux-eks-gitops-config documentation](https://github.com/aws-samples/flux-eks-gitops-config).

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.

