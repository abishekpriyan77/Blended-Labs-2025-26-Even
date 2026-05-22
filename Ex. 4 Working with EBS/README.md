# Lab 4 – Working with Amazon Elastic Block Store (EBS)

## Author

* **Name**: ABISHEIK PRIYAN V
* **Register Number**: 212224230005


---

## Objective

The objective of this experiment is to understand how Amazon Elastic Block Store (EBS) provides persistent block-level storage for EC2 instances. This lab focuses on creating and attaching an EBS volume, formatting and mounting it on an EC2 instance, storing data, and verifying data persistence after instance reboot.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* An existing EC2 instance (Amazon Linux 2 preferred)
* Basic knowledge of Linux commands

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Amazon EBS
* SSH Client (Terminal / PuTTY)

---

## Tasks Performed

### Task 1: Explore Amazon EBS

Explore the Amazon EBS service through the EC2 dashboard. Observe different volume types such as General Purpose SSD (gp2/gp3), Provisioned IOPS SSD, Throughput Optimized HDD, and Cold HDD.

---

### Task 2: Create an EBS Volume

Create a new EBS volume in the same Availability Zone as the EC2 instance. Choose an appropriate size and volume type.

---

### Task 3: Attach EBS Volume to EC2 Instance

Attach the created EBS volume to the running EC2 instance as an additional block device.

---

### Task 4: Format the EBS Volume

Connect to the EC2 instance using SSH and format the attached volume with a file system (for example, ext4).

---

### Task 5: Mount the EBS Volume

Mount the formatted volume to a directory in the EC2 instance (for example, /data or /mnt/ebs).

---

### Task 6: Store Data in EBS Volume

Create files and directories inside the mounted EBS volume and store sample data.

---

### Task 7: Verify Data Persistence

Reboot the EC2 instance and verify that the data stored in the EBS volume is still available after reboot.

---

## Workflow 

1.Create a 1 GiB EBS volume in the same Availability Zone as the EC2 (Lab) instance and name it “My Volume”.

2.Attach “My Volume” to the EC2 instance using device name /dev/sdb.

3.Connect to the instance via Session Manager, create /mnt/data-store, format /dev/sdb (ext3), mount it, and update /etc/fstab.

4.Write a file to the mounted volume and create a snapshot named “My Snapshot” from the EBS volume.

5.Restore the snapshot as a new volume, attach it to the instance, mount it (e.g., /dev/sdc), and verify the file.


---

## Output Screenshots (Attach 3)

### Screenshot 1: EBS Volume Created

<img width="1920" height="948" alt="image" src="https://github.com/user-attachments/assets/a3822d79-60fc-4c32-a113-b418f7a6e3ec" />

<img width="1920" height="950" alt="image" src="https://github.com/user-attachments/assets/80efda4f-7543-4d32-a55c-7b5600254b50" />



---

### Screenshot 2: EBS Volume Attached to EC2

<img width="1920" height="956" alt="image" src="https://github.com/user-attachments/assets/e1686907-0c42-42bf-b301-5549f33b4c8b" />

<img width="1920" height="955" alt="image" src="https://github.com/user-attachments/assets/489d321e-4f49-43c7-a27e-951cf2aadb87" />

<img width="1920" height="953" alt="image" src="https://github.com/user-attachments/assets/8570378d-0179-470d-96ae-ca8546f3e691" />

<img width="1920" height="949" alt="image" src="https://github.com/user-attachments/assets/b6f9d536-7060-4f90-a4a2-3a358d5f81af" />


---

### Screenshot 3: Mounted Volume with Data

<img width="1920" height="959" alt="image" src="https://github.com/user-attachments/assets/43f244ae-e775-4a54-b8ee-98f9a2c7eb89" />

<img width="1920" height="952" alt="image" src="https://github.com/user-attachments/assets/523c0381-6466-4bfd-8680-4046411eebc6" />

<img width="1920" height="944" alt="image" src="https://github.com/user-attachments/assets/da268936-7703-467d-a1e0-6737c0416868" />

<img width="1920" height="952" alt="image" src="https://github.com/user-attachments/assets/392711b1-4250-467e-bd35-1b9474c3599f" />

---

## Result / Conclusion

This experiment demonstrated how Amazon EBS provides persistent storage for EC2 instances. By creating, attaching, formatting, and mounting an EBS volume, and by verifying data after reboot, the concept of durable block storage in the cloud was clearly understood.
