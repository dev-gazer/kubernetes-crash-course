####Kukbernetes Crash Course
This is a simple understanding on how Kubernetes work, not so far from a real world application, although it is conducted using Minikube structure.

##How to get started

- Clone the repo
```
$ git clone https://github.com/dev-gazer/kubernetes-crash-course.git
```

- Start Minikube
```
$ minikube start
```

- Apply the Mongo Config file
```
$ kubectl apply -f mongo-config.yaml
```

- Add the Mongo environment variables through the usage of mongo-secret.yaml
```
$ kubectl apply -f mongo-secret.yaml
```

- Deploy the Mongo database
```
$ kubectl apply -f mongo.yaml
```

- Deploy the webapp that will consume the Mongo database
```
$ kubectl apply -f webapp.yaml
```

####Retrieve the IP address and test the application on your browser
```
$ minikube ip
```

- Copy the IP Address and paste it on your browser URL bar. Do not forget to add the port as well. Look at webapp.yaml nodePort in any case.