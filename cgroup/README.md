As cgroup v2 is GA in 1.25+, and is also the default on Ubuntu 22.04, customers may have to downgrade to cgroups v1 due to compatibility issues with older software.

To perform a cgroups version downgrade on your nodes, use this Daemonset.

Important note
The Daemonset by default will apply to all nodes in your cluster and will reboot them to apply the cgroup change. Please set a nodeSelector to control how this gets applied.

AKS did not support change cgroup version via modifying node directly.
https://learn.microsoft.com/en-us/azure/aks/resize-node-pool?tabs=azure-cli
