#step1:create namespace:
kubectl create -f ProjectName-namespace.yaml
#step2:install gitlab-runer via helm 
helm install gitlab-runner --namespace ProjectName -f gitlab-runner.yaml gitlab/gitlab-runner
#step3:create role && rolebinding
kubectl create -f ProjectName-role.yaml
