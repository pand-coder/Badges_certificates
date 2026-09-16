AZ-900 prep important overview

Describe Cloud COncepts (35–40%)



Describe cloud computing



Cloud computing is the delivery of computing services over the internet. Computing services include common IT infrastructure such as virtual machines, storage, databases, and networking.

cloud computing changes infrastructure planning from long procurement cycles to on-demand provisioning.

Cloud platforms also offer global reach, so teams can place services closer to users and design for regional resilience without building multiple physical datacenters.



Responsibilities get shared between the cloud provider and the consumer.

Physical security, power, cooling, and network connectivity are the responsibility of the cloud provider.

At the same time, the consumer is responsible for the data/information stored in the cloud and also responsible for access security



IaaS places the most responsibility on the consumer, with the cloud provider being responsible for the basics of physical security, power, and connectivity.

PaaS, being a middle ground between IaaS and SaaS, rests somewhere in the middle and evenly distributes responsibility between the cloud provider and the consumer.

SaaS places most of the responsibility with the cloud provider.



The cloud models define the deployment type of cloud resources. The three main cloud models are: private, public, and hybrid.





public cloud - shared infra provided by cloud provider - managed by cloud provider

private cloud - infra dedicated to a single company - managed by single or by any another org

hybrid - mixture ofpublic and private cloud - managed by both customer and cloud provider

MultiCloud -  using mutlitple cloud providers . use different features from different cloud provider or cloud migration. Deal with two (or more) public cloud providers and manage resources and security in both environments.

Azure Arc -  is a set of technologies that helps manage your cloud environment.

Azure Arc can help manage your cloud environment whether it's a public cloud solely on Azure, a private cloud in your datacenter, a hybrid configuration, or even a multicloud environment running on multiple cloud providers at once.

Azure VMWare Solution -  already established with VMware in a private cloud environment but want to migrate to a public or hybrid.







consumption-based model - you pay for resources allocated to you

Don't allocate more resources than you need

Ensure you utilize the resources you allocate

CapEx refers to up-front spending on physical infrastructure like servers, network hardware, and datacenter space.

OpEx refers to ongoing spending on services over time.



cloud computing is classified as an operational expense.



Cloud providers use a pay-as-you-go pricing model. You typically pay only for the services you consume, which helps you:



Plan and manage operating costs.

Run infrastructure more efficiently.

Scale as workload needs change.





Describe the benefits of using cloud services



Availability = An application and the systems it uses are accessible to users



Availability and Scale are very much important while building an application



Uptime is the amount of time a system, application, or service is available and working properly.

SLA is the formal agreement between a service provider and a customer

guaranteed percentage of time that a cloud service is expected to be available and operational.





Higher SLA = Less Downtime But May Increase Cost



high availability is considered to be 99% and higher '



scalability -



vertical scaling - scale up or down as per your requirement



horizontal sacking - scale out for more resources or scale back



elasticity - ability to scale up and down or out and back



fault refers to something that causes a problem and it occurs when failure happens

fault tolerance = maintain availability when a fault happens

disaster = large scale event

diasater recovery = planning Business continuity and disaster recovery

reliability = recover from failures and continue to function

predictability = move forward with confidence



Security restricts access to your resources to only those you allow.



Governance refers to the level of access someone has, what they can do with that access, and how they can do it.



manageability in cloud



Monitor your resources

scale as per your requirement

budget what you spnet

easily deploy and manage resources







Tools such as templates(repeatable deployments) help ensure that deployed resources meet your technical standards and regulatory requirements.



If you want patches and maintenance taken care of automatically, platform as a service or software as a service deployments may be the best cloud strategies for you.



Cloud providers are typically well suited to handle things like distributed denial of service (DDoS) attacks, making your network more robust and secure.



By establishing a good governance footprint early, you can keep your cloud footprint updated, secure, and well managed.



sustainability can be achieved by right size(matching resource to actual demand), automate disabling unused reosurces , optimize resources, track resource usage



Sustainability-aligned cloud practices



Examples of practices that support sustainability and cost efficiency include:



Scaling resources down when demand decreases

Turning off or deallocating resources that are not in use

Choosing efficient services and configurations to reduce overprovisioning

