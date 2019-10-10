# environment
## clone the repo & setup default config
```
git clone git@github.com:treytabner/hosted-cluster-poc.git && cd hosted-cluster-poc
cp config.sh.iks_example config.sh
```

## setup an ansible 2.8 virtualenv
```
virtualenv ~/ansible-2.8
. ~/ansible-2.8/bin/activate
cd ansible && pip3 install -r requirements.txt
```

## deploy managed master control plane
```
export NAMESPACE=hosted-example
export KUBECONFIG=/path/to/kubeconfig
ansible-playbook managed-master.yml
```
