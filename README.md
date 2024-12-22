# Creating a Watch Face Using Tag Expressions

In this session, we are going to learn how to create a watch face using Tag Expressions. That means today we are going to create a watch face for smartwatches that run on the Wear OS operating system. 

## Prerequisites

Before we start, we need to understand some concepts:

1. **Watch Face Studio**  
   Watch Face Studio is a development tool where we can build a watch face without any code. However, we can use tag expressions to apply common logic to dynamically change the UI and state of the watch face.

2. **Smartwatch Modes**  
   There are two types of modes in a smartwatch:
   - **Always-On Mode**: This mode is visible all the time, so we will minimize and remove extra elements from the watch face to ensure battery efficiency.
   - **Normal Mode**: In this mode, we will implement more features and visual elements compared to Always-On Mode.

## What We Are Building

Today, we are going to create an **analog watch face** that includes:
- **Index components**
- **Analog hand components**

Additionally, we will implement a feature where the **battery level icon color changes to red** when the charge level is less than or equal to 20%. This logic will be implemented using the `BATT_PER` tag, which will be explained later in this documentation.

## Demonstration

Below, I will demonstrate the result of the watch face in different modes that we will create in today’s session for better visibility.

normal mode and greater than 20% charge

![normal mode and greater than 20% charge](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/result/Normal_Mode%20%26%26%20%20enough_charge.png)

normal mode and less than 20% charge

![normal mode and less than 20% charge](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/result/normal_mode%20%26%26%20less_charge.png)

always on mode mode and greater than 20% charge

![always on mode mode and greater than 20% charge](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/result/always_on_mode%20%26%26%20enough_charge.png)

always on mode mode and less than 20% charge

![always on mode mode and less than 20% charge](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/result/always_on_mode%20%26%26%20less_charge%20.png)

# Environment Setup

To create a watch face for smartwatches that run on Wear OS, first, you need to install and set up **Watch Face Studio**, which provides various tools to develop watch faces.

