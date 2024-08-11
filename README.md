# Mastering Service Mesh with Istio on AWS EKS using Terraform EKS Blueprints

### Deploy
```
terraform init
terraform plan
terraform apply
```

### Access CLuster
Run update-kubeconfig command:
```
aws eks --region us-west-2 update-kubeconfig --name eks_istio
```


### Destroy
```
terraform destroy -target=module.eks_blueprints_addons -auto-approve
terraform destroy -target=module.eks -auto-approve
terraform destroy -target=module.vpc -auto-approve
terraform destroy -auto-approve
```

