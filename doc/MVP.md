# MVP

This demo showcases the simplicity of creating an MVP application from a Git repository using ArgoCD.

To do this, simply run the following command: 
```
argocd app create demo --app-namespace argocd 
--repo https://github.com/den-vasyliev/go-demo-app.git --path helm --dest-namespace demo 
--dest-server https://kubernetes.default.svc --sync-option CreateNamespace=true --sync-policy auto
```
Take into account the option ```--sync-option CreateNamespace=true```, which allows ArgoCD to create a new 'demo' namespace.

After the completion of the creation process, the application's health status changed from 'Progressing' to 'Healthy.

```
NAME         CLUSTER                         NAMESPACE  PROJECT  STATUS  HEALTH   SYNCPOLICY  CONDITIONS  REPO                                             PATH  TARGET
argocd/demo  https://kubernetes.default.svc  demo       default  Synced  Healthy  Auto        <none>      https://github.com/den-vasyliev/go-demo-app.git  helm
```

Then we are ready to check if the application is performing correctly.

Let's showcase all these steps in the next video: 

![new-argoapp](https://github.com/bergshrund/AsciiArtify/assets/17909431/a946d2a6-f1b1-4b55-8655-2f85a8ee5248)

We can achieve the same using the ArgoCD GUI:

![argo-gui](https://github.com/bergshrund/AsciiArtify/assets/17909431/09570d91-fcc0-43b7-a8bd-a9d8cfb6a2c1)

