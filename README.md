# articles
Demo golang api

## Running container
```bash
podman pull public.ecr.aws/flynshue/articles:v0.1.1
```
```bash
podman run -d -p 8080:5000 public.ecr.aws/flynshue/articles:v0.1.1
```

## Deploying to OCP using raw manifests
This uses ocp routes, which is why it's ocp specific.
```bash
oc apply -f deployment.yaml
```

## Deploying to k8s or ocp using helm chart
```bash
helm install -n <namespace> <helm release> charts/articles
```
Here's an example of deploying helm release articles to namespace test-flynshue
```bash
helm install -n test-flynshue articles charts/articles
```

