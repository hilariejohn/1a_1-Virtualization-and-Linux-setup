# 1a-1 Virtualization and Linux setup

- What are the advantages of using virtual machines for testing and development?

Using virtual machines for testing and development makes it easy to experiment with new software without breaking the main computer. If something goes wrong or a file gets corrupted inside the VM, the host system stays completely safe. The snapshot feature is really useful because it lets you save a working state of the system and restore it instantly if a command or program breaks everything. VMs also let you run different operating systems at the same time on one laptop, which makes testing software across platforms fast and convenient.

- What challenges did you face during installation or network setup?
  
During installation, I had to make sure hardware virtualization (VT-x/AMD-V) was turned on in my BIOS settings, along with enabling the Windows feature for WSL. Managing RAM and CPU usage was also tricky because WSL 2 can easily swallow up a lot of memory if you don't limit it with a .wslconfig file. The network setup took some trial and error, too—since WSL 2 runs on its own internal IP address, getting local servers to talk to Windows required figuring out port forwarding or network settings. Lastly, getting used to file permissions and working between the Windows folder paths and Linux terminal took a bit of practice.

- What are the differences between NAT and Bridged networking in VirtualBox?

The main difference comes down to how the virtual machine connects to the internet and local network. NAT (Network Address Translation) puts the VM behind the host computer's IP address. It gets an internal private IP, which lets the VM browse the internet while keeping it hidden and blocked from other devices on the physical network. On the other hand, Bridged Networking connects the VM directly to your home or lab router. The VM gets its own IP address on the local network just like a separate physical device, making it great for running local servers or testing connection tools.

- What did you learn about Linux distributions (distros) from your reading?
  
I learned how different Linux distributions handle software and system administration. Distros like Ubuntu use apt and .deb files for installing programs, while other distros use their own package managers. I also learned how important official software repositories and Linux file permissions are for system security. While using the desktop GUI is easy for everyday tasks, learning terminal commands showed me that the CLI is much faster and gives you way more direct control over the operating system.

