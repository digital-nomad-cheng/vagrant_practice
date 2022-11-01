1. virtualbox is the provider for vagrant
2. command
   + check version: vagrant -v

3. vagrant file all the settings go
   + config.vm.box: operating system
   + config.vm.provider - virtualbox
   + config.vm.network - how your host sees your box
   + config.vm.synced_folder - how you access files from your computer
   + config.vm.provision - what we want setup

4. config X11 forwarding on vagrant virtual machine. 
   X11 forwarding is crucial when you want to lancuh an application/utility on a virtual machine with GUI, but utilizing the GUI interface of your host machine. The vagrant instance running will use X11 to talk to the display system of the host machine.
  + install xauth on vagrant instance: `sudo apt install xauth`
  + config vagrantfile to forward using X11
    ```bash
      config.ssh.forward_agent = true
      config.ssh.forward_x11 = true 
    ```
 
## Resources
1. vagrant crash course: https://www.youtube.com/watch?v=vBreXjkizgo
