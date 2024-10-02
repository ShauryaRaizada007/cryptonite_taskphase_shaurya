##The Root:        
The flag will be captured by invoking the "pwn" program using its absolute path.     
command- /pwn   
flag- pwn.college{YyIoYg9yIHnfCGZLNvkZFefwjpU.dhzN5QDLxEjN0czW}   
   
##Program and absolute paths:       
Invoking "challenge" directory and "run" program in the terminal will give us the flag for this challenge.   
command- /challenge/run   
flag- pwn.college{YEG4hqeq32p10yGB2ejl6oJZ97v.dVDN1QDLxEjN0czW}   
   
##Position thy self:     
By changing directory(cd /directoryname) to "etc" directory and then invoking the "challenge" directory with "run" program will give us the flag.   
command- cd /etc      
         /challenge/run      
flag- pwn.college{IY4koKgjuk_H8NoCUWB9l8XV4eW.dZDN1QDLxEjN0czW}  
     
##Position elsewhere:     
By first invoking "/challenge/run" provides with the location of the directory i.e., /proc/301. By changing directory to /proc/301 and then invoking /challenge/run.      
command- cd /proc/301.   
         /challenge/run    
flag- pwn.college{o0ZcdkANsmmGoE_1ljryfl0mHJn.ddDN1QDLxEjN0czW}     
       
##Position yet elsewhere:       
This challenge is similar to the previous challenge. The only difference is that the directory path is longer than the previous one.     
command- cd /usr/share/zoneinfo/posix/Asia     
         /challenge/run     
flag- pwn.college{EDQsfhC72tuADNLNLHIF25BYdpN.dhDN1QDLxEjN0czW}     
      
##Implicit relative paths, from /:     
The challenge wants us to invoke using / command, so "cd /" will open the home directory and the invoking "challenge/run" would give us the flag.     
command- cd /      
          challenge/run      
flag- pwn.college{wEAuitzrmW-dvqtahTqWHADNxGE.dlDN1QDLxEjN0czW}     
       
##Explicit relative paths, from /:          
This challenge is similar to the previous one. A relative path must used with /. While invoking "/challenge/run", start the command with "." to remain in the same directory(./challenge/run).      
command- cd /      
         ./challenge/run      
flag- pwn.college{wlQyOZk4qJNio3OUr7RsEA50ZUO.dBTN1QDLxEjN0czW}        
     
##Implicit relative path:        
The program must be invoked from the challenge directory rather than the home directory like in the previous challenge. After changing directory, just using the naked command "run" would result in an error since Linux will search for programs with same name outside of the current directory as well. "./run" would search for programs in the current directory.     
command- cd /challenge      
         ./run      
flag- pwn.college{oIEXz8pid8BXyQoWGFM-fCBW1iq.dFTN1QDLxEjN0czW}      
      
##Home sweet home:        
In this challenge we will first create a file having a single character("s") as its name with the "touch" command and then invoke the file in /challenge/run using ~ prompt which repesents home/hacker in pwn.college. "~/.s" would be the argument for /challenge/run.     
command- touch s      
         /challenge/run ~/s     
flag- pwn.college{ssOcFuqpwYzK0HGALydok6_hu0B.dNzM4QDLxEjN0czW}        
       
