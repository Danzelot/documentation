# Overview over our machines
The current Norwegian academic HPC infrastructure consists of three systems, located in Tromsø ([Stallo](http://hpc-uit.readthedocs.io/en/latest/help/faq.html), [Fram](quick/fram.md)) and Trondheim ([Saga](quick/saga.md)).

Each of the facilities consists of a compute resource (a number of compute nodes each with a number of processors and internal shared-memory, plus an interconnect that connects the nodes), a central storage resource that is accessible by all the nodes, and a secondary storage resource for back-up (and in few cases also for archiving). All facilities use variants of the UNIX operating system (Linux, AIX, etc.).

Additionally, [NIRD](storage/nird.md) provides storage and archiving services for research data.

## Comparison between current hardware

The table below compares the available systems with respect to the type of applications they are suited for.

|Resource |	Job types |	Memory (min/max) |	Cores/Node |
| :------------- | :------------- | :------------- | :------------- |
| Saga |    A   P   S   L | 186/3066 |  24/64 |
| Stallo |	P   S   L |	32/128 |	16/20 |
| Fram |	P&ensp;&ensp;&ensp;L |	64/512 |	32 |

**A** means the resource supports GPU-accelerated jobs, **P** means the resource supports parallel jobs, **S** means the system supports serial jobs, and **L** means that large I/O jobs are supported.
The **Memory** column specifies physical node memory in Gigabytes (GiB). Saga and Stallo provide a few large memory nodes.
The **Cores** column is the number of physical cores in each node.

The resource allocation committee (RFK) manages a part of the total cores on the resources for national allocations. The national share is 9824 cores on Saga, 13796 cores on Stallo, and approximately 31600 cores on Fram.

The following considerations should be kept in mind when selecting a system to execute applications:

* Saga and Stallo are throughput systems. These systems can be used for sequential (single-threaded) as well as parallel applications.

* Fram is a system for large scale parallel (distributed-memory) applications. Applications that use less than 128 cores (4 nodes) for production are discouraged. Requests for access to execute applications that use fewer cores are often rejected or moved to other systems.

* Saga, Stallo and Fram run CentOS Linux distributions. In case you need to install a specific software package, please make sure that you know for which environments the software is supported, before choosing a system.