
# **Lab 1: Create and Connect to Windows EC2 Machine**

## **Overview**
This lab demonstrates the process of creating an **Amazon EC2 instance** with a Windows operating system, configuring it for access, and connecting to the instance using Remote Desktop Protocol (RDP).

---

## **Technologies Used**
- **Amazon EC2**: Virtual server in the cloud.
- **RDP (Remote Desktop Protocol)**: For connecting to the Windows instance.
- **AWS Management Console**: To configure and manage the EC2 instance.

---

## **Steps Covered**

### **1. Launch a Windows EC2 Instance**
1. **Navigate to EC2 Service**:
   - Log in to the AWS Management Console and go to **EC2**.
2. **Create a New Instance**:
   - Select the "Launch Instance" option.
   - Choose a **Windows Server AMI** (e.g., Windows Server 2019 or 2022).
   - Select an **instance type** (e.g., `t2.micro` for free tier).
3. **Configure Key Pair**:
   - Create a new key pair (or use an existing one).
   - Download the key pair `.pem` file (keep it secure!).
4. **Security Group**:
   - Allow inbound RDP traffic (port `3389`) in the security group.
   - Restrict access to specific IPs for enhanced security.
5. **Launch Instance**:
   - Review settings and launch the instance.

---

### **2. Retrieve Administrator Password**
1. Wait for the instance's state to change to **Running**.
2. Select the instance, then go to the **Actions** menu → **Security** → **Get Windows Password**.
3. Upload the `.pem` file to decrypt the password.
4. Save the password securely.

---

### **3. Connect to the Instance**
1. Open **Remote Desktop Connection** (RDP) on your local machine.
2. Enter the public IP address of the EC2 instance.
3. Use the administrator username (default: `Administrator`) and the decrypted password.
4. Connect to the Windows instance.

---

### **4. Configure the Windows Instance**
- Optionally, install software, configure roles, or perform tasks as needed on the Windows instance.
- Ensure all configurations meet your security and operational requirements.

---

## **How to Use This Repository**
1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```
2. The repository includes:
   - Diagrams of the EC2 configuration process.
   - Sample configurations for security groups.

---

## **Expected Outcome**
- Successfully created and connected to a Windows EC2 instance.
- Instance ready for further configurations or application deployment.

---

## **Best Practices**
- Restrict RDP access to specific IP addresses in the security group.
- Use strong passwords and store them securely.
- Regularly monitor and update your EC2 instance to maintain security.

---

## **License**
This project is licensed under the MIT License. See the `LICENSE` file for more details.

---

Feel free to add or adjust content based on your specific lab setup!
