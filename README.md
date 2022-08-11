-use pulseaudio

-add "options snd-hda-intel model=asus-zenbook" 
 to /etc/modprobe.d/alsa-base.conf
 (create the file, if it doesn't exist)
 
-audio should work after a restart, but you cant control the volume

-add  
"[Element Master]  
  switch = mute  
  volume = ignore"  
 to /usr/share/pulseaudio/alsa-mixer/paths/analog-output.conf.common
 (in front of the [Element PCM] block)
 
 -restart pulseaudio
