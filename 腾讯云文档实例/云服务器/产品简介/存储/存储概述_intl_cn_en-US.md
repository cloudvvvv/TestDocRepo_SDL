Tencent Cloud delivers flexible, cost-effective, and easy-to-use data storage for cloud server instances. Different storage devices offer different performance and price points for different usage scenarios.
## Classification of storage devices
Storage devices can be divided into the following dimensions, depending on the division of the device:
<table class="cbcategory">
        <TBODY>
		<tr>
            <th style="width: 5%;">Dimensional </TH>
            <th style="width: 5%;" > Classification </TH>
            <th style="width: 20%; > Description</TH>
        </tr>
       
        <tr>
            <td rowspan="2">Storage Media</td>
            <td>Normal hard drive</td>
            <td> storage media is a mechanical hard drive. The features are lower price and better read and write speed. </td>
        </tr>
				<tr>
				    <td>SSD hard drive</td>
					<td> Storage media is available with Solid State Drives (SSD). Featuring exceptional IOPS, read/write speeds, up to 20x IOPS and 16x throughput compared to typical hard drives. More expensive than a regular hard drive. </td>
						
			    <tr>
            		<td rowspan="2">Usage Scenarios</td>
            		<td>System Tray</td>
            		<td> A collection of systems used to store control, schedule the operation of cloud servers using mirrors. </td>
        </tr>
				<tr>
				    <TD> Data Sheet</TD>
						<td> is used to store all user data. </td>
						
						<tr>
						<td rowspan="3">Schema mode</td>
            <td>Cloud Hard Drive</td>
            <td> Cloud hard drive is a flexible, highly available, reliable, low-cost, customizable network block device that can be used as a standalone, scalable hard drive for cloud servers. It provides block-level data storage with a three-copy distributed mechanism that provides data reliability assurance for CVM. <br><font style="font-weight:bold">Cloud servers with cloud hard drives can be tuned for hardware, disk and networking</font><br>
						</td>
        </tr>
				<tr>
				    <TD>Local Site</TD>
						<td> Local storage from the physical machine on which the CVM instance resides is a storage area divided from the physical machine on which the CVM instance resides. Data access can achieve lower latency, but there is a risk of data single points of failure.<br>
						<font style="font-weight:bold">Choosing a cloud server on this site does not support hardware upgrades (CPU, memory, disk), only bandwidth upgrades. </font>
						</td>
				<tr>
				    <td>Object Storage</td>
						<td> Object Storage is a data storage device located on the Internet that enables retrieval of data from a cloud server instance or anywhere on the Internet, thereby reducing storage costs. Not suitable for storage media in low latency, high IO scenarios.
						</td>
				</TBODY></TABLE>

## Block storage device mapping

Each instance has a system disk to guarantee basic operational data, and more data disks can be mounted to the instance. Instances use block-storage device mapping (device-mapping) to map these storage devices to locations they can recognize.
Block storage is a block-by-byte storage device that supports random access. Tencent Cloud supports two types of block storage devices: Local site and cloud hard drives.
! [](https://mc.qcloudimg.com/static/img/7e8715ce6bba831c61d0cc807bec8ce9/device-mapping.png)
This figure shows how CBS maps block storage devices to the cloud server: ` /dev/vda`  to the system disk and two data disks to '/dev/vdb' and '/dev/vdc' respectively.
A cloud server instance automatically creates block storage mappings for local and cloud hard disks mounted to it.

