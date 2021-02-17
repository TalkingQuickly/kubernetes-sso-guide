This is the supporting code for the tutorial series [A Comprehensive Guide to SSO on Kubernetes](http://localhost:4000/kubernetes-sso-a-comprehensive-guide).

Some of the highlights this series explains how to do are:

1. Login to the `kubectl` cli using SSO credentials via the browser
1. Replace basic auth ingress annotations with equally simple but much more secure SSO annotations
1. Push and pull to a secure private docker registry with full ACL

## Structure

- `charts/`: Charts which are currently only available as part of the deprecated `stable` helm repository. Any charts in this directory remain subject to the [licenses in the original repos, Apache 2.0 at time of writing](https://github.com/helm/charts/blob/master/LICENSE). As these charts become available elsewhere, they'll be removed when the tutorial series is updated.
- `docker-registry/`: The example helm values file for configuring the basic docker registry chart
- `gitea/`: The example helm values file for configuring gitea
- `group-auth/`: An example cluster role binding definition for configuring a specific SSO group to automatically have cluster admin access
- `harbor/`: The example helm values file for configuring harbor 
- `jwt-ruby-example/`: An example ruby application showing how to decode JSON Web Tokens
- `keycloak/`: The example helm values file for configuring Keycloak
- `kube-oidc-proxy/`: The example helm values for for configuring Kube OIDC Proxy
- `kubelogin/`: An example KUBECONFIG file for use with kubelogin and kube oidc proxy
- `nginx-demo-app/`: An example helm values file for deploying Nginx with ingress annotations which delegate authentication to Keycloak via OIDC and demonstrate passing the JWT through
- `oauth2-proxy/`: An example helm values file for `oauth2-proxy` which provides the underlying endpoints needed for nginx to delegate auth to Keycloak
- `openldap/`: An example helm values file for installing and configuring openldap
