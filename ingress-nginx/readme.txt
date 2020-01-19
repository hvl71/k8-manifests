Bare-metal nginx ingress controller (on-premise/none-cloud)

Basic setup:
https://kubernetes.github.io/ingress-nginx/deploy/

Bare-metal considerations:
https://kubernetes.github.io/ingress-nginx/deploy/baremetal/

Good troubleshooting SO post (search for externalIP):
https://stackoverflow.com/questions/49845021/getting-an-kubernetes-ingress-endpoint-ip-address

How-to:
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/nginx-0.27.1/deploy/static/mandatory.yaml
wget https://raw.githubusercontent.com/kubernetes/ingress-nginx/nginx-0.27.1/deploy/static/provider/baremetal/service-nodeport.yaml
configure service-nodeport.yaml
kubectl apply -f ./service-nodeport.yaml

For convenience mandatory.yaml and service-nodeport.yaml are copied to this repo from the official https://github.com/kubernetes/ingress-nginx
