# Mobile CTF Challenges Version 1.0 (5 Challenges)

This is the link for the recording: https://www.youtube.com/watch?v=WUNNxhppxV8  
The link for the CTF: https://ivrodriguez.com/mobile-ctf/

After downloading the ipa file and extracting it using unzip I started to search for specific keywords like "flag". 

This is the command used: grep -r "flag-*" .

These are the matches found: 

grep: Headbook.app/Base.lproj/Main.storyboardc/BYZ-38-t0r-view-8bC-Xf-vdC.nib: binary file matches
grep: Headbook.app/Info.plist: binary file matches
grep: Headbook.app/Headbook: binary file matches
grep: Headbook.app/Assets.car: binary file matches

Using the tool strings on the BYZ-38-t0r-view-8bC-Xf-vdC.nib file I've found the first flag: 
flag-5932744F-4810-4A6C-BD8F-66FF3E115ED6

Using the tool strings once again I've found the second flag in the Info.plist binary: 
flag-EC840814-CEBA-4731-8620-CB991D850B14

The third and fourth flag I found was in the Headbook binary file also using the strings tool: 
flag-9861DA53-C08C-47C4-84D6-B48463AB738A
flag-BD570736-D304-400A-A6B7-F61B02173428

For the fifth flag I started to use the strings tool on the Assets.car binary and found what it seems to be an image named flag@ex.png. At this point I started to search online 
for tools that I can use to get the image and found a tool named acextract. This is the repo: https://github.com/iHTCboy/acextract

I've followed the steps for the installation and used this command to get the image: ./acextract -i ~/Assests.car -o .

Finally, I could see the image that contained the flag: 
flag-2F110A91-4BAC-4A18-A680-A6C2987CC2C4
