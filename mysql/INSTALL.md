helm repo add bitnami https://charts.bitnami.com/bitnami
helm repo update
helm upgrade --install mysql bitnami/mysql --create-namespace --namespace database -f values.yaml
