### What's changed in v0.1.0

* feat: helm chart xrd (by @patrickleet)

* fix: standardize GitHub workflows (by @patrickleet)

* fix: add ClusterRoleBinding to e2e test for RBAC permissions (by @patrickleet)

  The Helm provider with InjectedIdentity needs cluster-admin permissions
  to create namespaces and install charts. Without the ClusterRoleBinding,
  the e2e test times out waiting for the helm release to become Ready.

  Also updated to use autoUpgrade.channel = "Rapid" instead of pinning
  a specific Crossplane version, matching the standard Helm XRD pattern.

  Co-Authored-By: Claude Opus 4.5 <noreply@anthropic.com>


