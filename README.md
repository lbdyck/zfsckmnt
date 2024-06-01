# ZFSMNTCK - Check for Mounted Filesystems Not in PARMLIB
This little tool will identify all mounted filesystems in the z/OS
UNIX System Services environment that are not defined in any
BPXPRMxx members of the System PARMLIBs.

Any system symbolics in the BPXPRMxx members will be resolved
for the dataset names of the filesystems.

## Usage
To use first copy the code into a PDS within a SYSEXEC or SYSPROC
allocation and then enter:

     `%zfsmntck`

## Notes
1. This tool requires the SDSF REXX interface
2. This tool will not run under OMVS or shell
   - the rexx sysdsn function is not available
3. In a shared zfs environment only those mounted filesystem on
   the active lpar that are NOT defined in parmlib will be reported.
   * this is because the system symbolics are resolved for the
     local system making the other systems filesystems unknown.
