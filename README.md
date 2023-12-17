Create an Argo in another cluster with argocd auto pltoi recover mode 
Note:
We need to connect( Kube config) to the cluster that would like to install Argocd
Step below no need to install ArgoCD core, argocd-autopilot  command will help get all config and installation from Git repository

Install Argo Pilot
```bash
brew install argocd-autopilot
```
Get Github token
First, we need to create a personal access token in GitHub. Go to your GitHub account settings, and then click on the "Developer settings" option. From there, select "Personal access tokens" and click on the "Generate new token" button. Give your token a name and select the scopes that you need for your deployments.

 
Export to ken and repo
```bash
GIT_REPO=https://github.com/patiyan-sukkasem/argo-sk.git
GIT_TOKEN=ghp_xxxxxxxxxxxx
```

Run argocd auto pltoi recovernode
```bash
argocd-autopilot repo bootstrap --recover
```


