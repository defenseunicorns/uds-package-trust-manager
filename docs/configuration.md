# Configuration

Trust Manager in this package is configured through the upstream [Trust Manager chart](https://charts.jetstack.io/trust-manager) as well as a UDS configuration chart that supports the following:

## Istio

Currently to avoid x509 errors for the trust-manager webhook when deploying with Istio, a `PeerAuthentication` resource is created by default that configures the webhook endpoint to use permissive mTLS. This is controlled by the `istio.enabled` value in the UDS configuration chart.

## Trust Bundles

This package only deploys the Trust Manager service, not custom CA bundles. In a UDS bundle that installs Trust Manager, after Trust Manager is deployed, custom CA bundles can be created and distributed by deploying packages that configure `Bundle` resources. Example usage in [trust-manager docs](https://cert-manager.io/docs/trust/trust-manager/#usage) as well as the [zarf package](../tests/trustbundle/trust-bundle.yaml) used to test trust-manager in this repo that shows a custom CA bundle that is distributed to every namespace managed by zarf. 