Using governance and monitoring to track usage trends and optimize deployments over time



Describe cloud service types



IAAS -> responsible for maintaining the hardware, network connectivity to the internet, and physical security.

Consumer is responsible for everything else

IaaS, you're essentially renting the hardware in a cloud datacenter



Lift-and-Shift Migration

What it means: You move your existing applications from your on-premises data center to the cloud without making major changes to the application.





Testing and Development



What it means: Developers often need temporary environments to test applications before deploying them to production.



With IaaS, you can quickly create and remove servers whenever needed.



ex: azure vm



PAAS ->

the cloud provider maintains the physical infrastructure, physical security, and connection to the internet. They also maintain the operating systems, middleware, development tools, and analytics services that make up a cloud solution.



focus on your application code, data, and access controls. Depending on service configuration, some networking and application security settings are shared.



Development Framework: PaaS provides ready-to-use development tools and built-in cloud features, enabling developers to build and deploy applications faster with less coding effort.



Analytics \& Business Intelligence: PaaS offers integrated analytics tools that help organizations analyze data, uncover insights, and make informed business decisions.

ex:azure app service,azure cosmos db



saas - infra,os and software provided by cloud

least responsibility for the consumer



ex: outlook,onedrive





Describe Azure architecture and services (35–40%)



Describe the core architectural components of Azure





Billing Account: The top-level billing entity that manages all subscriptions, invoices, and payment relationships.

Billing Profile: Represents an individual invoice and contains billing details such as payment methods, billing address, and payment settings.

Invoice Section: A subdivision within a billing profile used to organize and group charges by department, project, or team on the same invoice.





azure free acc -> popular products for 12 months , 200$ credit to use for first 30 days and accesss more than 65 services that are always free

azure freee student acc -> certail azure services, a credit to use in first 12 months and free access o certail software dev tools





Azure's core architectural components can be broken down into two main groupings: the physical infrastructure and the management infrastructure.



We are going through physical side



Azure Geography is a defined market area that contains one or more Azure regions and helps meet data residency and compliance requirements.

Azure region = It is a set of atleast one or more datacenters connected through a high-speed network within a specific geographic area

Most Azure regions are paired with another region within the same geography (such as US, Europe, or Asia) at least 300 miles away.





Avilability zone

physically separate datacenters within an Azure region. Each availability zone is made up of one or more datacenters equipped with independent power, cooling, and networking. An availability zone is set up to be an isolation boundary. If one zone goes down, the other continues working. Availability zones are connected through high-speed, private fiber-optic networks.



Azure services that support availability zones fall into three categories:



Zonal services: You pin the resource to a specific zone (for example, VMs, managed disks, IP addresses).

ex: vms,managed disks and ip addresses



Zone-redundant services: The platform replicates automatically across zones (for example, zone-redundant storage, SQL Database).

\-ex: Zone-redundant storage,specific zone



Non-regional services(global): Services are always available from Azure geographies and are resilient to zone-wide outages as well as region-wide outages.- ex: -Microsoft Entra ID, Azure Traffic Manager, and Azure DNS.



&#x20;



sovereign regions = is a specialized Azure region designed to meet strict government, regulatory, or data residency requirements and may have limited service availability compared to public Azure regions.





Hierarchy:



Geography → Region → Availability Zone → Data Center



In a one-direction pairing, the Primary region does not provide backup for its secondary region.



azure resource -any entity that you create and use within azure

each resource belongs to exactly one resource group



Resource Group - it is a logical container that holds related Azure resources for a solution or application.

It allows you to manage, monitor, secure, and organize multiple resources together.



Each resource group is in your azure subscription



how do you mange multiple azure subscriptions?

Management Groups = provides a way to mange azure subscriptions or hold another management subscription



subscriptions are a unit of management, billing, and scale. Subscriptions let you organize resource groups and control billing separately from access.



Billing boundary: Determines how an Azure account is billed. You can create multiple subscriptions for different billing requirements. Azure generates separate billing reports and invoices for each subscription.



Access control boundary: Azure applies access-management policies at the subscription level





Every Microsoft Entra tenant has a single top-level Tenant Root Group. All other management groups and subscriptions fold up to this root group, which lets you apply governance policies globally.



