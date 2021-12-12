# Deploy ECK
kubectl create -f crds.yaml
kubectl apply -f operator.yaml

# Deploy APM
kubectl apply -f elasticsearch.yaml kibana.yaml apm-server.yaml