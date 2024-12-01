# Lecture11 – Virtualization

## Basic Concepts of Virtualization

### Virtualization & Cloud Computing
>Virtualization is an enabling Technology for cloud computing. Majority of high-performing clouds is powered by a virtualized infrastructure.

Because 

1. Virtualization makes it possible to

> * run many operating systems
 simultaneously on a single 
machine

2. Using this method, 

> *  a single physical instance of a resource or application may be shared by several users,

>* allowing them to access several computers simultaneously.

---

### Virtualization VS. Cloud Computing

> #### Virtualization abstracts
1. compute resources typically as virtual machines (VMs)

2. with associated storage and networking connectivity.

> ### Cloud Computing determines 

1. how those virtualized resources

2. are allocated, delivered, and presented.




Virtualization is not necessary to create a cloud environment, but it enables rapid scaling of resources in a way that non-virtualized environments find hard to achieve.

---

### What is Virtualization?

>The term virtualization broadly describes
1.  the separation of a resource or request for a service 
2.  from the underlying physical delivery of that service.

### Virtualization Infrastructure
> Virtualization Infrastructure provides 
 *  a layer of abstraction between computing (CPUs), storage and networking 
hardware, and the application running on it.

>Benefits:
* Deployment of virtual infrastructure is non-disruptive and the user experience is 
largely unchanged.

*  Gives administrators the advantage of managed pooled resources across the 
enterprise

*  Allows IT managers to be more responsive to dynamic organizational needs and to 
better leverage infrastructure investmen

---

### Virtualization Architectures

>### Type 1: Hypervisor (bare-metal) architecture

 A Type1 hypervisor, a software layer (handles virtualization tasks), is 
directly installed onto the hardware.
   
*  Hypervisor can discover and virtualize the system's available CPU, 
memory and other resources.

* Hypervisor can create a virtual image of the system's resources, which it 
can then provision to create independent VMs. 

*  Every VM remains completely isolated and independent of every other VM. 

* No VM within a system shares resources with or even has awareness of any 
other VM on that system.

>### Type 2: Hosted Architecture

* The system first installs the host OS on the hardware

*  Then Hosted Hypervisors or Type 2 hypervisors are installed -- such 
as VMware Workstation, KVM or Oracle VirtualBox -- atop that OS.

*  Similar to bare-metal virtualization, 
* 1. Every VM created is isolated from every other VM. 
* 2. VMs in a hosted system run in memory and the system can save or load them 
as disk files to protect, restore or duplicate the VM as desired.

|                           | **Type 1 hypervisor**                | **Type 2 hypervisor**                |
|---------------------------|--------------------------------------|--------------------------------------|
| **Also known as**         | Bare metal hypervisor.               | Hosted hypervisor.                   |
| **Runs on**               | Underlying physical host machine hardware. | Underlying operating system (host OS). |
| **Best suited for**       | Large, resource-intensive, or fixed-use workloads. | Desktop and development environments. |
| **Can it negotiate dedicated resources?** | Yes.                                 | No.                                  |
| **Knowledge required**    | System administrator-level knowledge. | Basic user knowledge.                |
| **Examples**              | VMware ESXi, Microsoft Hyper-V, KVM. | Oracle VM VirtualBox, VMware Workstation, Microsoft Virtual PC. |