The Tenant Root Group is the highest-level management group in an Azure AD (Microsoft Entra ID) tenant. It sits above all other management groups and subscriptions and is automatically created when management groups are enabled. Policies and role assignments applied here can be inherited by all child management groups and subscriptions





tenant root group -> management group -> azure subscription/management group  -> reosurce group -> resources

is this the hierachy



### Describe Azure compute and networking services



compute - cloud resource that consumes cpu \& memory

onoute types - azure vm, azure container instances for manging small workloads ,Azure Functions is an event-driven, serverless compute option that doesn’t require maintaining virtual machines or containers



An image is a template that already includes an operating system and tools such as web hosting components.



vm size families nd names



B-series(Burstable, cost-efficient)
D-Series-(General Purpose)

E-Series-(Memory optimized)

F-Series-(compute optimized)

M-Series - Large memory footprint

L-Series - Storage optimized

N-series - Gpu enabled



VM names also carry useful sizing information. The base name indicates the family (or purpose), the number of vCPUs, and the hardware generation



how to read standard D2s\_V5



D: the VM family (general purpose in this case)

2: the number of vCPUs in this size

s: supports Premium SSD storage

v5: hardware generation for that family



Virtual Machine Scale Sets enable automatic scaling, load balancing, and centralized management of multiple identical VMs to improve availability and handle changing workloads efficiently. vms are scale dsuing auto-scale





Availability Sets improve VM resiliency within a region by distributing VMs across fault domains (hardware failures) and update domains (planned maintenance events). This reduces the risk of all VMs becoming unavailable at the same time.



Fault Domain: Protects against hardware, power, or network failures.

Update Domain: Ensures not all VMs are rebooted during planned maintenance.



azure virtual desktop



. Allow users to run application in a virtualized environment .



Azure IoT services help you connect, monitor, and manage devices.



Azure IoT Hub enables secure, bi-directional communication between cloud services and IoT devices.

Azure IoT Central provides a simplified software as a service (SaaS) IoT platform for solution builders.

Azure IoT Edge extends cloud capabilities to edge devices so some workloads can run closer to where data is generated.



Azure App Service: A PaaS service used to create, deploy, and host web applications in the cloud.

App Service Plan: A logical container that provides the compute resources and scaling capabilities for App Service applications.

&#x20;

With App Service, you can host most common app styles:

Web apps

API apps

WebJobs

Mobile apps



Azure Container Instances (ACI)



Run containers quickly without managing servers or clusters.



Azure Kubernetes Service (AKS)

Deploy and manage containerized applications using Kubernetes.



The Control Plane manages and orchestrates the Kubernetes cluster, while Worker Nodes run the containerized applications.



Azure virtual networks



Virtual network peering - connect 2 vnet's together

N/w traffic travels on microfost pvt n/w and it's unencrypted

you can peer Vnet's in same region or in different regions when peering Vnets in 2 different regions it's called global network peering



Azure DNS - helps you mange your dns records in azure

internet facing zones are called public zones

zones used for azure vnets are called private zones





Azure VPN gateway

* helps in building secure connection b/w azure Vnets and other networks
* It uses a gateway subnet that runs 2 or more vm's



Three types of vpn gateway

* Vnet-to-Vnet
* Site-to-Site
* Point-to-Site



key point: n/w speed i limited to 1.25 gb/second in azure vpn gateway



Azure Express Route

* Connects azure resources to on-premises networks
* upto 10Gbps
* u connect directly to MSEE (Microsoft Enterprise edge router)



micrososft calls an enterprise connection as circuit





Public endpoints

* A resource that has ip address and reachable over the internet



Private Endpoint

* Ip address only reachable over a private network



A resource can have both endpoints



Azure Tags are key-value labels used to organize resources and allocate costs for billing, reporting, and chargeback purposes



### Describe Azure storage services



Blob storage is used to store unstructured data such as images, videos, audio files, backups, and documents
A file stored in Blob Storage is called a blob, and blobs are organized inside containers, similar to folders on a hard drive.



Types of Blobs



Block Blob: Used for storing files such as documents, images, videos, and audio files.



