# environment
## setup an ansible 2.8 virtualenv
```
virtualenv ~/ansible-2.8
. ~/ansible-2.8/bin/activate
pip3 install -r requirements.txt
```

## install ansible requirements
```
ansible-galaxy install -r requirements.yml
```

## deploy cluster
```
export NAMESPACE=hosted-example
export KUBECONFIG=/path/to/kubeconfig
ansible-playbook managed-master.yml
```

# todo
## split up master deploy process into multiple parts
- generate PKI
- render managed (hosted) YAML for control plane
- apply managed YAML to host cluster
- render user in-cluster YAML (using appropriate host endpoint, nodeport, api service IP, etc.)
- apply user YAML to hosted cluster

## worker deployment playbook
