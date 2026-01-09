

## **Step 1: Install ArgoCD**

```bash
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

---

## **Step 2: Deploy Backstage**

```bash
kubectl apply -f https://raw.githubusercontent.com/appfactorylabs/backstage-deploy/main/backstage-install.yaml
```

---

## **Step 3: Verify**

```bash
kubectl get all -n argocd
kubectl get all -n backstage
```

* No variable substitution — it uses whatever is in the YAML.
* Backstage will deploy with the values defined in the YAML file.
