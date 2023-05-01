# pre-req

1- google service account 

default compute engine service account

OR

roles/logging.logWriter<br />
roles/monitoring.metricWriter<br />
roles/monitoring.viewer<br />
roles/stackdriver.resourceMetadata.writer<br />
roles/storage.objectViewer<br />
roles/artifactregistry.reader<br />

OR

roles/container.nodeServiceAccount

2- kubernetes cluster with new service account, DNS admin permission

3- private cloud DNS zone

4- ingress controller nginx ingress with private ip

5- demo ingress with subdomain

## private ingress controller

helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx

helm install ingress-controller ingress-nginx/ingress-nginx 

internal type için annotation ekleme >>> cloud.google.com/load-balancer-type: "Internal" 
