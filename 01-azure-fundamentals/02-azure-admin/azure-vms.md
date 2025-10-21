# Azure Virtual Machines (VMs)

## What is it?
Azure Virtual Machines are Infrastructure-as-a-Service (IaaS) offerings that allow you to run Windows or Linux servers in the cloud.

## Why use it?
- Host custom applications
- Run legacy workloads
- Create jump servers or bastion hosts
- Scale compute resources on demand

## How to create?
1. Go to Azure Portal → Virtual Machines → Create
2. Choose OS image (Windows/Linux), VM size, disk type
3. Configure networking (VNet, NSG, public IP)
4. Set admin credentials and enable monitoring
5. Review + Create

## CLI Example
```bash
az vm create \
  --resource-group myRG \
  --name myVM \
  --image UbuntuLTS \
  --admin-username azureuser \
  --generate-ssh-keys

Industrial Use Case -
Used by enterprises to host web apps, databases, and internal tools with full control over OS and software.

Best Practices -
Use managed disks

Enable boot diagnostics

Apply NSGs to restrict access

Use Azure Backup for recovery