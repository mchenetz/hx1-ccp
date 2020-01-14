# How-To: Create CCP Tenant Cluster in CPSG-Galaxy

In order to create a tenant cluster in CPSG-Galaxy for development/testing, please perform the following steps:

 1. CLONE glxy_ccp-env_manifest.json
 
 2. Add the necessary information for your required development environment:
 
	- [[USERNAME]]
	- [[CLUSTER_NAME]]
	- [[K8S_VERSION]] = [[1.14.8]]
	- [[CLUSTER_TYPE]] = [[vmware | azure | aks ]]
	- [[NODES]] = [[3 | 5 ]]
	- [[VCPU]] = [[2 | 4]]
	- [[SSH_KEY]]
  
3. Commit your changes and perform a PULL REQUEST

4. Once the request is approved, your tenant cluster will be automatically created and you will receive an email notifcation  

## Example JSON

       {
        "username": "username",
        "clusters": [
          {
            "cluster_name": "username_cluster-1",
            "cluster_type": "vmware",
            "k8s_version": "1.14.8",
            "nodes": "3",
            "vcpu": "2",
            "memory": "16384",
            "ssh_key": "ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIG94bb+s1tKhuSM7gko6HkmbrpHcFiXwwhAJHM59SSgj ccpuser-key"
        }

