1.Node Affinity ensures that pods are hosted on particular nodes.
2.Node affinity allows us to direct the scheduler based on the attributes on the nodes. For instance we can direct the scheduler
to only place certain pods on nodes with a specific label or nodes in a certain availability zone. 
[This can be coupled with taints and tolerations to ensure pods only run on the nodes we dictate.] This works well when we have different types of nodes
that are designed to host certain pods, for instance if we have nodes with larger instance types to host larger applications or nodes with attached volumes.

1.Pod Affinity ensures two pods to be co-located in a single node.
2.The pod affinity rule says that the pod can be scheduled to a nodeonly if that node is in the same zone as at least one already-running pod
that has a label with key “security” and value “S1”
3.the pod affinity rule indicates that the pod can schedule onto a node only if that node has at least one already-running pod with a label that has 
the key security and value S1. The pod anti-affinity rule says that the pod prefers to not schedule onto a node if that node is already running a pod 
with label having key security and value S2.
4.Use the podAffinity stanza to configure the requiredDuringSchedulingIgnoredDuringExecution parameter or preferredDuringSchedulingIgnoredDuringExecution parameter
