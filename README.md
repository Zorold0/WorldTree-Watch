# WorldTree-Watch

## Loading the Project
You will need [Watch Face Studio to load this project](https://developer.samsung.com/watch-face-studio/download.html).

Once installed, open the application and select `File -> Open Project` and open `WorldTree.wfs`.

## Loading it onto your Watch with Watch Face Studio

**For the easiest directions, you can follow [this youtube tutorial starting from 1:39.](https://youtu.be/sF3us77rbdc?si=8M9ulIMDcbyEWGuQ&t=99)**

Otherwise here are instructions:

1. **Enable debug mode on your WearOS watch.**
     - On your watch, open the Settings app.
     - Scroll down and tap on "About" or "System" (depending on your watch model).
     - Look for the "Build number" and tap on it multiple times (usually 7 times) until you see a message that says "You are now a developer!" or "Developer mode has been enabled!"
     - Go back to the main Settings menu and you should now see a new option called "Developer options" or "Developer settings". Tap on it.
     - Look for the "Debugging" section and enable the "ADB debugging" option. This will allow you to connect your watch to your computer and install apps using ADB commands.
2. **Download the Android SDK Platform Tools to run `adb` commands.**
   - Download the Android SDK Platform Tools here: https://developer.android.com/tools/releases/platform-tools
   - Extract the downloaded zip file to a location on your computer where you can easily access it.

3. **Open a command prompt / terminal and navigate into the extracted folder.**

```cmd
cd path\to\extracted\platform-tools
```

4. **Wirelessly connect to your watch using ADB.**
   - Make sure your computer and watch are on the same Wi-Fi network.
   - On your watch, go to the "Developer options" or "Developer settings" menu and look for the "Wireless debugging" option. Enable it.
   - In the Wireless Debugging menu, scroll to the bottom and select "Pair new device" and note the pairing code and IP address displayed on your watch.
   - In your command prompt / terminal, run the following command to pair your watch with your computer, replacing `<pairing_code>` and `<ip_address>` with the values from your watch:
   - ```cmd
     adb pair <ip_address>:<port> <pairing_code>
     ```
   - After running the command, you should see a message confirming that the pairing was successful.
   - Once paired, go back to the Wireless Debugging menu on your watch and find the IP address and port number for the wireless debugging connection. It should be in the format `<ip_address>:<port>`. **Note that this might be a different port than the one used for pairing.**
   - In your command prompt / terminal, run the following command to connect to your watch, replacing `<ip_address>` and `<port>` with the values from your watch:
   - ```cmd
     adb connect <ip_address>:<port>
     ```
   - After running the command, you should see a message confirming that the connection was successful.
5. **Open Watch Face Studio and load the project as described in the "Loading the Project" section above.**

6. **If you want to remove some of the features like the step counter or weather tracker,**
    - Find the relevant widget in the items on the left sidebar and hover your mouse over the lock icons.
    - This will change the icons to an eye, which you can click on to toggle the visibility on the watch once you perform step 7.  I couldn't figure out how to turn these items into complications / widgets that you can enable or disable from the watch itself.
    - Above the list of these items is a category selection labeled either "NORMAL" or "ALWAYS-ON".
    - You can click on them to change what is visible when the watch lights up as you raise your arm, or if you have Always on mode enabled what is visible there.
    - Always On has a limitation of 15% of the pixels on the watch face can be illuminated at maximum, which is why stuff like the background picture cannot be set to visible, but other things can.
   
8. **On the top right, click the "Run on device" button.** You should see your watch listed as a target device. Select it and click "OK" to install the watch face on your watch.

## Credits
bighead.0@gmail.com /  @ Ay, el mao#3513 on discord / @ "benancio_gomez" on discord

- for their datamined assets project

  



 
