*File system analysis with autopsy* 

**Name:** **Alaoui Belghiti Hanaa** 

First thing I’ll do is install autopsy and put the disk image into it in kali: 

![](Aspose.Words.2f1f1d51-ed19-4d8c-8e25-f0138001f1c4.001.jpeg)

Choosing the image I’m working on: 

![](Aspose.Words.2f1f1d51-ed19-4d8c-8e25-f0138001f1c4.002.png)

Analysing It:  

` `![](Aspose.Words.2f1f1d51-ed19-4d8c-8e25-f0138001f1c4.003.jpeg)![](Aspose.Words.2f1f1d51-ed19-4d8c-8e25-f0138001f1c4.004.png)

1. **What is the type and model of the device?** 

In order to determine the type and model of the device I’ll try looking for keywords that include “device” “type” etc. 

Here is my first try:

![](Aspose.Words.2f1f1d51-ed19-4d8c-8e25-f0138001f1c4.005.jpeg)

Result : 

![](Aspose.Words.2f1f1d51-ed19-4d8c-8e25-f0138001f1c4.006.jpeg)

Clicking on it: 

![](Aspose.Words.2f1f1d51-ed19-4d8c-8e25-f0138001f1c4.007.jpeg)

As you can see above, I found the info, therefore: 



|**Device name** |**manufacturer** |**Model name** |
| - | - | - |
|**U8833** |HUAWEI |Ascend Y300 |

2. **What is the Mac address of the ethernet interface?** 

I switched to autopsy on windows for more convenience. 

In order to detect the mac address of the internet interface, first I tried looking for keywords such as “mac” “interface” “Ethernet” etc, didn’t find much info, so I  searched for the keyword” Lan” and this is the result: 

![](Aspose.Words.2f1f1d51-ed19-4d8c-8e25-f0138001f1c4.008.png)

![](Aspose.Words.2f1f1d51-ed19-4d8c-8e25-f0138001f1c4.009.png)

As you can see, I found multiple files that contains “Lan” keyword but I checked the unallocated one first: 

![](Aspose.Words.2f1f1d51-ed19-4d8c-8e25-f0138001f1c4.010.png)

Thus: 



|**interface** |**Mac address** |
| - | - |
|**Eth0** |A4:99:47:3A:6D:C3 |

3. **List 3 applications that were installed on the device:**

In order to do so I looked up the extension .apk

![](Aspose.Words.2f1f1d51-ed19-4d8c-8e25-f0138001f1c4.011.png)

Result : 

![](Aspose.Words.2f1f1d51-ed19-4d8c-8e25-f0138001f1c4.012.png)

Therefore some three applications that were found on the device would be: 

- Browser.apk 
- Calculator.apk 
- Contacts.apk 
4. **Find the SSID network names and passwords for all the networks which the device ever connected to:**

Looked up the word SSID and read the file and this was the result: 

![](Aspose.Words.2f1f1d51-ed19-4d8c-8e25-f0138001f1c4.013.png)

5. **Find the SSID and the password of the WIFI hotspot of the device:** 

I looked for the host file since that’s where network info is stored, and looked for SSID, and also “wpa” and this is the result:

![](Aspose.Words.2f1f1d51-ed19-4d8c-8e25-f0138001f1c4.014.png)

6. **When was the contact Ivan BBB called and for how long did the call last?** 

Looked up the name of the contact:

![](Aspose.Words.2f1f1d51-ed19-4d8c-8e25-f0138001f1c4.015.jpeg)

As you can see the duration was 25 and the date is as follows: 

![](Aspose.Words.2f1f1d51-ed19-4d8c-8e25-f0138001f1c4.016.png)

![](Aspose.Words.2f1f1d51-ed19-4d8c-8e25-f0138001f1c4.017.png)

7. **Which movie did the user of the device search twice for on google?** 

The film is “American history x” 

![](Aspose.Words.2f1f1d51-ed19-4d8c-8e25-f0138001f1c4.018.png)

**VIII.  In what football match the photo inside the DCIM folder was taken?** 

As for this task, I will need to correct the wrong value from 04 to 02 to restore the corrupted media:

![](Aspose.Words.2f1f1d51-ed19-4d8c-8e25-f0138001f1c4.019.png)

After fixing it, the timeline shows this: 

![](Aspose.Words.2f1f1d51-ed19-4d8c-8e25-f0138001f1c4.020.jpeg)

I’ll navigate to the “dcim” folder 

![](Aspose.Words.2f1f1d51-ed19-4d8c-8e25-f0138001f1c4.021.jpeg)

This is the image I found 

![](Aspose.Words.2f1f1d51-ed19-4d8c-8e25-f0138001f1c4.022.png)

Examining the EXIF metadata, I found no information regarding the location, no GPS coordinates, I also tried exiftool on kali Linux, but got same result. 

However, I found this picture on the device: 

![](Aspose.Words.2f1f1d51-ed19-4d8c-8e25-f0138001f1c4.023.jpeg)

Which indicates the football team name is west ham united, and since they’re on same device I’m assuming the picture was taken in London. 
