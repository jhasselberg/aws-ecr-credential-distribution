# AWS ECR Credential Distribution

ECR credentials are only valid for 12 hours after creation, so they must be renewed regularly and distributed across all namespaces. This can be done by a cronjob in the cluster which combines different approaches. The following methods combine the work from [aws-kubectl](https://github.com/Odania-IT/aws-kubectl) (so that ARM ready, because i handle a K3S-Cluster) and [registry-creds](https://github.com/alexellis/registry-creds), for distribution instead of using the Bash one... This workflow ensures that valid ECR credentials are always available.

