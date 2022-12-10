# CTFRoom!
## @Author : M3tr1c_r00t
## _**TP_LINK!**_

![instructions](https://user-images.githubusercontent.com/99975622/206875571-c0610a53-697a-4f66-a593-d702c72b6900.PNG)
To start of the challenge, lets download the bin file that were given...
<br>
<br>
After running the ** _file_** command on the file after unzipping, we can see that the bin file is further compressed..
<br>
<br>
On running the __**binwalk**__ command on the file, we can see that it's indeed compressed..
<br>
Well, we can decompress this bin file using binwalk...
<br>
![Screenshot_2022-12-10_00_38_09](https://user-images.githubusercontent.com/99975622/206877454-bf3100a2-72f2-4de9-bac9-1b49c10ea48f.png)
On moving into the extracted directory, we find some system files from the router's firmware's system...
<br>
![Screenshot_2022-12-10_00_38_20](https://user-images.githubusercontent.com/99975622/206877508-d62716c8-d502-4749-b7a9-341bfce6b622.png)

After looking arround the directories, we find some creds in the etc directory....
<br>Also with reference from some site, you can find saved passwords from a connected network(TP_Link based networks...) from the command line via the /etc directory of the system's files....
```
https://ostechnix.com/find-wifi-password-of-connected-networks-in-linux/
```
![Screenshot_2022-12-10_00_40_49](https://user-images.githubusercontent.com/99975622/206877627-01b562c6-0f2f-4023-97ab-03c0acf417ad.png)

You can also get a clearer view on the tp-links firmware's system on the following link:
```
https://thunderysteak.github.io/tl-wa901nd-basic-re
```

![Screenshot_2022-12-10_00_40_43](https://user-images.githubusercontent.com/99975622/206877574-d4da5c36-c351-4bbe-ac19-933343ac87ef.png)

And we can see a file named _**passwd.bak**_
We find some hashed passwords and with the admin on being on question we can try to crack it using John_The_Ripper...
![Screenshot_2022-12-10_00_37_11](https://user-images.githubusercontent.com/99975622/206877660-0fd2159b-b496-4f23-a09d-3b760023a009.png)
And boom!
we've got our flag...
![Screenshot_2022-12-10_00_36_14](https://user-images.githubusercontent.com/99975622/206877864-7ea6c29f-b699-4f27-8c97-a4961fdf4c1e.png)

