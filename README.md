# DIO_Bootcamp_Azure_AI
Online bootcamp focused on Azure Cloud and Artificial Intelligence.

# Azure (Microsoft Cloud)

## Basic Steps
1. **Create a new account**  
[Create your free Azure account or pay-as-you-go | Microsoft Azure](https://azure.microsoft.com/pt-br/pricing/purchase-options/azure-account)  
**Note:** If you're a student, your university may provide you with additional benefits.

2. **Log in to your account**

## Key Concepts

- **Cloud Computing:** Storage, data processing, software, and networking are provided over the internet instead of being hosted on local company servers. Resources can be consumed on demand, meaning users are only charged for what they use. This enables scalability, flexibility, agility, and remote access.

- **Scalability:** The ability to adjust resources to meet changing (higher or lower) demand. Users pay only for what they consume.

- **Reliability:** Cloud infrastructure is distributed across multiple regions, so if one fails, others can maintain availability.

- **Predictability:** Trust in the cloud environment to use optimal resources that support the growth and advancement of user technology.

- **Security:** Offers a variety of tools and services to ensure data protection.

- **Governance:** Includes internal auditing features that notify users of non-compliance and provide tools to mitigate risks.

- **Manageability:** Users have control over which resources they use and how they are configured.

- **SLA (Service Level Agreement):** A commitment by the cloud provider guaranteeing a certain level of service availability.

- **Infrastructure Models:** On-Premises, Cloud, and Hybrid
  - **On-Premises (local):** Physical infrastructure (e.g., data centers) is hosted within the company. Offers more customization and control, but it's expensive and requires physical space.
  - **Cloud (remote):** Infrastructure is hosted off-site and maintained by providers (e.g., Azure, AWS). It is more cost-effective, scalable, and flexible, but depends on internet connectivity.
  - **Hybrid:** A combination of on-premises and cloud infrastructure. Offers greater flexibility by allowing companies to choose the best storage location (local or remote) based on their needs. However, it can be more complex to manage.

# Quickstart: Create a Windows Virtual Machine in the Azure Portal

This guide walks you through creating a Windows Server 2022 Datacenter virtual machine (VM) using the Azure portal. It's ideal for testing, learning, or development purposes.

> **Note:** If you don't have an Azure subscription, you can create a free account at [https://azure.microsoft.com/free](https://azure.microsoft.com/free).

---

## 📌 Prerequisites

- An active Azure subscription.
- A Remote Desktop Protocol (RDP) client to connect to the VM.

---

## 🚀 Steps to Create the Virtual Machine

### 1. Sign in to the Azure Portal

Navigate to [https://portal.azure.com](https://portal.azure.com) and sign in with your Azure account credentials.

### 2. Create a Virtual Machine

1. In the Azure portal, search for **Virtual machines** in the search bar at the top.
2. Click on **Virtual machines** under the "Services" section.
3. On the **Virtual machines** page, click **+ Create** and select **Azure virtual machine**.

### 3. Configure Basic Settings

On the **Basics** tab:

- **Subscription:** Select your Azure subscription.
- **Resource group:** Choose an existing resource group or click **Create new** to create one.
- **Virtual machine name:** Enter a name for your VM (e.g., `myVM`).
- **Region:** Select the Azure region closest to you.
- **Availability options:** Leave as default (`No infrastructure redundancy required`).
- **Image:** Choose **Windows Server 2022 Datacenter: Azure Edition - x64 Gen2**.
- **Azure Spot instance:** Leave as default (`No`).
- **Size:** Click **See all sizes** to select a VM size that fits your needs (e.g., `Standard_DS1_v2`).
- **Administrator account:**
  - **Username:** Enter a username (e.g., `azureuser`).
  - **Password:** Enter a secure password and confirm it.
- **Inbound port rules:**
  - **Public inbound ports:** Select **Allow selected ports**.
  - **Select inbound ports:** Choose **RDP (3389)** to enable remote desktop access.

Click **Next: Disks >** to proceed.

### 4. Configure Disks

On the **Disks** tab:

- **OS disk type:** Choose between **Premium SSD**, **Standard SSD**, or **Standard HDD** based on your performance and cost requirements.

Click **Next: Networking >** to continue.

### 5. Configure Networking

On the **Networking** tab:

- **Virtual network:** Select an existing virtual network or create a new one.
- **Subnet:** Choose a subnet within the selected virtual network.
- **Public IP:** Select **Create new** to assign a public IP address.
- **NIC network security group:** Choose **Basic**.
- **Public inbound ports:** Ensure **RDP (3389)** is selected to allow remote desktop access.

Click **Next: Management >** to proceed.

### 6. Configure Management Options

On the **Management** tab:

- **Monitoring:** Decide whether to enable **Boot diagnostics** and **OS guest diagnostics** based on your requirements.

Click **Next: Advanced >**, then **Next: Tags >**, and finally **Next: Review + create >**.

### 7. Review and Create

- Review all the configurations you've made.
- Ensure that the **Validation passed** message appears at the top.
- Click **Create** to start the deployment.

Azure will begin provisioning your virtual machine. This process may take a few minutes.

---

## 🔗 Connect to the Virtual Machine

Once the deployment is complete:

1. Navigate to the **Virtual machines** section in the Azure portal.
2. Click on your newly created VM (e.g., `myVM`).
3. On the VM's overview page, click **Connect** and select **RDP**.
4. Click **Download RDP File**.
5. Open the downloaded `.rdp` file with your RDP client.
6. Enter the username and password you specified during VM creation.
7. Click **Connect** to access your VM.

---

## 🧹 Clean Up Resources

To avoid incurring charges:

1. In the Azure portal, go to **Resource groups**.
2. Select the resource group you used for the VM.
3. Click **Delete resource group**.
4. Confirm the deletion by typing the resource group name.
5. Click **Delete**.

This action will remove all resources associated with the VM.

---

## 📚 Additional Resources

- [Azure Virtual Machines Documentation](https://learn.microsoft.com/en-us/azure/virtual-machines/)
- [Azure Pricing Calculator](https://azure.microsoft.com/en-us/pricing/calculator/)
- [Azure Free Account](https://azure.microsoft.com/free)

---

*This guide is based on the official Microsoft documentation: [Quickstart: Create a Windows virtual machine in the Azure portal](https://learn.microsoft.com/en-us/azure/virtual-machines/windows/quick-create-portal).*

