Notes on Using the Shell Technology Preview Update with
Windows NT Version 3.51

Using Write to View this Document
If you enlarge the Write window to its maximum size, this document will be easier to read. To do so, click the
Maximize button in the upper-right corner of the window, or open the Control menu in the upper-left corner of the
Write window (press ALT+SPACEBAR), and then choose the Maximize command.

To print the document, choose Print from the File menu. For Help on using Write, press F1. To read other online
documents, choose Open from the File menu.


Details
The Shell Technology Preview Update is being provided to Microsoft® Developer Network (MSDN) Level 2
subscribers, and is available on CompuServe® and the Internet.  If you would like further information about MSDN
or wish to subscribe, please call (800) 759-5474.

This update includes a few important bug fixes to problems reported using Office for Windows® 95, NetScape, and
MFC applications on the original Shell Technology Preview.  This release is intended to enable software developers
and vendors to test their applications on both Windows 95 and Windows NT™ version 3.51 platforms.  This release
includes the Windows 95-compatible user interface and shell APIs, but does not include additional applets and other
UI changes such as the fonts and printers folders.  This user interface will be integrated into the base Windows NT
product and made available in a future release of Windows NT.  The date of this release is to be determined.


Reporting Problems
The Shell Technology Preview Update has not been fully tested and should not be deployed in production
environments.  There is currently no official Microsoft Product Support Services support available for using the Shell
Technology Preview on Windows NT version 3.51.  If you wish to join other customers who are using and
exchanging feedback on the Shell Technology Preview, Section 15 of the MSDR forum on CompuServe has been
created for this type of member-to-member communication.

If you wish to report a problem, please do so through our CompuServe or Internet services as follows.  These are not
support locations, but may be used to submit problems you encounter, using PROBREP.TXT.

CompuServe: Upload PROBREP.TXT to the WINNT forum, Library 3.

FTP: Connect to ftp.microsoft.com

	ftp>cd e:
	ftp>cd incoming/bussys/winnt/probrep
	ftp>bin
	ftp>put probrep.txt

Internet mail: send to ntbug@microsoft.com


Installation Notes
If you have read this statement and are in agreement with the terms and conditions of the license agreement
(STPULIC.WRI) and still want to install the Shell Technology Preview Update, please read the instructions below
carefully.  By installing this release, you agree to the terms and conditions of the license agreement.

Installing This Update on a Previous Release
If you installed a previous release of the Shell Technology Preview and you wish to install the Shell Technology
Preview Update, you must first remove the installed Shell Technology Preview before installing the update:

1.	Locate the original installation media for the installed Shell Technology Preview.
2.	Change to the directory that corresponds to your hardware platform (for example, \NEWSHELL\I386).
3.	Run SHUPDATE.CMD /U directly from this location.  This command will remove the Shell Technology Preview
and reinstall Program Manager from the previous Windows NT version 3.51 configuration.
4.	You may now install the Shell Technology Preview Update outlined in "Performing a Clean Installation" below.

Installing Service Pack Updates
If you utilize the Shell Technology Preview or Update, and you wish to install the latest fixes available for Windows
NT, you may obtain the latest Windows NT Workstation and Server version 3.51 Service Pack release from:

  	Microsoft Sales Information Center at (800) 426-9400
	Microsoft's anonymous FTP server:
		ftp: \\ftp.microsoft.com\bussys\winnt\winnt-public\fixes\nt351\ussp1
	Microsoft Software Library, type GO ! MSL
	Microsoft Download Area, type GO ! WINNTDL

Before installing the Service Pack release to update your computer, you must first remove the Shell Technology
Preview.  When updating the base operating system, the Service Pack will not install if the Shell Technology Preview
is running.  To remove the Shell Technology Preview, follow the instructions above under the heading "Installing
This Update on a Previous Release."  Once the Shell has been removed and the Service Pack has been successfully
installed, you may reinstall the Shell Technology Preview Update.

Performing a Clean Installation
First, ensure that any previous installation of the Shell Technology Preview has been removed, as outlined above.
Apply the Shell Technology Preview Update by running SHUPDATE.CMD from one of the following locations
corresponding to the hardware platform to which you are installing:
	
	\NEWSHELL\ALPHA
	\NEWSHELL\I386
	\NEWSHELL\MIPS
	\NEWSHELL\PPC

If you are running the Windows NT version 3.51 checked build, you should run SHUPDATE.CMD from the
corresponding \CHECKED\NEWSHELL directories of the Windows NT version 3.51 CD-ROM provided to MSDN
Level 2 subscribers.

If you wish to remove the Shell Technology Preview Update, run SHUPDATE.CMD /U.  This command will remove
the Shell Technology Preview Update and reinstall Program Manager from the previous Windows NT 3.51
configuration.


Symbol Files	
To aid developers with debugging, symbol files for the Shell Technology Preview Update binaries are provided in the
symbols subdirectory found under the \newshell and/or \checked\newshell directories of the Windows NT 3.51 CD-
ROM that is provided with MSDN Level 2.

To install the symbol files, simply xcopy the symbols tree for the appropriate hardware platform to the symbols tree
on the host debugger.  For example, if a machine is set up to debug an Alpha AXP™ machine running the free build
and the symbol path is d:\debug\symbols, the command to copy over the Shell Technology Preview Update symbol
files would be:

	xcopy /i cd:\newshell\symbols\alpha d:\debug\symbols

This command will copy the symbols to their correct location on the debugger machine.

