# Analysis-of-the-Disk-Structure-using-Sleuth-Kit

### NAME MOHAMMED IBRAHIM MN 
### REG 212223100034

## AIM:
To analyze the disk structure of a given disk image using Sleuth Kit tools in Kali Linux.

## DESIGN STEPS:
### Step 1:
Obtain or create a disk image file (e.g., disk.dd) to analyze. Open the terminal in Kali Linux.

### Step 2:
Use Sleuth Kit tools like mmls, fsstat, and fls to examine the partition layout, file system details, and file listing.

### Step 3:
Interpret the output of the tools to understand the disk structure, including partitions, sectors, and files.

## PROGRAM:
Sleuth Kit Disk Analysis Commands

 Option 1: Create a Sample Disk Image (for Testing)

Let’s create a 10MB blank disk image and simulate file system activity:

```bash
cd ~/Downloads

# Step 1: Create an empty disk image
dd if=/dev/zero of=disk.dd bs=1M count=10

# Step 2: Format it with a file system (like FAT32)
mkfs.vfat disk.dd
```

## OUTPUT:

<img width="722" height="142" alt="Screenshot 2025-09-13 133914" src="https://github.com/user-attachments/assets/49fbb8d4-4765-41af-af7b-e210a43a7919" />


### Create Disk
<img width="551" height="152" alt="Screenshot 2025-09-13 133922" src="https://github.com/user-attachments/assets/40487cc5-cc90-481c-a3a0-4d83db54e06c" />


### mmls 
```bash
mmls disk.dd
```
### fls
```bash
fls -f fat -o 0 disk.dd
```

<img width="460" height="118" alt="Screenshot 2025-09-13 133928" src="https://github.com/user-attachments/assets/d3df4022-fc15-43ac-8f75-a5d9d66bf4b7" />

<img width="637" height="481" alt="Screenshot 2025-09-13 133653" src="https://github.com/user-attachments/assets/f958f444-0b7d-42cb-9cc3-3e52d8a917b0" />

## RESULT:
The analysis was performed successfully using Sleuth Kit, and the disk structure was understood in detail.
