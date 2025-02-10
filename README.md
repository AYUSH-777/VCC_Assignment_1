# **Microservice Deployment Using VirtualBox**  

## **Overview**  
This project demonstrates the process of creating and configuring multiple Virtual Machines (VMs) in VirtualBox, setting up network communication, and deploying microservices using **Node.js (Express.js)** and **Python (Flask)**. The goal is to simulate a distributed system where different VMs host different microservices while maintaining seamless communication.  

## **1️⃣ Virtual Machine Setup**  
- Installed **VirtualBox** and created multiple **Ubuntu VMs**.  
- Allocated **4GB RAM** and **30GB storage** per VM for optimal performance.  
- Configured the required network settings for inter-VM communication.  

## **2️⃣ Network Configuration**  
- Configured **two network adapters** for each VM:  
  - **NAT (Adapter 1)**: Provides internet access.  
  - **Internal Network (Adapter 2, intnet)**: Enables direct communication between VMs.  
- Enabled **Promiscuous Mode** to allow unrestricted data transmission.  

## **3️⃣ Network Testing**  
- Verified connectivity using `ping` commands between VMs.  
- Successful responses confirmed correct network setup.  

## **4️⃣ Microservice Deployment**  
### **Node.js Microservice (Node.js VM)**  
- Installed **Node.js** and **Express**.  
- Created a basic REST API responding with:  
  ```plaintext
  Microservice Running!
  ```
- Runs on port **3000**.  

### **Flask REST API (Flask VM)**  
- Installed **Python** and **Flask**.  
- Created an API responding with:  
  ```plaintext
  Microservice VM is running!
  ```
- Runs on port **3307**.  

## **5️⃣ Testing Microservice Communication**  
- Used `curl` from the **Tester VM** to verify services:  
  ```sh
  curl http://192.168.100.13:3000/  # Node.js Microservice
  curl http://192.168.100.10:3307/  # Flask REST API
  ```
- Successful responses confirmed proper deployment and accessibility.  

## **6️⃣ Results & Observations**  
✅ Inter-VM communication was successfully established.  
✅ Microservices were deployed and accessible over their respective ports.  
✅ No packet loss observed during network tests.  

## **7️⃣ Conclusion**  
This project successfully demonstrates **VM setup, network configuration, and microservice deployment** using VirtualBox. The implementation highlights how VirtualBox can effectively simulate a **distributed microservice architecture** for testing and development purposes.  

## **📌 Technologies Used**  
- **VirtualBox** (for VM creation and configuration)  
- **Ubuntu** (as the operating system for VMs)  
- **Node.js & Express** (for the backend microservice)  
- **Python & Flask** (for the REST API)  
- **cURL & Ping** (for network and service testing)  

---
