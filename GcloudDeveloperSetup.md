# Dowload gcloud sdk

# Get gcloud kubectl context
gcloud container clusters get-credentials <clustername>

# Switch kubectl context
kubectl config get-contexts
kubectl config use-context <contextname> 

# Enable Cloud Build API

# Update skaffold and deployment


# Created Ingress and loadbalancer for cluster
kubectl create clusterrolebinding cluster-admin-binding --clusterrole cluster-admin --user $(gcloud config get-value account)
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v0.43.0/deploy/static/provider/cloud/deploy.yaml

# update hosts file with loadbalancer IP

# Start the deployment
skaffold dev
