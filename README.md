# Complete guide to set up Keil µVision for your ES Lab!
- `STEP 1`:- **Download**<br>[**Direct download link**](https://armkeil.blob.core.windows.net/eval/MDK539.EXE)<br>**OR**<br>Go to this [website](https://www.keil.com/demo/eval/arm.htm) and download the software. It will ask you for some details, but you don't have to enter anything correctly. Put some random values and move on.
  ![Installation](https://github.com/ishan-surana/Keil--Vision-Installation/assets/121395061/21ccf25f-4c58-41f4-ae67-4b82f8c6d15e)<br><br>
- `STEP 2`:- **Installation**<br>The installer will get downloaded on to your device. Open it and begin installation. Ideally, **do not** change the paths in the dialog box and let the installation proceed. In the process you will get confirmation prompts as well; proceed regardless. After the installation completes, the Pack Manager will open.
  ![Pack Manager](https://github.com/ishan-surana/Keil--Vision-Installation/assets/121395061/f23f33a2-9f87-4e1d-ae8d-053090b3e049)<br><br>
- `STEP 3`:- **Package downloading**<br>Here, under manufacturer NXP, navigate to device LPC1768 under series LPC1700 -> LPC176x series. On the right panel, you will see a suggested package to install. Press install and hope it goes well.
  ![LPC168](https://github.com/ishan-surana/Keil--Vision-Installation/assets/121395061/c121c90c-a55b-4df6-b0ed-3da6793b7fd0)
  ![Pending installation](https://github.com/ishan-surana/Keil--Vision-Installation/assets/121395061/b42d9b64-28db-4134-a3f4-586fdfe75562)
  + !!!`PROBABLE ERROR`:-<br>Due to the shitty nature of the software, it won't install for you regardless of how many times you try to reinstall it. So follow the given steps to solve this error. 
  ![ERROR](https://github.com/ishan-surana/Keil--Vision-Installation/assets/121395061/4d76b686-8f58-4bc4-8f4a-245ec73c18e1)
    - **Solution =>** In the **File** menu, in *Settings* option, check the path where `cpackget` is located (in a default installation, `C:\Keil_v5\ARM\cmsis-toolbox\bin`). Navigate to that directory, and open it in Terminal. After, that run the following command:-<br><br><details><summary> `./cpackget.exe add -a http://www.keil.com/pack/Keil.LPC1700_DFP.2.7.1.pack`</details><br>
    This will essentially do what the Pack Manager was trying to do, but due to goofy-aah coding, it just won't.
  ![Installed](https://github.com/ishan-surana/Keil--Vision-Installation/assets/121395061/bda293fd-4f57-4946-933e-e5a1d431a825)
*CONGRATULATIONS!* The support for LPC1768 will finally have been installed! 🥳<br><br>
- `STEP 4`:- **Project build and run settings**
 Open up the Keil µVision software on your laptop. For a new project, you will be able to select the LPC1768 in your target device. Write up the code and add it to target folder. Now go to `Project` menu and click on `Options For Target`. In the `Target` tab, make sure that the missing compiler is NOT selected (any other is fine), and in the `Debug` tab, the `Use simulator` option is selected.<br>
 ![Project Target](https://github.com/ishan-surana/Keil--Vision-Installation/assets/121395061/0149cf95-2339-47ec-bdf7-9db56122cb90)
<img src="https://github.com/ishan-surana/Keil--Vision-Installation/assets/121395061/46bf0108-f9e6-4c56-a3ae-07baa4c0d887" alt="Target" width="45%"/>
<img src="https://github.com/ishan-surana/Keil--Vision-Installation/assets/121395061/f62639c7-d408-40c7-9478-d1bac7eaf3d6" alt="Debug" width="45%"/>

<br><br>
  **Now you can build and run your programs as show in lab! ✨**
