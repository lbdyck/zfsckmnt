# ZFSMNTCK - Check for Mounted Filesystems Not in PARMLIB
This little tool will identify all mounted filesystems in the z/OS
UNIX System Services environment that are not defined in any
BPXPRMxx members of the System PARMLIBs.

## Usage
To use first copy the code into a PDS within a SYSEXEC or SYSPROC
allocation and then enter:

     `%zfsmntck`

