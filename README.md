# CCNA-LAB-1-Basics
Enter Privledge Exec Mode  CLI: en(Enable)
How to reboot cisco router Router# Reload
Can always check out configs in confused on command to enter w/ ? command (ie Router> ?) Every level will have its own commands
To go back to exec mode Router# 
To enter global configuration the command is Router#Conf T (Configure Terminal) (Configuration that affects the device as a whole
Do #Show ip int br (Show ip interface Brief) this will check what interfaces are avaliable from global configuration mode
To configure a specific interface:
R1(config)#Interface gigabitethernet 0/0
#This will change the promp to : R1(config-if)#
to get out of this screen and go back into global configration mode:
R1(config-if)#exit
The exit command always brings you back down one level
You can ultizie arrow keys up and down to go to previous commands
You can also enter in the #end command to go all the way back down to exec mode
To view the enteire device configuration: 
R1#Show running-configuration 
You can specifiy speciic portions in the configuration with a "|"
ie R1:sh run | begin hostname (This will show you the config starting from the hostname)
another example show configuration only lines with this command:
R1#sh run | include interface
Alternativley you can do this and exclude the word interface it will show you everything the word you included:
r1#sh run | exclude interface
its always important to copy the running configuration to the startup configuration to save changes
r1#copy run start
You can also change the name of the router currently working on:
r1#hostname RouterX
Also its never a good idea to save the backup only on the device itself always copy the running config to a tftp server:
RouterX#copy run tfpt
Always reload to check the cahnges have been saved w/ Reload command 
