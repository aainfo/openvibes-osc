openvibes-osc
=============

openvibe python box to send data in OSC(Open Sound Control)

This script send OSC packet from openvibes signal.                                                                                             
It work with Linux and Windows version of openvibes.

This script allow Openvibes to communicate with software like PureData, Max/MSP

See:
Openvibes : http://openvibe.inria.fr (Software for Brain Computer Interfaces and Real Time Neurosciences)
PureData: http://puredata.info/
Max/MSP: http://cycling74.com/products/max/

Dep:                                                                                                                      

1.Numpy

Install numpy http://sourceforge.net/projects/numpy/files/


2.simpleOSC

You need to install simpleOSC, modules can be found here:                                                                                 
 http://opensoundcontrol.org/implementation/python-simple-osc                                                                                  
 http://www.ixi-audio.net/content/body_backyard_python.html                                                                                    
                                                                                                                                               
Install Simple OSC:                                                                                                                            
methode 1                                                                                                                                      
 pip install SimpleOSC                                                                                                                         
                                                                                                                                               
methode 2:                                                                                                                                     
 get OSC.py and simpleOSC.py and add this files to python path.                                                                                
 simply copy these files in your custome lib folder ,                                                                                          
 mkdir -p ~/script/openvibes-python/lib                                                                                                        
 cp OSC.py simpleOSC.py /home/user/script/openvibes-python/lib/                                                                                
 and add some lines to the beginning of the python script:                                                                                     
                                                                                                                                               
 from sys import path                                                                                                                          
 path.append("/home/user/script/openvibes-python/lib")                                                                                         
                                                                                                                                               
methode 3:                                                                                                                                     
 copy OSC.py and simpleOSC.py in your python module directory                                                                                  
 cp OSC.py simpleOSC.py /usr/lib/python2.7/                                                                                                    
                                                                                                                                               
How to use:                                                                                                                                    
 1-create python scripting box                                                                                                                 
   Scripting -> Python scripting                                                                                                               
                                                                                                                                               
 2-right click on the box then click "configure box"                                                                                           
   set the path of the script in script section                                                                                                
                                                                                                                           3-right click on the box and click on settings -> new                                                                                         
   set name IP, the type is String                                                                                                             
   default value is what you want                                                                                                              
   ex: 127.0.0.1                                                                                                                               
                                                                                                                                               
 4-right click on the box and click on settings -> new                                                                                         
   set name PORT, the type is Integer                                                                                                          
   default value is what you want                                                                                                              
   ex : 5003                                                                                                                                   
                                                                                                                                               
 5-right click on the box and click on settings -> new                                                                                         
   set name TAG, the type is Sting                                                                                                             
   default value is what you want                                                                                                              
   ex : /eeg/AF1                                                                                                                               
                                                                                                                                               
 6-right click on the box then configuration                                                                                                   
   in field IP, PORT, TAG set the value to your needs.                                                                                         
                                                                                                                                               
 7-play scenario with openvibes                                                                                                                
