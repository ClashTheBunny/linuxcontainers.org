![Download icon](/static/img/containers.png)
# News
## LXD 0.8.1 release announcement<span class="text-muted">29th of April 2015</span>

Bugfix only release on top of 0.8 fixing some regressions:

 * Fix building on all architectures
 * Change the go-protobuf repository URL

### Downloads
The release tarballs can be found on our [download page](/lxd/downloads).


## LXD 0.8 release announcement<span class="text-muted">28th of April 2015</span>

The major changes for this release are:

 * Fixed uid/gid in lxc file push
 * Respect PROXY environment variables
 * Fix database locking issues
 * Add more debugging options
 * Various fixes to ephemeral containers
 * Fix creating a new container from a snapshot
 * When available, use btrfs subvolumes for faster container creation

### Downloads
The release tarballs can be found on our [download page](/lxd/downloads).


## LXD 0.7 release announcement<span class="text-muted">14th of April 2015</span>

The major changes for this release are:

 * Containers can now be started from a private image
 * Ephemeral containers are supported
 * Improved debugging
 * Some documentation update
 * A few more minor fixes

Please note that it's still early in the LXD development and that current LXD isn't intended  
for production use and comes with no support statement from upstream.  
(reported bugs and patches will be included in the next release)

### Downloads
The release tarballs can be found on our [download page](/lxd/downloads).


## LXD 0.6 release announcement<span class="text-muted">7th of April 2015</span>

The major changes for this release are:

 * Added a vagrant configuration file
 * The container's MAC address is now persistent
 * Variety of fixes regarding remote servers handling
 * Recursive query support (massive speed improvement for image servers)
 * TLS now configured to only support strong ciphers
 * Support setting aliases at image import time
 * Improved test coverage
 * Improved error messages on the client
 * Fix privileged containers handling
 * LXD can now be built on powerpc
 * And a lot more bugfixes and tweaks

Please note that it's still early in the LXD development and that current LXD isn't intended  
for production use and comes with no support statement from upstream.  
(reported bugs and patches will be included in the next release)

### Downloads
The release tarballs can be found on our [download page](/lxd/downloads).


## LXD 0.5 release announcement<span class="text-muted">24th of March 2015</span>

The major changes for this release are:

 * IPv6 support for remote servers
 * Check if the remote server happens to have a certificate which is trusted by the system
 * Implemented "lxc image copy"
 * Improved remote handling (default configuration, support for https:// and unix:// and a bunch of convenient aliases)
 * API consistency for key/value storage (always exported as dictionaries)
 * Remote images can now be started by their long or short hash
 * Remote image properties are now properly mirrored in the local cache
 * A lot of database locking issues have been resolved

Please note that it's still early in the LXD development and that current LXD isn't intended  
for production use and comes with no support statement from upstream.  
(reported bugs and patches will be included in the next release)

At this point, most core LXD features are present but many of the  
particular options aren't implemented yet (don't match our  
specifications), we expect to make great progress in supporting all of  
the expected options over the next couple of releases.

### Downloads
The release tarballs can be found on our [download page](/lxd/downloads).


## LXD 0.4 release announcement<span class="text-muted">17th of March 2015</span>

The major changes for this release are:

 * Support for starting a container from a remote image
 * Support for copying/moving containers between hosts
 * Improved command line (listing, aliases, profiles, partial hashes, ...)
 * Improved error logging
 * API fixes to more closely match the spec
 * A lot of bugfixes

Please note that it's still early in the LXD development and that current LXD isn't intended  
for production use and comes with no support statement from upstream.  
(reported bugs and patches will be included in the next release)

At this point, most core LXD features are present but many of the  
particular options aren't implemented yet (don't match our  
specifications), we expect to make great progress in supporting all of  
the expected options over the next couple of releases.

### Downloads
The release tarballs can be found on our [download page](/lxd/downloads).


## LXD 0.3 release announcement<span class="text-muted">10th of March 2015</span>

The major changes for this release are:

 * lxd:
    * Reworked exec, now with separate interactive and non-interactive modes and proper support for escape sequences.
    * Improved image handling, now supporting more compression algorithms and support for image export.
    * Initial support of live migration (requires particular container configuration)
    * Initial support of container configuration and profiles
        * Support for disks and network interfaces
        * Support for creating/deleting/assigining profiles
    * Introduce a "default" profile which is applied to all new containers unless otherwise specified.
 * lxc:
    * Improved user experience for the various "list" commands
    * Improved info command, now showing PID and IP addresses
    * Implement the image info command, shows all image properties and aliases.
    * Early (partial) french translation as an example translation of LXD.
    * Support of the "edit" command for images and profiles.
 * lxd-images:
    * Now supports creating a minimal busybox image.
    * Vastly improved image imports from images.linuxcontainers.org by no longer requiring repacking.
    * Now working with python3.2
 * Testsuite:
    * Added tests for container configuration, profiles, devices, migration, exec and database.
    * Now running using a minimal busybox image, making it run in just a few seconds.
 * Many bugfixes

Please note that it's still early in the LXD development and that current LXD isn't intended  
for production use and comes with no support statement from upstream.  
(reported bugs and patches will be included in the next release)

At this point, most core LXD features are present but many of the  
particular options aren't implemented yet (don't match our  
specifications), we expect to make great progress in supporting all of  
the expected options over the next couple of releases.

### Downloads
The release tarballs can be found on our [download page](/lxd/downloads).


## LXD 0.2 release announcement<span class="text-muted">27th of February 2015</span>

The major changes for this release are:

 * Initial version of the built-in image store
    * All containers must now be created from images
    * Images can be imported into LXD by using the provided "lxd-images" tool
    * Image aliases can be setup to make it easier to find your images
 * Database backend (all LXD data is now stored in a SQLite database)
 * Early stage of container configuration (partial API only)
 * Support for building for many architectures through gcc-go (not all dependencies are compatible)
 * Reworked exec mechanism
 * A lot of bugfixes

Please note that it's still early in the LXD development and that current LXD isn't intended  
for production use and comes with no support statement from upstream.  
(reported bugs and patches will be included in the next release)

We are still busy working on container migration, proper container configuration and a stable REST API.

### Downloads
The release tarballs can be found on our [download page](/lxd/downloads).


## LXD 0.1 release announcement<span class="text-muted">13th of February 2015</span>
This is the initial LXD release.

With this first release of LXD, it is possible to:

 * List containers
 * create, destroy, start, stop and execute commands into an Ubuntu 14.04 LTS amd64 container
 * Transfer files in and out of containers
 * Management of multiple LXD hosts through the lxc command line tool
 * Experiment with the LXD [REST API](/lxd/rest-api)

Support for other container images, container migration, container configuration and profiles  
and a stable REST API will be coming in the next few releases.

This release is our first development snapshot and isn't intended for production use  
and comes with no support statement from upstream. 
(reported bugs and patches will be included in the next release)

### Downloads
The release tarballs can be found on our [download page](/lxd/downloads).
