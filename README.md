# Proyecto Final - Curso Docker & Kubernetes

**Autora:** Cintia Denisse Mollinedo Laura  
**Curso:** [Curso Docker & Kubernetes - i-Quattro]

01. Ambiente Setup - Preparacion de entorno e instalaciones requeridas, con microk8s para un entorno de desarrollo, como cluster

1.1 Crear Máquina Virtual
lsb_release -a

<img width="1548" height="717" alt="image" src="https://github.com/user-attachments/assets/fea22190-e319-4ca4-ab24-660e8dd8787d" />

1.2 Instalando Status Microk8s, se ejecutan los siguientes comandos:
 sudo snap install microk8s --clas

root@cintiamollinedo k8s: microk8s enable dns ingress storage registry metrics-server metallb:192.168.1.200-192.168.1.210
root@cintiamollinedo k8s: microk8s status --wait-ready
root@cintiamollinedo k8s: microk8s kubectl get nodes

<img width="644" height="241" alt="image" src="https://github.com/user-attachments/assets/f1e67a5a-39d9-4b62-b475-ac96f8a199e6" />

Habilitando los addons tenemos:

root@cintiamollinedo k8s: microk8s enable dns
root@cintiamollinedo k8s: microk8s enable storage
root@cintiamollinedo k8s: microk8s enable ingress
root@cintiamollinedo k8s: microk8s enable metrics-server
root@cintiamollinedo k8s: microk8s enable metallb:192.168.1.200-192.168.1.210

Verificación del estado del cluster
root@cintiamollinedo k8s: microk8s status --wait-ready
root@cintiamollinedo k8s: microk8s kubectl get nodes

Despliegue de recursos (ejemplo ConfigMap y Secret)
root@cintiamollinedo k8s: microk8s kubectl apply -f 01-configmaps/api-config.yaml
root@cintiamollinedo k8s: microk8s kubectl apply -f 02-secrets/postgres-secret.yaml

Verificación de pods
root@cintiamollinedo k8s: microk8s kubectl get pods -A

<img width="590" height="101" alt="image" src="https://github.com/user-attachments/assets/3367fb77-6bba-4f61-90bb-59eb90ac344f" />
<img width="590" height="46" alt="image" src="https://github.com/user-attachments/assets/1b2d1cae-6543-4130-8257-7bb107f6a86a" />
<img width="595" height="42" alt="image" src="https://github.com/user-attachments/assets/7d123660-883e-4f1e-a060-57e2a87d5176" />
<img width="629" height="19" alt="image" src="https://github.com/user-attachments/assets/f42fa09c-e331-45da-b7dc-d5e941605f60" />


1.3 Despliegue del Proyecto integrador

root@cintiamollinedo k8s: kubectl get all -n proyecto-integrador

Este comando mostrará una tabla con varias secciones:

** Pods

Nombre del pod (por ejemplo: api-6cdf65cd-f6w6g, frontend-75cc98dd59-cbjt, postgres-0, redis-76ccfc6df-fw6k8).
READY (ej. 1/1 o 2/2).
STATUS (ej. Running).
RESTARTS (ej. 0).
AGE (tiempo desde que se creó, ej. 69m).

** Services

Nombre (ej. api-service, frontend-service, postgres-headless, redis-service).
TYPE (ClusterIP).
CLUSTER-IP (ej. 10.152.183.55).
PORT(S) (ej. 8080/TCP, 5432/TCP, 6379/TCP).
AGE.

**Deployments y ReplicaSets

Nombre del deployment (ej. apps/api, apps/frontend, apps/redis).
READY, UP-TO-DATE, AVAILABLE.
AGE.

**StatefulSets

Nombre (ej. apps/postgres).
READY y AGE.

**HorizontalPodAutoscaler (si está habilitado)

Nombre (ej. api-hpa).
Targets (CPU/Memoria).
MINPODS, MAXPODS, REPLICAS, AGE.



1.4 Navegador accediendo al frontend via IP de MetalLB

 
 
