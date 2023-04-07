***********************************************************************************
HOW TO TRANSFER FILES FROM EC2 INSTANCE/SERVER TO LOCAL HOST/CLIENT AND VICE VERSE
***********************************************************************************
What is scp?
scp (secure copy) SCP is a widely used tool in the Linux community for securely transferring files between systems, especially in server and network administration scenarios. It is a command-line utility, which means it can be automated and scripted for more efficient file transfers.SCP uses the SSH (Secure Shell) protocol to authenticate and encrypt data during transfer, making it a secure alternative to other file transfer protocols like FTP.

***********************************************************************************
COPYING FROM SERVER TO LOCAL MACHINE
***********************************************************************************
To copy from ec2 instance to local, you can use the below command. You will be running this command on the local machine command line.

	scp -i <pem file> ec2-user@<ip_address>:<file_to_copy_from_instance> <destination_in_local>
  Example : scp -i kpair.pem ubuntu@13.233.85.7:/home/ubuntu/filefromsserver.html . (Here " . " indicates to copy the file in my current directory)

***********************************************************************************
COPYING FROM LOCAL MACHINE TO SERVER
***********************************************************************************
To copy from local to ec2 instance, you can use the below command. You will be running this command on the local machine command line.

	scp -i <pem file> <file_to_copy_from_local> ec2-user@<ip_address>:<location_in_the_instance>
  Example : scp -i kpair.pem demofile.html ubuntu@13.233.85.7:/home/ubuntu


