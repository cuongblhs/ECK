# Deploy ECK
kubectl create -f crds.yaml
kubectl apply -f operator.yaml

# Deploy APM
kubectl apply -f elasticsearch.yaml kibana.yaml apm-server.yaml  
kubectl get secret smartlog-es-elastic-user -o go-template='{{.data.elastic | base64decode}}'