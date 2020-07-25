# go-kubernetes
Deploying a Go app on k8s

[Source](https://www.callicoder.com/deploy-containerized-go-app-kubernetes/)

## Deploy locally for dev
#### Deploy
`tilt up`

#### Delete deployment
`tilt down`

## Deploy from image pulled from Docker Hub registry

#### Deploy
`kubectl apply -f deployment/k8s-deployment.yaml`

#### Delete deployment
`kubectl delete deployment go-kubernetes`

## Testing Go app server
- Get the service's port as an env var: `kubectl get services | grep go-kubernetes-service | egrep -o ':(.*?)\/' | grep '[0-9]'`
- Make an HTTP request: `curl localhost:<service's port>`
