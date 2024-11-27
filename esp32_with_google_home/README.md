# Google Integration with ESP32 via Arduino Cloud

This guide walks you through integrating Google Home with an ESP32 using the Arduino Cloud platform. By the end of this setup, you'll be able to control devices (like lights) using your ESP32 and monitor them via the Arduino Cloud interface.

---

## Steps to Set Up the Integration

### 1. Set Up Arduino Cloud

1. Go to [Arduino Cloud](https://cloud.arduino.cc/).
2. Click **Get Started** and log in to your Arduino Cloud account. If you don’t have an account, create a new one.  
   <img src="https://github.com/user-attachments/assets/9104c351-2d7e-4afc-b7d9-74d2402550da" width="200" />  

3. From the left menu, select the **Devices** option.  
   <img src="https://github.com/user-attachments/assets/437df131-a52e-4ac8-b398-f2ec14f42090" width="400" />  

4. On the top right, click the **Add Device** option.  
   <img src="https://github.com/user-attachments/assets/007ed743-ab12-4171-b812-ab47a925f754" width="200" />  

5. Select **Third Party** under board options.  
   <img src="https://github.com/user-attachments/assets/f3798411-b80f-4199-8a99-4119ba6b3d5a" width="400" />  

6. Choose **ESP32** and select **ESP32 Dev Module**.  
   <img src="https://github.com/user-attachments/assets/684aa528-e507-49db-bd42-1241ad6c28ea" width="400" />  

7. Name your device and proceed.  
   <img src="https://github.com/user-attachments/assets/98ab83b9-a3ba-486b-b69d-de703e33bbd9" width="400" />  

8. Download the provided PDF containing your **Secret Key** and **Device ID**—these will be needed later for integration.  
   <img src="https://github.com/user-attachments/assets/2c9825cb-1ffc-457d-ab33-68b75deeddb1" width="400" />  

### 2. Set Up a "Thing"

1. Navigate to the **Things** section from the main menu.  
   <img src="https://github.com/user-attachments/assets/6174ffb0-0be0-4f9a-8802-7e44c5af2c2c" width="300" />  

2. Click the **Add Things** button in the top right.  
   <img src="https://github.com/user-attachments/assets/3798869e-fed1-482f-a357-2cf29c0b6571" width="300" />  

3. Click **Add** and give the "Thing" a name (e.g., "Light").  
   <img src="https://github.com/user-attachments/assets/3115ad7f-c3a2-462b-9be5-35c44cd19d55" width="400" />  

4. Select the variable type as **Light** by choosing the "Light and Color" option.  
   <img src="https://github.com/user-attachments/assets/ed6f0d03-f204-4620-a3de-f58220bbffff" width="400" />  

5. Configure the variable permissions (e.g., Read/Write) and click **Add Variable**.  
   <img src="https://github.com/user-attachments/assets/1e5aefb5-8885-463b-b24a-3a2869207218" width="400" />  

   - For multiple lights, you can duplicate variables and modify their declarations, such as `light_1`, `light_2`, etc.   
     <img src="https://github.com/user-attachments/assets/3b20c998-c4c3-4334-9bd5-d51729e64deb" width="800" />  

### 3. Associate Device and Configure Network

1. On the right, click the **Associate Device** option and select the ESP32 board you previously created.  
   <img src="https://github.com/user-attachments/assets/483f4cc7-1fd5-43aa-8448-4da5c2f0cc8b" width="400" />  

2. Enter your network credentials under the **Network** section:  
   - WiFi **SSID** and **Password**  
   - The **Secret Key** from the PDF you downloaded earlier.  

### 4. Integrate with Google Home

1. Navigate to the **Home Integration** section and select **Google Home**.

### 5. Upload the Sketch

1. Click on the **Sketch** option at the top right to open the Arduino Cloud IDE.  
   <img src="https://github.com/user-attachments/assets/074a8433-73c6-4db4-9095-44d30f5aa173" width="200" />  

2. Modify the code to define your ESP32’s pins while keeping the pre-defined functions intact. Here's an example:  
   ```cpp
   // Example code
   void onLightChange() {
       // Logic for toggling the light
   } 
3. If you're following this guide, use the code provided inside the .ino file above.

### 6. Flash the Code to ESP32  
1. Install the **Arduino Cloud Agent** on your system. Instructions will be displayed during the upload process.  
2. Connect the ESP32 to your system via USB and upload the code.  
3. Use the **Serial Monitor** to verify the flashing process. Ensure the ESP32 is properly connected during this step.

### 7. Set Up Google Home
1. Install Google Home and Login or Signup
2. Go to Device Section at the bottom menu and click add device
  <img src="https://github.com/user-attachments/assets/e8c878b4-b6a3-45f0-8f81-735d435f88ff" width="300" />

4. On the menus displayed select works with google home
  <img src="https://github.com/user-attachments/assets/1c47e601-387d-402a-b9bc-24bd4d577bba" width="400" />

5. Search for Arduino Cloud and Login with the same account you used to login to arduino cloud. There you can find the things you had created.

Happy Hacking...!
---

## Key Features  
- Control devices such as lights via Google Home integration.  
- Manage your ESP32 remotely with Arduino Cloud.  
- Easily expand to multiple devices with minimal configuration.  

---

## Troubleshooting  
- Ensure your ESP32 is in **boot mode** during flashing by pressing the boot button when prompted.  
- Double-check WiFi credentials and Secret Key for accuracy.  
- Use the **Serial Monitor** to debug any connectivity issues.

### Connect with Me  
For questions, suggestions, or collaboration, connect with me on [LinkedIn](https://www.linkedin.com/in/adheeb-v-k-6304b324b)
