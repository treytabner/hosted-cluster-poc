# hosted-cluster-poc
Deploy an Openshift cluster that has its master components hosted within a namespace of another existing cluster.


### Deploying a hosted cluster
Perform the following commands to install the hosted cluster:

~~~
export KUBECONFIG=...                   # path to kubeconfig of an existing cluster
export NAMESPACE=hosted
cp config.sh.iks_example config.sh
./install-openshift.sh
~~~

Once the install script has completed, you can view your hosted cluster control plane:
~~~
oc -n $NAMESPACE get all
~~~