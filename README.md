Linux kernel
============

There are several guides for kernel developers and users. These guides can
be rendered in a number of formats, like HTML and PDF. Please read
Documentation/admin-guide/README.rst first.

In order to build the documentation, use ``make htmldocs`` or
``make pdfdocs``.  The formatted documentation can also be read online at:

    https://www.kernel.org/doc/html/latest/

There are various text files in the Documentation/ subdirectory,
several of them using the Restructured Text markup notation.

Please read the Documentation/process/changes.rst file, as it contains the
requirements for building and running the kernel, and information about
the problems which may result by upgrading your kernel.

## Installation:
1. Select a branch other than master
2. Clone the repo

`git clone https://github.com/Rybo713/IntelLinuxKernel.git`

3. Go into the directory 

`cd /IntelLinuxKernel`

4. Compile the kernel

`sudo make -j$(nproc --all)` Note: `(nproc -all)` uses all your cpu cores to compile the kernel

5. Compile the rest of the kernel

`sudo make modules_install`

6. Install the kernel into your system
`sudo make install`

7. Reboot your system and select version with `-ILK` at the end

8. That's it!
