# My CIS-92 Project 

This repository has the starter code for CIS-92. 
By Joe Bonanno

| Key | Use | Default |
| --- | --- | --- | 
| ENV PORT= | 8000 | 8000 | 
| ENV SITE_NAME= | your site name | "Really Cool Site" | 
| ENV SECRET_KEY= | your secret | "defaultsecret" | 
| ENV DEBUG=| 1 or 0 | "1" | 
| ENV DATA_DIR=| "/data" | "/data" | 
| WORKDIR  | /mysite | /mysite | 

| secret.yaml |
| --- |
| SECRET_KEY: "joesbadkey" |
| POSTGRES_PASSWORD: "joes-bad-password" |
| POSTGRES_USER: "mysiteuser" |

| values-postgres.yaml |
| --- |
| username: mysiteuser |
| password: this-is-a-bad-password |
| database: mysite |
| postgresPassword: joes-bad-password |
|  resources: |
|    requests: |
|      memory: "512Mi" |
|      cpu: "500m" |
|      ephemeral-storage: "100Mi" |
|    limits: |
|      memory: "512Mi" |
|      cpu: "500m" |
|      ephemeral-storage: "100Mi" |


**Startup commands**  
helm install postgres oci://registry-1.docker.io/bitnamicharts/postgresql --values values-postgres.yaml  
kubectl apply -f deployment/pod.yaml  

**Turn Down**  
kubectl delete -f deployment/pod.yaml  
helm uninstall postgres