Append Blob: Optimized for append operations and commonly used for log files.



Page Blob: Stores random-access files such as Virtual Hard Disks (VHDs) used by Azure Virtual Machines.



Azure Disks provide persistent block storage for Azure Virtual Machines and are available in HDD and SSD options.



OS Disk: Contains the operating system for the VM.

Data Disk: An additional disk attached to a VM for storing application data that must persist independently of the OS.



Azure Files is a fully managed SMB-based file share service that provides shared file storage in the cloud.



Accessible from Windows, Linux, and macOS.

Can be synchronized with on-premises servers using Azure File Sync.



Storage Tiers



Storage tiers are used to optimize cost and performance based on how frequently data is accessed.



Hot Tier – Used for frequently accessed data. It has a higher storage cost but a lower access cost.



Example: Active application data, website images.



Cool Tier – Used for data stored for longer periods and accessed occasionally. It has a lower storage cost but a higher access cost. - min:30 days



Archive Tier – Used for long-term storage of rarely accessed data. It offers the lowest storage cost but has a high retrieval time and access cost.

\- min: 180 days



Redundancy Options

LRS (Locally Redundant Storage): Keeps multiple copies of data within a single datacenter.

ZRS (Zone-Redundant Storage): Replicates data across multiple Availability Zones within a region.

GRS (Geo-Redundant Storage): Replicates data to a secondary region for disaster recovery.

GZRS (Geo-Zone-Redundant Storage): Combines zone redundancy and geo-replication for maximum protection.Both store in the same region



more broad explanation:



LRS (Locally Redundant Storage)-Microsoft stores 3 copies of your data within a single datacenter in the primary region.

ZRS (Zone-Redundant Storage)- Microsoft stores 3 copies of your data across multiple Availability Zones in the same region.

GRS (Geo-Redundant Storage)-Microsoft stores 3 copies of data using LRS in the primary region and another 3 copies using LRS in a paired secondary region.

GZRS (Geo-Zone-Redundant Storage)-Microsoft stores 3 copies across Availability Zones in the primary region (ZRS) and another 3 copies in a secondary region using LRS.



Storage Account Options



* Standard - General-purpose v2 for blob storage,azure files,queue storage and table storage -
* Premium - Block blobs storage - storage acc type for storing block blobs and append blobs that are in blob storage - offers lrs and zrs
* Premium - File share Storage - it's for file shares in azure files - offers lrs and zrs
* Premium - Premium page blobs - for storing page blobs - supports lrs



all use SSD for max performance



AZCopy



* Copy blobs and files to and from azure storage
* can copy entire directories
* It's a cli tool
* can be scripted

&#x20;

AzureStorage

* Azure Storage Explorer is a standalone desktop application that allows you to view, upload, download, and manage Azure Storage resources from Windows, macOS, and Linux. It provides a graphical interface for working with Azure Storage





AzureFileSync - utility to sync azure files to on-premises servers



Migration Options





Azure Migrate - migrates servers, Db's , Webapp's , etc.

can migrate from another cloud provier or on-premises



AZURE DATABOX - for migration of large amounts of data

Three offerings

* Databox disk - microsoft sends you 5 ssd's with 7 tb capacity of each
* Databox - plugin the the applinace and connect to netowrk its' of 80 tb
* Databaoz heavy - 1 pettabyte box on a wheel cart will be provided out of which 770 tb will be used



Datbox disk can be only used with one storage acc whereas others you can use upto 10 sotrage aaccs



### Describe Azure identity, access, and security



Service Principal → Identity(user, group, service principal r managed identity) for applications to access Azure resources.





Azure AD DS → Cloud-based version of Active Directory providing domain services such as LDAP, Kerberos, and Group Policy.

Managed Domain → Microsoft-managed AD domain.

Replica Set → Replicated domain controllers for high availability.'



Single Sign-On (SSO)

&#x20;Allows users to sign in once and access multiple applications without re-entering credentials.



Password Hash Synchronization (PHS)

&#x20;Synchronizes a hash of the on-premises Active Directory password to Microsoft Entra ID (Azure AD) for cloud authentication.



Pass-Through Authentication (PTA)

