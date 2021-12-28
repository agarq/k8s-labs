- Run the app in Kubernetes
The folder k8s-specifications contains the yaml specifications of the Voting App's services.

- First create the vote namespace
$ kubectl create namespace vote

- Run the following command to create the deployments and services objects:

$ kubectl create -f k8s-specifications/
deployment "db" created
service "db" created
deployment "redis" created
service "redis" created
deployment "result" created
service "result" created
deployment "vote" created
service "vote" created
deployment "worker" created

The vote interface is then available on port 31000 on each host of the cluster, the result one is available on port 31001.