# Faster Way to Install
Just add the helm repo and run this in the cluster

helm upgrade --install open-webui open-webui/open-webui \
  --set ingress.enabled=true \
  --set ingress.host=openwebui.uplifttech.org \
  --set ingress.tls=true \
  --set ingress.annotations."kubernetes\.io/ingress\.class"=nginx \
  --set ingress.annotations."cert-manager\.io/cluster-issuer"=letsencrypt-prod
