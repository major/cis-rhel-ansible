#Notes and caveats

These notes are valid as of the CIS Red Hat Enterprise Linux 6 benchmark version 1.3.0.

### Section 1

##### 1.1.1 - 1.1.16
Existing mounts will be modified with benchmark options.  Mount points are not created if not pre-existing.

###### 1.1.17
Skipped: Adjusting permissions across the filesystem can be destructive.

##### 1.2.{1,2,5,6}
Skipped: Some yum operations are skipped as they apply only to RHEL and not CentOS.

##### 1.4.6
Skipped: Checking for unconfined daemons should be done via cron jobs or via manual inspection

##### 1.5.{3,4}
Skipped: Adjusting bootloader configurations at a large scale on production machines could be highly destructive upon reboot.

### Section 4

##### 4.8
IPv6 is disabled so ip6tables is also disabled.

### Section 6

##### 6.4
Skipped: Restricting root access only to the system console is a bit too restrictive for most environments.

### Section 7

##### 7.1.1 - 7.1.3
Existing user password age is not modified.

### Section 8

##### 8.2
Satisfied by 8.1.

##### 8.3
Not addressing graphical desktop environments.

### Section 9

##### 9.1.1
Not a scorable item and requires human interpretation.  This is best handled by AIDE or other file integrity monitoring systems.

##### 9.1.10 - 9.1.14
This is best handled by AIDE or other file integrity monitoring systems.

##### 9.2
These items all require human intervention to resolve.  None of these will be a concern while applying CIS to a vanilla RHEL6 install.