&#x20;User credentials are validated by an on-premises authentication agent instead of storing password hashes in the cloud.



Azure Multi-Factor Authentication (MFA)

&#x20;Requires an additional verification method (such as a mobile app, SMS, or phone call) along with a password to improve security.



Passwordless Authentication

&#x20;Allows users to sign in without a password using methods such as FIDO2 security keys, Temporary Access Pass (TAP), or certificate-based authentication.



Conditional Access Policy

&#x20;Applies access controls based on conditions such as user identity, location, device, risk level, or application being accessed.



Azure RBAC authorizes access to Azure resources based on a Security Principal, Role Definition, and Scope.









Role Definition

&#x20;A collection of permissions that determines what actions can be performed.



Examples: Owner, Contributor, Reader



Scope

&#x20;The level at which access is assigned.

Management Group

Subscription

Resource Group

Resource



Zero Trust → Never trust, always verify; assume a breach and continuously validate access.

Defense in Depth → Use multiple layers of security controls to protect resources and minimize the impact of an attack.



Microssoft Defender For CLoud



Security service protects axure,on-premises and other cloud resources

feature : security,regulatory complaince , workload protections
and constantly monitors security posture





### Describe Azure management and governance (30–35%)



#### Describe Cost Management in Azure



Factors that can affect costs



* Meters assigned to a specific resource
* how you purchase your resources
* some regions cost more than others

always review pricing page for your resources



Compare the pricing calculator and Total cost of ownership calculator



Pricing Calculator → Estimates the monthly cost of Azure services before deployment.



TCO Calculator → Estimates potential savings when migrating workloads from on-premises infrastructure to Azure.



Azure cost management and billing tool



* can analyze costs ,create budgets and set alerts



Azure Tags are key-value pairs applied to resources for organization, management, and cost allocation in billing and reporting.



Azure Blueprints help you deploy and standardize cloud environments by packaging resources, policies, role assignments, and templates into a reusable blueprint.



Azure Policy is a
governance service that defines and enforces rules for resource creation and management and enforces organizational rules and standards across Azure resources



Resource Locks prevent accidental changes or deletion of Azure resources.



Azure portal



cli tools

&#x20;

cloudshell - integrated into portal

powershell



get-azresource



&#x20;get-azresource | format-table



az resource list



\--output table



Azure arc

* Extend management and governance to resources outside of azure
* Arc-enabled servers bring azure management and governance features to on-premise and another clous environment
* Arc-enabled kubernetes for kubernetes clusters
* Arc-enbabled data services and application services



Azure Resource Manager (ARM) is the system for creating and managing resources enables predictability and repeatability with declarative syntax templates of json and xml





azure advisor



tools ensure high avilability and efficiency and also helps resolve problems regarding security and reccomendations



azure service health = provides ifnromation on azure service incidents

provides infor on planned maintainennance events that may impact you



azure monitor

provides metrics for your webapps and vms

create custom views and also provides application insights

for historical infor use log analystics



mistakes



Azure Reservations offers discounted prices on certain Azure services. Azure Reservations can save you up to 72 percent compared to pay-as-you-go prices. To receive a discount, you can reserve services and resources by paying in advance. Spending limits can suspend a subscription when the spend limit is reached



Azure pricing varies by region, so the location to which a resource is deployed affects cost, and outbound data transfers are billed based on type and destination.



Azure Policy enables you to define both individual policies and groups of related policies called initiatives. Azure Policy evaluates your resources and highlights resources that are not compliant with the policies you created. Azure Policy can also prevent noncompliant resources from being created.



Azure Monitor is a platform that collects metric and logging data, such as CPU percentages. The data can be used to trigger autoscaling.



Health advisories are issues that require that you take proactive action to avoid service interruptions, such as service retirements and breaking changes. Service issues are problems such as outages that require immediate actions.



Service endpoints are used to expose Azure services to a virtual network, providing communication between the two. ExpressRoute is used to connect an on-premises network to Azure. NSGs allow you to configure inbound and outbound rules for virtual networks and virtual machines. Peering allows you to connect virtual networks together.





