**ZFS Features** :
1. Pooled Storage
1. Copy On Write
1. Snapshots
1. Data Integrity
1. Automatic Repair
1. Suport for Raid and raid-Z
1. 128-bit Filesystem 
  (16 exabyte max filesize
   256 quadrillion zebibytes max fileststem size)

![image](https://user-images.githubusercontent.com/88557305/200140299-1109f2fb-b4bd-4060-a79f-f4f9c5cc520b.png)

Pooled storage

Pooled storage is basically a ZFS pool that is a collection of one or more vdevs that are virtual devices storing the data. The ZFS pool, also called Zpool, serves as the highest data container in the whole ZFS system. The Zpool is used to create one or more file systems (datasets) or block devices (volumes). These file systems and block devices share the remaining pool’s space. Partitioning and formatting operations will be conducted by the ZFS system.
Copy-on-write

Copy-on-write can be explained as follows. On most file systems, the data is lost forever once it is overwritten. On ZFS, on the other hand, the new information is written to a different block. The file systems’ metadata is then updated to the point of the new information once the write is complete. This results in preserving the old data in case of a system crash or other harmful event.
Snapshots

The snapshot is a read-only copy of the file system created during a particular point in time. It is possible to make snapshots of entire datasets or pools. The snapshot includes the original system version of the file system together with any changes made once the snapshot has been taken. In simple terms, a differential read-only copy is being created while creating a snapshot. You are able to revert the changes by performing a rollback operation of the snapshot. Bear in mind that you will lose all changes since the snapshot was taken. Read an article about how do snapshots really work>>
Data integrity

Data integrity can be elaborated in the following way. While writing data, a checksum is calculated and written together with it. Later on, when the data is read, the checksum is calculated once more. In case the checksums of the written and read data do not match, a data error is detected. An attempt to correct the error automatically will be then made by the system.
RAID-Z

RAID-Z is an implementation of a modified RAID-5. On ZFS, it is capable of overcoming the write hole error detected in original RAID-5. The basic level of RAID-Z, that is, RAID-Z1 requires three disks to work: two disks for storage and one for parity. In turn, RAID-Z2 has to have two disks for storage and two for parity. RAID-Z3 has to have minimum two storage drives and three drives for parity. Note that drives have to be placed in multiples of two when they are added to the RAID-Z pools.
Closing notes

Taking everything into consideration, the ZFS is undoubtedly a file system offering a vast array of possibilities. Not only it is possible to manage data in an efficient and innovative way but also in case of a harmful event, you are able to restore your data without any interruptions to your work. Additionally, in case of a failure, the whole system can be easily restored by using the snapshot capability and reverting the system to a particular point in time.


![image](https://user-images.githubusercontent.com/88557305/200137072-49ae8113-1b74-4e33-958d-1a4ce1094d94.png)
![image](https://user-images.githubusercontent.com/88557305/200137076-c8e68ac6-0126-442a-ad32-87a6549a2038.png)
