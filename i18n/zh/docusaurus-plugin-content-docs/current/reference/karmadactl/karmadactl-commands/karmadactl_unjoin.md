---
title: karmadactl unjoin
---

Remove a cluster from Karmada control plane

### Synopsis

Remove a cluster from Karmada control plane.

```
karmadactl unjoin CLUSTER_NAME --cluster-kubeconfig=<KUBECONFIG>
```

### Examples

```
  # Unjoin cluster from karmada control plane, but not to remove resources created by karmada in the unjoining cluster
  karmadactl unjoin CLUSTER_NAME
  
  # Unjoin cluster from karmada control plane and attempt to remove resources created by karmada in the unjoining cluster
  karmadactl unjoin CLUSTER_NAME --cluster-kubeconfig=<KUBECONFIG>
  
  # Unjoin cluster from karmada control plane with timeout
  karmadactl unjoin CLUSTER_NAME --cluster-kubeconfig=<KUBECONFIG> --wait 2m
```

### Options

```
      --cluster-context string      Context name of cluster in kubeconfig. Only works when there are multiple contexts in the kubeconfig.
      --cluster-kubeconfig string   Path of the cluster's kubeconfig.
      --cluster-namespace string    Namespace in the control plane where member cluster secrets are stored. (default "karmada-cluster")
      --dry-run                     Run the command in dry-run mode, without making any server requests.
      --force                       Delete cluster and secret resources even if resources in the cluster targeted for unjoin are not removed successfully.
  -h, --help                        help for unjoin
      --karmada-context string      The name of the kubeconfig context to use
      --wait duration               wait for the unjoin command execution process(default 60s), if there is no success after this time, timeout will be returned. (default 1m0s)
```

### Options inherited from parent commands

```
      --add-dir-header                   If true, adds the file directory to the header of the log messages
      --alsologtostderr                  log to standard error as well as files (no effect when -logtostderr=true)
      --kubeconfig string                Paths to a kubeconfig. Only required if out-of-cluster.
      --log-backtrace-at traceLocation   when logging hits line file:N, emit a stack trace (default :0)
      --log-dir string                   If non-empty, write log files in this directory (no effect when -logtostderr=true)
      --log-file string                  If non-empty, use this log file (no effect when -logtostderr=true)
      --log-file-max-size uint           Defines the maximum size a log file can grow to (no effect when -logtostderr=true). Unit is megabytes. If the value is 0, the maximum file size is unlimited. (default 1800)
      --logtostderr                      log to standard error instead of files (default true)
      --one-output                       If true, only write logs to their native severity level (vs also writing to each lower severity level; no effect when -logtostderr=true)
      --skip-headers                     If true, avoid header prefixes in the log messages
      --skip-log-headers                 If true, avoid headers when opening log files (no effect when -logtostderr=true)
      --stderrthreshold severity         logs at or above this threshold go to stderr when writing to files and stderr (no effect when -logtostderr=true or -alsologtostderr=false) (default 2)
  -v, --v Level                          number for the log level verbosity
      --vmodule moduleSpec               comma-separated list of pattern=N settings for file-filtered logging
```

### SEE ALSO

* [karmadactl](karmadactl.md)	 - karmadactl controls a Kubernetes Cluster Federation.

#### Go Back to [Karmadactl Commands](karmadactl_index.md) Homepage.


###### Auto generated by [spf13/cobra script in Karmada](https://github.com/karmada-io/karmada/tree/master/hack/tools/genkarmadactldocs).