Low storage costs and unlimited file formats make blob storage a good location to store backups and archives. Blob storage can be reached from anywhere by using an internet connection. Azure Disk Storage provides disks for Azure virtual machines. Azure Files supports mounting file storage shares.



Conditional Access allows administrators to control, allow, or deny access to resources based on certain signals. You can require that access to certain applications only be allowed if the users are using an approved client application. MFA is a process whereby a user is prompted during the sign-in process for an additional form of identification. Examples include a code on their mobile phone or a fingerprint scan.



Conditional Access in Microsoft Entra ID allows you to create policies based on conditions such as location, device, user, or risk level, and then require Multifactor Authentication (MFA) before granting access.



Microsoft Entra Domain Services provides managed Active Directory Domain Services (AD DS) capabilities without requiring customers to deploy or manage domain controllers. Microsoft Entra ID is a cloud identity service that does not provide AD DS functionality, managed identities are used for application authentication, and Azure App Service is an application-hosting platform.



Availability zones are primarily for virtual machines, managed disks, load balancers, and SQL databases.



Azure Cost Management allows you to create and manage cost and usage budgets by monitoring resource demand trends, consumption rates, and cost patterns. It also allows you to use historical data to generate reports and forecast future usage and expenditures.



Different services have different SLAs. Sometimes different tiers of the same service will offer different SLAs, which can increase or decrease the promised availability



ARM is the deployment and management service for Azure. It provides a management layer that enables you to create, update, and delete resources in an Azure account.



GRS uses LRS in both regions, while GZRS uses ZRS in the primary region and LRS in the secondary region.

To read secondary-region data before failover, enable read-access geo-redundant storage (RA-GRS) or read-access geo-zone-redundant storage (RA-GZRS).

Remember that the data in your secondary region may not be up-to-date due to RPO.



Microsoft Entra Connect synchronizes user identities between on-premises Active Directory and Microsoft Entra ID.



Microsoft Entra Domain Services provides managed domain services — domain join, group policy, LDAP, and Kerberos/NTLM authentication — without requiring you to deploy or maintain domain controllers in the cloud.

Because Microsoft Entra Domain Services integrate with your existing Microsoft Entra tenant, users can sign in to the managed domain with their existing credentials. Existing groups and user accounts also carry over, providing a smoother migration path.



When you create a Microsoft Entra Domain Services managed domain, you define a unique namespace. This namespace is the domain name. Two Windows Server domain controllers are then deployed into your selected Azure region. This deployment of DCs is known as a replica set.



Users are created in On-Prem Active Directory (AD DS).

Microsoft Entra Connect syncs them to Microsoft Entra ID.

Entra ID then syncs them to Microsoft Entra Domain Services



Microsoft Entra External ID is used to give people outside your organization secure access to your applications and resources. These external users can be:



Customers 👥

Partners 🤝

Vendors 🏢

Guest users 📧



Choose Reservations for predictable, long-running workloads with stable resource needs.

Choose Azure savings plan for compute when usage is steady but you need more flexibility across compute services.

Choose Spot pricing for fault-tolerant or interruptible workloads where lowest cost is the top priority.



Microsoft Purview is used to discover, classify, govern, protect, and monitor your organization's data wherever it exists. It gives a unified view of data across on-premises, multicloud, and SaaS environments



Azure Policy enables you to define both individual policies and groups of related policies, known as initiatives.



Resource Locks can be applied at three main Azure scopes:



Subscription level

Resource Group level

Individual Resource level



Microsoft Service Trust Portal is a portal that provides access to various content, tools, and other resources about Microsoft security, privacy, and compliance practices.



Bicep is a declarative language for deploying Azure resources through ARM. Compared to JSON ARM templates, Bicep is generally simpler and more concise.



Azure Status gives you a global picture of Azure health across all services and regions.

Service Health focuses on the Azure services and regions you actually use. Because you're signed in, Service Health knows which services matter to you and shows outages, planned maintenance, and health advisories relevant to your environment. You can set up alerts so you're notified automatically.

Resource Health zooms in on individual resources, such as a specific virtual machine. It tells you whether a resource is running normally or experiencing a problem, and whether the issue is on Azure's side or yours.



Azure Monitor is a platform for collecting, analyzing, and acting on data from your Azure resources and applications

