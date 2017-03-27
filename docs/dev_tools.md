---
layout: default
category: Services
title: Dev Tools
---

<meta http-equiv="Content-Type" content="text/html; charset=UTF-8"></meta></style>

#### Applicable Plans - All Cloud Hosting Plans

# Installing the CentOS Development Tools (gcc, flex, autoconf, etc)

### Overview

If you are going to do any software development on your Virtual Server, or manually install software or applications that need to be compiled in order to work, you will need to install the CentOS Development Tools. These tools are installed from the command line of the VS using yum. 

The "Development tools" are a ***yum group***, which is a predefined bundle of software that can be installed at once, instead of having to install each application separately. 

The Development tools will allow you to build and compile software from source code. Tools for building RPMs are also included, as well as source code management tools like Git, SVN, and CVS. 

<a href="#installing-the-development-tools">Installing the Development Tools</a>  
&nbsp; &nbsp; <a href="#development-tools---included-applications">Development Tools - included applications</a>  
&nbsp; &nbsp; <a href="#installing-the-development-tools-using-yum">Installing the Development tools using yum</a>  

---

## Installing the Development Tools 

To install the CentOS Development tools, you will need to be able to connect to your Virtual Server using SSH, and work as the *root* user. Information on connecting to your VS using SSH is found here - [*http://support.eapps.com/ispmgr/ssh*](http://support.eapps.com/ispmgr/ssh "SSH User Guide")

### Development Tools - included applications 

The current applications available with the CentOS Development tools yum group are: 

<p style="border:1px solid black; background-color: white; padding:5px; font-family: Courier New, Courier, monospace; color:black; width: 50%;">
<span style="font-weight: bold;">
bison <br />
byacc <br />
cscope <br />
ctags <br />
cvs <br />
diffstat <br />
doxygen <br />
flex <br />
gcc <br />
gcc-c++ <br />
gcc-gfortran <br />
gettext <br />
git <br />
indent <br />
intltool <br />
libtool <br />
patch <br />
patchutils <br />
rcs <br />
redhat-rpm-config <br />
rpm-build <br />
subversion <br />
swig <br />
systemtap <br />
</span>
</p>

There are also dependencies that will install with these tools. 

### Installing the Development tools using yum 

Before installing the Development tools, run the ***yum clean all*** command. This will clear the yum cache and force it to reread any changed configuration files. 

<table style="text-align: left; width: 90%;" border="0" cellpadding="2"
cellspacing="2">
<tbody>
<tr>
<td
style="vertical-align: top; background-color: rgb(71, 71, 71);"><span
style="font-family: Courier New,Courier,monospace; color: white;">[root@eapps-example
~]# <span style="font-weight: bold;">yum clean all</span><br>
Loaded plugins: fastestmirror, priorities, remove-with-leaves<br>
Cleaning up Everything<br>
Cleaning up list of fastest mirrors<br>
[root@eapps-example ~]# </span><br>
</td>
</tr>
</tbody>
</table>

<br />
To install the Development tools, use the ***`yum groupinstall "Development tools"`*** command. This will search the yum repositories, and install the tools from the closest repo. This creates several screens of output, which are truncated in this example. 

<table style="text-align: left; width: 90%;" border="0" cellpadding="2"
cellspacing="2">
<tbody>
<tr>
<td
style="vertical-align: top; background-color: rgb(71, 71, 71);"><span
style="font-family: Courier New,Courier,monospace; color: white;">[root@eapps-example
~]# <span style="font-weight: bold;">yum groupinstall "Development
tools"</span><br>
<br>
<span style="font-style: italic;">....Output truncated....</span><br>
<br>
Install&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 86 Package(s)<br>
Upgrade&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0 Package(s)<br>
<br>
Total download size: 77 M<br>
Installed size: 234 M<br>
Is this ok [y/N]:</span><br>
</td>
</tr>
</tbody>
</table>


You will need to confirm that you want to continue the installation. Enter a ***y*** to continue. 

How many packages will be installed depends on your template. A **LAMP** template will require fewer packages than a non-LAMP template. 

It will take anywhere from 3 to 5 minutes to install all the packages. Once everything is installed, you will see a ***Complete!*** message, and be returned to the command prompt. 

<table style="text-align: left; width: 90%;" border="0" cellpadding="2"
cellspacing="2">
<tbody>
<tr>
<td
style="vertical-align: top; background-color: rgb(71, 71, 71);"><span
style="font-family: Courier New,Courier,monospace; color: white;">Complete!<br>
[root@eapps-example ~]# </span><br>
</td>
</tr>
</tbody>
</table>

<br />
The Development tools are now installed. 

---
