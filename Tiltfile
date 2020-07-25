# Use "tilt up" to run container locally
# User "tilt down" to remove deployment

docker_build('go-kubernetes-local-image', '.', dockerfile='deployment/dockerfile')
k8s_yaml('deployment/k8s-deployment.local.yaml')
# k8s_resource('go-kubernetes', port_forwards=8030) # port forward a single pod to port 8030