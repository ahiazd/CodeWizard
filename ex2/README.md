Open ldap on K8S cluster 

on minikube :
1. create openldap namespace- kubectl create openldap 
2. Run oldap.yaml on your cluter with kubectl apply -f oldap.yaml -n openldap
3. Run minikube tunnel

4. run `kubectl -n openldap get svc | grep phpldap' to get the ip and port and open the ldap admin UI
