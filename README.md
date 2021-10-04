# cs3219-devops

## Command to build all docker images
`docker build -t cs3219/mariadb:1.0.0 ./mariadb;
docker build -t cs3219/catalog-service:1.0.0 ./catalog-service;
docker build -t cs3219/customer-service:1.0.0 ./customer-service;
docker build -t cs3219/order-service:1.0.0 ./order-service;
docker build -t cs3219/api-gateway:1.0.0 ./api-gateway`

## Create namespace
`kubectl apply -f ./kubernetes/namespace.yaml`

## Command to deploy and create all services
`kubectl apply -f "./kubernetes/01 - mariadb-statefulset.yaml";
kubectl apply -f "./kubernetes/02 - mariadb-service.yaml";
kubectl apply -f "./kubernetes/03 - catalog-deployment.yaml";
kubectl apply -f "./kubernetes/04 - catalog-service.yaml";
kubectl apply -f "./kubernetes/05 - customer-deployment.yaml";
kubectl apply -f "./kubernetes/06 - customer-service.yaml";
kubectl apply -f "./kubernetes/07 - order-deployment.yaml";
kubectl apply -f "./kubernetes/08 - order-service.yaml";
kubectl apply -f "./kubernetes/09 - api-gateway-deployment.yaml";
kubectl apply -f "./kubernetes/10 - api-gateway-service.yaml"`

## View all elements in cs3219 namespace
`kubectl get all -n cs3219`