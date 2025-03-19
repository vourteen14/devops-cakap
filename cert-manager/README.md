helm repo add jetstack https://charts.jetstack.io

helm repo update

helm upgrade --install cert-manager jetstack/cert-manager --namespace cert-manager --create-namespace -f values.yaml

kubectl apply -f clusterissuer.yaml
