# BlueEyes - Simplified Bluetooth Reconnaissance
**Author: ExME168**

### About BlueEyes
![image](https://user-images.githubusercontent.com/63983951/206750495-e6d3c42b-d0d3-4be3-861a-f54fbc1212b4.png)
Long story short, I had a college group project for an "Advanced and Offensive Security" course where the task was (in particular to my group) to create a wireless hacking tool.
But due to my lacking a Kali-compatible WiFi adapter and also thanks to a random suggestion by a group mate (shout out to jm55DLSU), I decided to write a tool centered around Bluetooth
as it is still a "wireless" protocol. BlueEyes is a tool that simplifies the reconnaissance of BT devices by providing one streamlined interface for gathering useful information about 
nearby BT devices such as, but not limited to: MAC address, device class, clock offset, and running services. The tool also places emphasis on education about Bluetooth technology by
providing brief descriptions of the scan results as well as a dedicated section for knowing about the basics of the protocol. I hastily made this tool in less than a week to comply with
the deadline but I really wished I started this earlier. Making this tool was an eye-opener to the complex world of Bluetooth and it got me thinking if I could maybe come back to this tool
someday for a Bluetooth-related thesis topic. More importantly, this is the first tool I've made in my cybersecurity journey. I think I'd rather choose this career than game development.
This is fun.

![image](https://user-images.githubusercontent.com/63983951/206753159-bec43bec-99dd-4a50-946f-588cbf52b0e3.png)

**Basics of Bluetooth Technology**
- To view more information about Bluetooth Technology, select '0' on BlueEyes’ main menu.

![image](https://user-images.githubusercontent.com/63983951/206753245-505ae658-2ff3-4dab-8268-055a3f638366.png)

**Check Bluetooth Service Status**
- To determine whether the BT service on Linux has been launched, you may enter '1' to check Bluetooth service status.

![image](https://user-images.githubusercontent.com/63983951/206753330-1ade12ee-678b-4f2e-bb99-9df6d4773a04.png)

**Start Bluetooth Service**
- In case you find yourself with an inactive BT service, select '2' for BlueEyes to attempt to enable the service on your behalf.

![image](https://user-images.githubusercontent.com/63983951/206753381-bd0cff64-5721-4b43-bbd4-6acb0cd263d9.png)

**Check My Bluetooth Device**
- To check for your device’s BT interface details, select '3' on the main menu. It will contain details such as the BT interface logicalname and MAC address.

![image](https://user-images.githubusercontent.com/63983951/206753428-5953d8ef-62d2-4901-a5a4-cc5c48450382.png)

**Check All Bluetooth Devices**
- To determine if a specific BT interface is up and running, select '4' on the main menu to check for it.

![image](https://user-images.githubusercontent.com/63983951/206753574-deb974e2-82c0-4d96-98f9-15c545ad6fb5.png)

**Start BlueEyes**
- To begin using the main BlueEyes features, select '5' in the main menu. Afterwards, a new menu will appear with a new set of commands as well as a target list. Each scanned BT device is assigned an ID number which should be used for target selection. Note that every command is not case-sensitive but the syntax must still be followed (the words must be in order).

  ![image](https://user-images.githubusercontent.com/63983951/206753846-f03ca951-ca08-4947-b8e9-4776a759005d.png)
  - **set target**
      - To select a target, enter this command but replace the '<id>' substring with the assigned ID of the target based on the target list.

  ![image](https://user-images.githubusercontent.com/63983951/206753983-7f299e8b-ae26-4657-a1c5-963d98a7646d.png)
  - **unset target**
    - To deselect a target, enter this command.
    
  ![image](https://user-images.githubusercontent.com/63983951/206754182-4c571bd8-8292-465b-b317-c4174af17e7a.png)
  - **show ALL**
    - To redisplay the target list, enter this command. This can be useful when the terminal becomes too congested.
    
  ![image](https://user-images.githubusercontent.com/63983951/206754331-6b64a223-dd39-448e-8322-ab2b8f137cf1.png)
  - **show TARGET**
    - To show the currently selected target, enter this command. It is recommended to run this command before starting a ping or scan.
	
  ![image](https://user-images.githubusercontent.com/63983951/206754364-b763a9f4-1ed6-480e-8a54-da4f048bced1.png)
  - **ping**
    - To ping the selected target, enter this command. You may need to enter your Kali profile password if you are not a root user.
    
  ![image](https://user-images.githubusercontent.com/63983951/206754508-05f6ab2b-0108-4a1d-9b2c-76fe918e41ce.png)
  - **scan**
    - To begin scanning the target, enter this command. This command outputs the clock offset, device class, and a list of running services of the target.

  - **scan -o <filename>**
    - To scan the target and save the results in a text file, enter this command but replace the '<filename>' substring with any filename of your choice. You do not need to append ‘.txt’ as the tool will do that for you. The text file will be saved in the same directory as airhound.py. 
  - **exit**
    - To stop using the BlueEyes feature and go back to the main menu, enter this command.
    
**Exit**
- To return to Airhound’s main menu, type in '6' to exit BlueEyes
