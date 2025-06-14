Here's a complete and categorized list of commonly used `kubectl get` commands to **view Kubernetes resources**. These are especially useful for DevOps roles:

---

### 🔹 **Basic Syntax**

```bash
kubectl get <resource-type>                # Get all resources of a specific type
kubectl get <resource-type> <resource-name>   # Get a specific resource
kubectl get <resource-type> -n <namespace>   # Get from a specific namespace
kubectl get all                            # Get all workload resources (pods, svc, deploy, etc.)
```

---

### 🔹 **Most Common `get` Commands**

#### 1. **Pods**

```bash
kubectl get pods
kubectl get po                            # Short form
kubectl get pods -o wide                  # Show node, IP, etc.
```

#### 2. **Deployments**

```bash
kubectl get deployments
kubectl get deploy                        # Short form
```

#### 3. **Services**

```bash
kubectl get services
kubectl get svc                           # Short form
```

#### 4. **ReplicaSets**

```bash
kubectl get rs
```

#### 5. **Namespaces**

```bash
kubectl get ns
```

#### 6. **Nodes**

```bash
kubectl get nodes
kubectl get no                            # Short form
```

#### 7. **ConfigMaps & Secrets**

```bash
kubectl get configmaps
kubectl get secrets
```

#### 8. **Persistent Volumes (PV) & Claims (PVC)**

```bash
kubectl get pv
kubectl get pvc
```

#### 9. **StatefulSets & DaemonSets**

```bash
kubectl get statefulsets
kubectl get daemonsets
```

#### 10. **Ingress**

```bash
kubectl get ingress
kubectl get ing
```

---

### 🔹 **Additional Resource Types**

```bash
kubectl get jobs
kubectl get cronjobs
kubectl get events
kubectl get endpoints
kubectl get serviceaccounts
kubectl get roles
kubectl get rolebindings
kubectl get clusterroles
kubectl get clusterrolebindings
kubectl get networkpolicies
```

---

### 🔹 **Useful Flags**

| Flag                       | Description                 |
| -------------------------- | --------------------------- |
| `-A` or `--all-namespaces` | Show across all namespaces  |
| `-n <namespace>`           | Show within a namespace     |
| `-o wide`                  | More info (e.g. node names) |
| `-o yaml`                  | Output in YAML              |
| `-o json`                  | Output in JSON              |
| `--show-labels`            | Show labels                 |
| `--selector=<label>`       | Filter using labels         |
| `-w`                       | Watch updates live          |

Example:

```bash
kubectl get pods -n kube-system -o wide --show-labels
kubectl get pods --selector=app=nginx
```

---

### 🔹 **List All Resource Types**

To get a full list of all supported resources:

```bash
kubectl api-resources
```

---

If you want, I can also give you a **printable cheat sheet** of `kubectl` commands. Let me know!
