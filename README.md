# Sync your resources with Flux !

Tools used : 

- FLuxV2 : tool to sync your k8s infrastructure with a GitOps approach.
- SealedSecrets : this app is easy to use and install, maintained by bitnami, it lets you encrypt your secrets (so you can host them wherever you want). 
- Kubed: This app help you to sync your secrets/configMaps on labelled namespaces.


FluxV2 documentation : 
https://toolkit.fluxcd.io/get-started/

Article on medium : 


Tree of this repo : 
```
├── apps
│   ├── base
│   │   ├── kubed
│   │   │   ├── kustomization.yaml
│   │   │   └── release.yaml
│   │   └── sealed-secrets
│   │       ├── kustomization.yaml
│   │       └── release.yaml
│   └── staging
│       └── kustomization.yaml
├── clusters
│   └── my-cluster
│       ├── apps.yaml
│       ├── flux-system
│       │   ├── gotk-components.yaml
│       │   ├── gotk-sync.yaml
│       │   └── kustomization.yaml
│       ├── namespaces.yaml
│       ├── resources.yaml
│       └── sources.yaml
├── namespaces
│   ├── kustomization.yaml
│   └── namespaces.yaml
├── resources
│   └── staging
│       ├── configmaps
│       │   ├── apps-cm.yaml
│       │   ├── cm.yaml
│       │   └── kustomization.yaml
│       ├── kustomization.yaml
│       └── secrets
│           ├── kustomization.yaml
│           ├── regcred-sealed.yaml
│           └── secret2-sealed.yaml
└── sources
    ├── appscode.yaml
    ├── kustomization.yaml
    └── sealed-secrets.yaml
```
