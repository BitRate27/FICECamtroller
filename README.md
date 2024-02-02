# FICE Camtroller

## Background
Frustrated using the PTZ Optics software to run our weekly stream, I turned to the web. I found this great video by Churchfront https://www.youtube.com/watch?v=c4RHOwh5f5k showing how to get the best settings, and it helped tremendously. In it, Matt asks if anyone knows a better way. Well after diving into this for a few months, I came up with one.

As Matt points out in the video, the current Focus, Image, Color and Exposure (FICE) settings are stored when you save a preset. When you recall a preset, those settings overwrite your current settings. This means that after you have spent time finding the best settings for your environment, when you recall a preset they get wiped out and replaced with the settings in the preset. The video shows you how to use the onscreen menu from the PTZOptics software to navigate the menus. These menus are like the menu on your tv monitor or projector, designed to be used with a simple remote control. When I saw this, I thought...there has to be a better way.

A quick search of 'ptzoptics sdk' took me to the ptzoptics developers portal. This site introduced me to the VISCA commands that can be sent to the camera over the network. These commands openned the door to a way to workaround the problems with the ptzootics software and a better way of using the underlying controls hidden in the onscreen menus.
  
After digesting the documentation of the commands, I set out to develop an App to control the camera. The key role of the App is the ability to download the camera's FICE settings, store in a file, and then upload those settings into the camera. This allows you to dial in your FICE settings until they are perfect for your environment, save them, and then overwrite any preset with those settings. The App doesnt change the Pan, Tilt and Zoom (PTZ) settings in the presets. The App basically acts as a more useful Advanced panel as it works in concert with the PTZ optics software or any controller you may have. You can even load those FICE settings into other cameras.

## How to use it

### Install
1. Download the App for your platform by selecting the latest release on the right.
2. Install the App
2.1  For MacOS: Unzip the .zip file and double click on the .app file
2.2  For Windows: double click on the .msi file

### Run the App
4. Enter the IP address of the camera in the Camera IP field. Press Enter/Return
5. Open up the PTZ Optics software and Recall a preset
6. Select the Refresh button in FICE Camtroller
    - Notice the FICE values might change, if they did then there are FICE settings stored in that preset
  
### Save the best FICE settings
7. Change the FICE settings for the camera using FICE Camtroller, PTZ Optics, or the PTZ Menu
8. Select the Refresh button in FICE Camtroller to display the current settings
9. Select the Download button in FICE Camtroller to save the settings to a local file
   - On mac: /Users/[username]/Library/settings.json
   - On windows: %AppData%\FICE Camtroller\settings.json
  
### Fix a preset
10. Select Recall mode (hollow circle) in PTZ Optics
11. Select a preset in PTZ Optics
12. Select Upload button in FICE Camtroller to Upload the saved settings to the camera
13. Change the Preset mode to "Set" (hollow circle) and select the preset you recalled in step 11

If you want to use those same settings for the presets on another camera, then change the IP address in FICE Camtroller and repeat steps 10-13 for all the presets.


## Benefits
You may also choose to use FICE Camtroller as your main interface for adjusting FICE settings
- Complete control over settings like White Balance, only available in PTZ Menu mode
- Easier to navigate than PTZ Menu
- Refresh button to see actual values stored in presets or values which may have been changed my PTZ Optics, PTZ Menu or another controller.
- Ability to share FICE settings across cameras
    
