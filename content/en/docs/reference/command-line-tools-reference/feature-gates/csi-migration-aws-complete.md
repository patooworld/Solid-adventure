---
# Removed from Kubernetes
title: CSIMigrationAWSComplete
content_type: feature_gate

_build:
  list: never
  render: false
---
Stops registering the EBS in-tree plugin in
kubelet and volume controllers and enables shims and translation logic to
route volume operations from the AWS-EBS in-tree plugin to EBS CSI plugin.
Requires CSIMigration and CSIMigrationAWS feature flags enabled and EBS CSI
plugin installed and configured on all nodes in the cluster. This flag has
been deprecated in favor of the `InTreePluginAWSUnregister` feature flag
which prevents the registration of in-tree EBS plugin.
