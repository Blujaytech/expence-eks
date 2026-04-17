https://github.com/Blujaytech/expence-eks

cd expense-k8/
ls

kubectl apply -f namespace.yaml

kubectl get ns

cd mysql/
ls
vim manifest.yaml

kubectl apply -f manifest.yaml

kubectl get pods -n expense
cd ..
cd backend/

vim manifest.yaml

kubectl apply -f manifest.yaml
cd ..
cd frontend/
vim manifest.yaml

kubectl apply -f manifest.yaml

kubectl get pods -n expense

kubectl get svc -n expense

kubectl port-forward svc/frontend -n expense 8080:80

kubectl config set-context --current --namespace=expense

