***Broken under current kernel***




-install and enable pulseaudio

-mask ***pipewire.service*** and ***pipewire.socket***

-add ***options snd-hda-intel model=asus-zenbook***<br>
 to /etc/modprobe.d/alsa-base.conf
 (create the file, if it doesn't exist)
 
-audio should work after a restart, but you cant control the volume

-add  
***[Element Master]<br>
switch = mute<br>
volume = ignore***<br>
(in front of the [Element PCM] block)<br>

 to /usr/share/pulseaudio/alsa-mixer/paths/analog-output.conf.common
 
 
 -restart pulseaudio
