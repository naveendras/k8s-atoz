# Workloads

- ReplicaSet
- Deployment
- DaemonSet
- StatefulSet
- Job
- CronJob

### ReplicaSet

- Primary method of managing pod replicas and their lifecycle.
- Handles scheduling, scaling, and deletion of pods.
- Ensures the desired number of pods are always running.

### Deployment

- Way of managing Pods via ReplicaSets.
- Provide rollback functionality and update control.
- Updates are managed through the pod-template-hash label. 
- Each iteration creates a unique label that is assigned to both the ReplicaSet and subsequent Pods.

### DaemonSet

- Ensure that all nodes matching certain criteria will run an instance of the supplied Pod.
- Are ideal for cluster wide services such as log forwarding or monitoring.

### StatefulSet

- Tailored to managing Pods that must persist or maintain state. 
- Assigned a unique ordinal name following the convention of ‘<statefulset name>-<ordinal index>’.
- Useful when:
    - Stable, unique network identifiers are required
    - Stable, persistent storage is needed
    - Ordered, graceful deployment and scaling is important
