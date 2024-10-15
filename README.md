## Deploy en kubernetes usando kubectl y minikube
1. minikube start --insecure-registry true
2. eval $(minikube docker-env)
3. sudo docker build -t td-springboot ./springboot-app
4. minikube image load td-springboot
5. kubectl apply -f kubernetes.yaml
6. minikube service springboot-loadbalancer -n talento-digital --url
7. minikube delete