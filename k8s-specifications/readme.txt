RUNNING THE APP IN KUBERNETES

The folder k8s-specifications contains the yaml specifications of the Voting App's services.

1. First create the vote namespace
$ kubectl create namespace vote

2. Run the following command to create the deployments and services objects:

$ kubectl create -f k8s-specifications/

The vote interface is then available on port 31000 on each host of the cluster, the result one is available on port 31001.

this example is from: https://github.com/dockersamples/example-voting-app


NOTES
The voting application only accepts one vote per client. It does not register votes if a vote has already been submitted from a client.
This isn't an example of a properly architected perfectly designed distributed app... it's just a simple example of the various types of pieces and languages you might see (queues, persistent data, etc), and how to deal with them in Docker at a basic level.