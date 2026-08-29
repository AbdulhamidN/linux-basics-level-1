# Linux Basics - Level 1 Task

**Submitted by:** Abdulhamid Nuri 
**Date:** August 29, 2026  
**Environment:** Kali Linux (Windows WSL / Terminal)

---

## Task Overview
This project demonstrates the successful completion of all 8 basic Linux file operations as required for Level 1 — Basics.

---

## Screenshot Proof

### Screenshot 1: Directory & File Creation (Steps 1–3)
This screenshot shows the creation of the `linux_test` directory, navigating into it, creating `one.txt`, `two.txt`, and `three.txt`, and listing them.

![Step 1-3](shot1.png)

**Terminal output (all in one block):**
mkdir linux_test
cd linux_test
touch one.txt two.txt three.txt
ls
one.txt three.txt two.txt

text

---

### Screenshot 2: Text Input, Renaming, Copying & Deleting (Steps 4–7)
This screenshot shows adding unique text to the files, renaming `three.txt` to `final.txt`, creating `another_directory`, copying `one.txt` into it, and deleting `two.txt`.

![Step 4-7](shot2.png)

**Terminal output (all in one block):**
echo "This is the content for file one" > one.txt
echo "This is the content for file two" > two.txt
echo "This is the content for file three" > three.txt
mv three.txt final.txt
mkdir another_directory
cp one.txt another_directory/
rm two.txt

text

---

### Screenshot 3: Final Verification (Step 8)
This screenshot shows the current working directory (`pwd`) and the final list of contents (`ls`) confirming the successful completion of all tasks.

![Step 8](shot3.png)

**Terminal output (all in one block):**
pwd
/home/Noor/linux_test
ls
another_directory final.txt one.txt

text

---

## Verification Checklist

- [x] **Step 1:** Created directory `linux_test`.
- [x] **Step 2:** Created files `one.txt`, `two.txt`, and `three.txt`.
- [x] **Step 3:** Listed the files to confirm creation.
- [x] **Step 4:** Added unique text to all three files.
- [x] **Step 5:** Renamed `three.txt` to `final.txt`.
- [x] **Step 6:** Created `another_directory` and copied `one.txt` into it.
- [x] **Step 7:** Deleted `two.txt`.
- [x] **Step 8:** Displayed the current directory and final contents.

## Conclusion
All tasks have been executed successfully on Kali Linux. The final directory contains exactly `another_directory`, `final.txt`, and `one.txt`, confirming `two.txt` is removed and the renaming/copying was successful.
