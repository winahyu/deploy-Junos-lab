# deploy-vqfx-lab
Ansible playbooks to manage the vQFX Lab in the Openstack with Contrail.

Status:

Using single playbook with the extra parameters to differentiate between deployment type, the selections are CREATE or DESTROY,

### other parameters :

Username : openstack username credential <br>
Password : openstack password credential <br>
NumberofPods : Number of Pods need to be created <br>
PodPrefix    : Pod prefix name <br>
DeployType   : DESTROY or CREATE <br>


### Provisioning Lab (all pods):

```
ansible-playbook deploy.yaml -e DeployType=CREATE -e Username=admin -e PodPrefix=VQFX-LAB-POD -e NumberofPods=1 -e Password=*****
```

### Deprovisioning Lab (all pods):

```
ansible-playbook deploy.yaml -e DeployType=DESTROY -e Username=admin -e PodPrefix=VQFX-LAB-POD -e NumberofPods=1 -e Password=*****
```
