#Docker Stack K8s demo

This is the Docker Kuberenetes demo 

Using Docker for Mac/Windows enable Kubernetes. Next, run the following command:

    ```
    $ docker stack deploy --compose-file docker-stack.yml demo
    
    $ kubectl get pods
    
    NAME                     READY     STATUS    RESTARTS   AGE
    db-59ddfb4f8-j88tk       1/1       Running   0          1m
    web-57989d8497-zg9hc     1/1       Running   0          1m
    words-6f878d4d5b-5b99x   1/1       Running   0          1m
    ```

Check the status of the services

    ```
    $ kubectl get service

    NAME               TYPE           CLUSTER-IP      EXTERNAL-IP   PORT(S)          AGE
    db                 ClusterIP      None            <none>        55555/TCP        4m
    version: '3.3'
    kubernetes         ClusterIP      10.96.0.1       <none>        443/TCP          61d
    redis              ClusterIP      None            <none>        55555/TCP        4m
    result             ClusterIP      None            <none>        55555/TCP        4m
    result-published   LoadBalancer   10.100.65.123   <pending>     5001:32126/TCP   4m
    ```

