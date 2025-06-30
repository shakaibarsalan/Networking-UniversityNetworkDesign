## Project Overview

This project presents an **efficient IP addressing and subnetting plan** for a university network comprising eight departments. The design leverages **Variable Length Subnet Masking (VLSM)** to optimize address usage, ensure scalability, and minimize wastage. The network is based on the **20.20.10.0/22** address block, providing a total of 1024 IP addresses for allocation[1].

## Objectives

- **Efficiently allocate IP addresses** to each department based on size and future growth.
- **Minimize address wastage** by using VLSM.
- **Ensure scalability** for future network expansion.
- **Provide clear documentation** for network management and troubleshooting.

## Department Categorization & Subnet Allocation

Departments are categorized by size to determine subnet requirements:

- **Large:** Computer Science
- **Medium:** Electrical Engineering, Mechanical Engineering, Civil Engineering, Library
- **Small:** Admin Office, Hostel, Faculty Block

| Department           | Subnet ID           | Subnet Mask         | Usable Hosts | Usable Range                  |
|----------------------|---------------------|---------------------|--------------|-------------------------------|
| Computer Science     | 20.20.8.0/24        | 255.255.255.0       | 254          | 20.20.8.1 – 20.20.8.254       |
| Electrical Engg.     | 20.20.9.0/25        | 255.255.255.128     | 126          | 20.20.9.1 – 20.20.9.126       |
| Library              | 20.20.9.128/25      | 255.255.255.128     | 126          | 20.20.9.129 – 20.20.9.254     |
| Mechanical Engg.     | 20.20.10.0/25       | 255.255.255.128     | 126          | 20.20.10.1 – 20.20.10.126     |
| Civil Engg.          | 20.20.10.128/25     | 255.255.255.128     | 126          | 20.20.10.129 – 20.20.10.254   |
| Hostel               | 20.20.11.0/26       | 255.255.255.192     | 62           | 20.20.11.1 – 20.20.11.62      |
| Admin Office         | 20.20.11.64/26      | 255.255.255.192     | 62           | 20.20.11.65 – 20.20.11.126    |
| Faculty Block        | 20.20.11.128/26     | 255.255.255.192     | 62           | 20.20.11.129 – 20.20.11.190   |
| **Free Space**       | 20.20.11.192/26     | 255.255.255.192     | 62           | 20.20.11.193 – 20.20.11.254   |

- **Total usable IPs allocated:** 944
- **Free/Reserved IPs:** 64 (for future expansion or infrastructure)[1]

## Why VLSM?

- **Address blocks are sized according to actual departmental needs**, reducing unused IPs.
- **Supports future scalability**: Reserved subnets can be allocated as departments grow.
- **Facilitates easier network management** and periodic review for reallocation if needed[1].

## Implementation Steps

1. **Subnet Planning:** Analyze each department's current and projected device count.
2. **VLSM Calculation:** Assign subnet masks to each department based on size.
3. **Address Assignment:** Allocate subnets as per the table above.
4. **Documentation:** Maintain detailed records of all allocations.
5. **Simulation:** (Optional) Implement the design in Cisco Packet Tracer for validation.

## Challenges & Solutions

- **Growth Beyond Allocation:** If a department outgrows its subnet, periodic reviews and the reserved free space allow for flexible reallocation.
- **Documentation:** Comprehensive documentation ensures smooth management and troubleshooting[1].

## Files Included

- **Subnetting Plan Report:** Detailed breakdown of subnetting and allocation (see PDF report).
- **Packet Tracer File:** (If provided) Network simulation for practical validation.

## Contact

- **Author:** Muhammad Shakaib Arsalan (F2022266626)
- **Course:** CC3071, UMT Lahore
- **Instructor:** Sir Usman Ul Haq

> This VLSM-based subnetting plan provides efficient, scalable, and well-documented IP address management for the university, meeting all objectives outlined in the assignment[1].

**End of README**