## Step 1: Download Watch Face Studio
1. Go to the given URL: [https://developer.samsung.com/watch-face-studio/download.html].  
2. Download **Watch Face Studio** according to the operating system of your machine.  
3. The download process may take some time depending on your internet connection.  
   - The download screen should look like this:  

![download screen](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/Images%20during%20the%20development%20phase/downloadPage.png)


## Step 2: Install Watch Face Studio
1. Complete the installation process.  

## Step 3: Open Watch Face Studio
1. After installation, open Watch Face Studio.  
2. You should see the initial interface, which looks like this:  

![initial screen](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/Images%20during%20the%20development%20phase/initialInterface.png)

# Development 

## Step 1: Create a New Project
1. Click on the **New Project** button located on the left side of the Watch Face Studio interface.  
2. Enter the project name and press **OK**.  
3. You will now see the main interface.

![New project creation](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/Images%20during%20the%20development%20phase/newProject.png)

4. Initial screen after creating a new project

![Alt text](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/Images%20during%20the%20development%20phase/initialScreenAfterCreate%20New%20Project.png)

## Step 2: Add Index Components
1. In the top panel bar, click the **Add Component** button with the **+ icon**.  

![Import Index](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/Images%20during%20the%20development%20phase/importIndex.png)

2. Import three indexes to act as different time indicators, as shown in the given images:  
   - **Select Number 4**: Set it as the large pointed stick index.  
   - **Select Number 12**: Set it as the small pointed stick index.  
   - **Select Number 60**: Set it as the small round stick index.  

![medium index](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/Images%20during%20the%20development%20phase/medium%20index.png)

![4 main index](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/Images%20during%20the%20development%20phase/4%20large%20index%20as%20hour.png)

![small index](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/Images%20during%20the%20development%20phase/second%20index.png)

3. Arrange the components to set up the interface accordingly.

## Step 3: Add Analog Hands
1. Import **Analog Hands** from the components list.  
2. Add three different hands to represent:
   - **Hours**
   - **Minutes**
   - **Seconds**
  
![select analog hand ](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/Images%20during%20the%20development%20phase/analog%20hand%20select%20for%20hour.png)

![minute hand ](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/Images%20during%20the%20development%20phase/munite%20hand.png)

![second hand](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/Images%20during%20the%20development%20phase/second%20hand.png)

3. Select the components to adjust their position and color for better visibility.
4. Now we implement hands and index in our watch face

![index and hands](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/Images%20during%20the%20development%20phase/index%20and%20hand%20added.png)

## Step 4: Adjust Time Display
1. At the bottom of the Watch Face Studio interface, you will see a **horizontal bar** that represents the time strap.  
2. Change the time using this bar to preview how the watch face looks in the panel.
   
![time](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/Images%20during%20the%20development%20phase/bottom%20display.png)

## Step 5: Add a Progress Bar for Battery Life
1. Import the **Progress Bar** from the components list and rename it as **Battery**.

![A progress bar](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/Images%20during%20the%20development%20phase/progress%20bar.png)

3. In the properties panel, select the option to show **Progress Bar + Icon + Text**.  

![A select option](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/Images%20during%20the%20development%20phase/progress%20bar%20%2C%20icon%20%2C%20text.png)

4. Under the **Default Provider** option, set it to **Watch Battery**.  
![A watch battery](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/Images%20during%20the%20development%20phase/provider%20as%20watch%20battery.png)

5. Place the battery component in the desired position based on user preference.

## Step 6: Implement Dynamic Functionality with Tag Expressions
Now, we will add a dynamic feature where the **battery icon turns red** when the battery life is less than 20%. This will be done using **Tag Expressions**.

1. **Create a Copy of the Battery Component**:  
   - Duplicate the battery component.
   - 
![copy battery](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/Images%20during%20the%20development%20phase/copy%20battery.png)
     
   - Change the icon color of the copied battery component to **red**.

![set colour for copy battery](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/Images%20during%20the%20development%20phase/color%20for%20copy%20battery.png)


2. **Configure the Original Battery Component**:  
   - Select the original battery component and go to the **Properties Panel**.
![original battery](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/Images%20during%20the%20development%20phase/orginal%20battery.png)
   - Focus on the **Color** option.
     
   - In the input field for opacity (default is `100%`), click the value field.  
   - Press the **Tag** button and enter the following condition:  
     ```
     [BATT_PER] <= 20 ? -100 : 0
     ```
![tag view](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/Images%20during%20the%20development%20phase/tag%20view.png)
     
![condition](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/Images%20during%20the%20development%20phase/tag%20condition.png) 
   - This condition means:
     - When the battery level is less than or equal to 20%, the opacity of the original battery component becomes **0%**, making it invisible.
     - Otherwise, the opacity remains at **100%**.

3. **Result**:  
   - The **copied battery component** (set to red) will now appear when the battery life is below 20%, as the original battery component becomes hidden.  
   - When the battery life is above 20%, the original battery component remains visible.


# Test the Watch Face

## Testing on a Real Watch
If you want to test the watch face after completion on a real device, follow these steps:

1. Ensure you have a smartwatch that runs on Wear OS.
2. Connect your PC and the watch to the same network.
3. Enable **Developer Mode** on your watch:
   - Go to **Settings > About Watch > Software Information**.
   - Press the **Software Version** 5 times to enable Developer Mode.
4. Once in Developer Mode:
   - Go to **Developer Options** and enable **ADB Debugging**.
   - Enable **Wireless Debugging**.
   - Note the **IP address** and **port number**.
   - Press **Pair on New Device**.
5. Open **Watch Face Studio** and click the **Run on Device** option at the top right of the interface.
6. Press the **+** icon, then enter the **IP address**, **port**, **pairing code**, and **pairing port**. Press **OK** to connect.

### Alternate Method: Using ADB Tool
If the above method doesn't work, you can use the **ADB tool** to establish a connection.

---

## Publishing the Watch Face
After completing the UI design and functionality based on preferences, it's time to release the watch face for users.

### Steps to Publish
1. Click the **Publish** button located at the top right of the Watch Face Studio interface.

![publish button](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/Publish%20apk%20and%20abb/publish%20button.png)

2. After clicking, you will see a **Loading Indicator** with two statuses:
   - **Analysis on Display Check** (top of the indicator).
   - **Analyzing on Circle Shape** (bottom of the indicator).

![loading state](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/Publish%20apk%20and%20abb/loading%20state.png)

3. The loading indicator verifies any potential errors that may interrupt the building process of the APK or AAB file.
   - It is recommended to use a **black display** for power efficiency.
4. Once both analyses are complete, a **Publish Form** appears.

![publish form](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/Publish%20apk%20and%20abb/publish%20form.png)


### Completing the Publish Form
1. **Package Name**:
   - Input a unique name according to naming standards. Non-unique names will be rejected by the Play Store.
2. **Output Location**:
   - Select the folder to store the generated APK or AAB file.
3. **Version Information**:
   - Specify the version name and version code (updated with future releases).
4. **Minimum SDK Version**:
   - This field is fixed. For most projects, it will be API 30+.
5. **Publish Type**:
   - Select the output format:
     - APK
     - AAB (required for Play Store submission)
     - Both APK and AAB.
6. **Keystore File**:
   - A **keystore** is a file containing security certificates used to sign your app or watch face.
   - Required for publishing updates. If you don’t have a keystore file:
     - Click **Create New Key**.
     - Fill in the required fields in the form that appears.
     - Select the **Keystore Path** to save the keystore file.
     - Complete the form and click **OK**.
     - The keystore file will be created and saved to the specified location.

![keystore form](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/Publish%20apk%20and%20abb/keystore%20form.png)


7. Return to the **Publish Form**, select the keystore path, and complete other fields like passwords and additional information.

### Final Step
1. Click **OK** to generate the APK or AAB file.
2. The file will be saved in the selected output location.
3. A **WFS (Watch Face Studio)** file will also be created to save and manage your watch face designs.

![save](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/Publish%20apk%20and%20abb/saved%20on%20local%20machine.png)

---

By following these steps, you will successfully create a dynamic watch face with a battery icon that changes color based on the charge level.



