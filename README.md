Deployment Order
- terraform/ (this in case use GKE, not used if on premise)
- metallb/ (if on premise)
- local-path-provisioner/ (if on premise)
- ingress-nginx/
- cert-manager/
- mysql/
- laravel/

in ubuntu pvc.yaml, if adjust the storageclassname based on where the kubernetes is deployed, if on premise the storageclassname it must be `local-path`, if is cloud based (like GKE), determine with getting the storageclassname using `kubectl get sc`