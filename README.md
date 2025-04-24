Analysis-of-the-Disk-Structure-using-Sleuth-Kit

AIM:
To analyze the disk structure of a given disk image using Sleuth Kit tools in Kali Linux.

DESIGN STEPS:
Step 1:
Obtain or create a disk image file (e.g., disk.dd) to analyze. Open the terminal in Kali Linux.

Step 2:
Use Sleuth Kit tools like mmls, fsstat, and fls to examine the partition layout, file system details, and file listing.

Step 3:
Interpret the output of the tools to understand the disk structure, including partitions, sectors, and files.

PROGRAM:
Sleuth Kit Disk Analysis Commands

Create a Sample Disk Image (for Testing)

Let’s create a 10MB blank disk image and simulate file system activity:
```
cd ~/Downloads

# Step 1: Create an empty disk image
dd if=/dev/zero of=disk.dd bs=1M count=10

# Step 2: Format it with a file system (like FAT32)
mkfs.vfat disk.dd
```
OUTPUT:

![436175046-5068592b-2040-4489-a36b-8a3858a59638](https://github.com/user-attachments/assets/63b6ab27-bfbc-4912-a886-523a5048e77f)

Create Disk:

![436175109-60e230b6-58e7-42d6-bd40-a7dca1728371](https://github.com/user-attachments/assets/c5fe60ba-d96f-4993-8e0a-662d291e6236)


mmls
```
mmls disk.dd
```
fls
```
fls -f fat -o 0 disk.dd
```

![436175264-ac3f0e98-0a69-430f-98ae-1e49f23371d3](https://github.com/user-attachments/assets/1d49dc55-3b87-4a5e-bbbc-9fe02dbabb9e)


![436175311-f5f43c31-e547-4bff-8aa9-37ba76137a44](https://github.com/user-attachments/assets/eb2f28c5-689e-46b1-8676-826558e642fb)



![436175354-5dc5a1ed-d685-41c8-9be9-4211d0f6548f](https://github.com/user-attachments/assets/c2cf4754-d54d-4795-847e-7e1ac8a5ccfb)


RESULT:

The analysis was performed successfully using Sleuth Kit, and the disk structure was understood in detail.
