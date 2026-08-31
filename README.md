# Linux Basics - Level 1 & 2 Tasks

**Submitted by:** Abdulhamid Nuri  
**Date:** August 31, 2026  
**Environment:** Kali Linux (Windows WSL)

---

## Part 1: Level 1 — Basics (Steps 1–8)

### Screenshot 1: Directory & File Creation (Steps 1–3)
![Step 1-3](shot1.png)

**Terminal output:**
mkdir linux_test
cd linux_test
touch one.txt two.txt three.txt
ls
one.txt three.txt two.txt

text

### Screenshot 2: Text Input, Renaming, Copying & Deleting (Steps 4–7)
![Step 4-7](shot2.png)

**Terminal output:**
echo "This is the content for file one" > one.txt
echo "This is the content for file two" > two.txt
echo "This is the content for file three" > three.txt
mv three.txt final.txt
mkdir another_directory
cp one.txt another_directory/
rm two.txt

text

### Screenshot 3: Final Verification of Level 1 (Step 8)
![Step 8](shot3.png)

**Terminal output:**
pwd
/home/Noor/linux_test
ls
another_directory final.txt one.txt

text

---

## Part 2: Permissions & Ownership (Steps 9–10)

### Screenshot 4: Create secret.txt and set permissions to 640
![Step 9-10](shot4.png)

**Terminal output:**
touch secret.txt
echo "This is confidential" > secret.txt
chmod 640 secret.txt
ls -l secret.txt
-rw-r----- 1 Noor Noor 21 Aug 31 15:26 secret.txt

text

### 📖 Explanation: What does "640" mean?

`640` is an **octal (numeric) representation** of Linux file permissions. It is decoded into three digits:

- **First digit (6) = Owner permissions**:  
  Read (4) + Write (2) = 6.  
  *The owner can read and modify the file.*

- **Second digit (4) = Group permissions**:  
  Read (4) + 0 = 4.  
  *Members of the group can only read the file (cannot modify it).*

- **Third digit (0) = Others permissions**:  
  0 + 0 = 0.  
  *Everyone else on the system has zero access (cannot read, write, or execute).*

**Security context:** This enforces the **Principle of Least Privilege**. Only the owner can edit, the team can view, and unauthorized users are completely locked out. This is the standard permission model for sensitive configuration files (e.g., SSH private keys must be `600` to work).

---

### Screenshot 5: Change Owner and Group
![Ownership Change](shot5.png)

**Terminal output:**
sudo useradd -m testuser
sudo groupadd testgroup
sudo chown testuser:testgroup secret.txt
ls -l secret.txt
-rw-r----- 1 testuser testgroup 21 Aug 31 15:26 secret.txt

text

**Explanation:**  
The `chown` (Change Owner) command updated the ownership from `Noor` to `testuser` and the group to `testgroup`.  
*Note: `sudo` is required because changing the ownership of a file is a privileged operation—only the superuser (root) can reassign file ownership in Linux.*

---

## Final Verification Checklist

- [x] Steps 1–10 completed successfully.
- [x] `secret.txt` created.
- [x] Permissions set to `640` (`-rw-r-----`).
- [x] Explained the numeric meaning of `640`.
- [x] Changed owner to `testuser` and group to `testgroup`.
- [x] Verified with `ls -l`.

## Conclusion
All required tasks (1 through 10) have been executed successfully. The repository contains complete screenshot proof and a clear explanation of the underlying Linux security concepts.
