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

**Startup commands**  
kubectl apply -f deployment/pod.yaml  

**Turn Down**  
kubectl delete -f deployment/pod.yaml