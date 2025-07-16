
## 🧪 Group Policy Management Home Lab (Part 2): Applying and Testing GPOs

This lab is a **continuation** of my previous Group Policy Management setup, where I created Group Policy Objects (GPOs) using Windows Server and the Group Policy Management Console (GPMC). In this phase, I focus on **applying and testing** those GPOs on client machines to verify their effectiveness.

---

### 🎯 Objective

The goal of this lab is to:

* Apply pre-configured GPOs to domain-joined clients
* Test and validate whether GPOs are being enforced correctly
* Simulate a real-world setup with client-server interaction in a domain environment

---

### ✅ Prerequisites

Make sure the following components are ready before continuing:

* ✅ **Windows Server (Domain Controller)** installed
* ✅ **Group Policy Management Console (GPMC)** installed
* ✅ **GPOs already created** in GPMC
* ✅ A **Windows 10/11 Pro or Enterprise** client machine (VM or physical)
* ✅ Client machine must be **domain-joined**



### 🖥️ Setting Up the Windows Client VM

If you need a test machine:

* Download the **Windows 10/11 Enterprise evaluation ISO** from Microsoft
* Create a virtual machine using **VirtualBox**, **Hyper-V**, or **VMware**
* Install the OS and connect it to the same virtual network as your Domain Controller
* Join the client to your domain:

  ```
  Settings > System > About > Rename this PC (join domain)
  ```

---

### ⚙️ Applying the GPO

Steps followed in the lab:

1. ✅ Log in to the **Domain Controller**
2. ✅ Ensure that the GPO is **linked** to the correct **OU** where the client resides
3. ✅ Use the **Group Policy Management Console** to:

   * Verify GPO links
   * Force a **Group Policy update**:

     ```
     gpupdate /force
     ```
4. ✅ On the client machine:

   * Reboot or run `gpupdate /force`
   * Use `gpresult /r` or `rsop.msc` to confirm applied policies
   * Check for enforcement (e.g., password complexity, lock screen, disabled control panel, etc.)

---

### 🧪 Test Cases Used

In this lab, I tested the following GPO behaviors:

| GPO Feature Tested      | Expected Result                 | Test Outcome |
| ----------------------- | ------------------------------- | ------------ |
| Password Policy         | Enforces min. 8-char complexity | ✅ Passed     |
| Lock Screen Timeout     | Locks after 5 min of inactivity | ✅ Passed     |
| Disable Control Panel   | Prevents access via UI          | ✅ Passed     |
| Windows Update Settings | Automatic install enabled       | ✅ Passed     |

---

---

### 📌 Why This Lab Matters

This part of the lab proves my ability to:

* **Deploy and manage policies in an enterprise-like environment**
* **Troubleshoot client-server GPO application issues**
* **Verify security and configuration enforcement using built-in tools**

It reinforces my **hands-on knowledge of Windows Server administration**, **AD DS**, **client-domain interaction**, and **GPO troubleshooting**—essential skills for any **System Administrator**, **IAM Engineer**, or **Cybersecurity Analyst**.

---


