# pre-req

1- google service account

2- kubernetes cluster with new service account, DNS admin permission

3- private cloud DNS zone

4- ingress controller nginx ingress with private ip

5- demo ingress with subdomain

## private ingress controller

helm install --name ingress-controller stable/nginx-ingress \
--set controller.service.annotations."cloud\.google\.com/load-balancer-type"="Internal"
