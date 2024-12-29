"As a team, we carried out the following procedure step by step to successfully complete our RetroPie gaming project:

Installing RetroPie on Raspberry Pi:

We began by downloading the RetroPie image file for Raspberry Pi 3 from the official RetroPie website.
Using a tool called balenaEtcher, we flashed the RetroPie image onto a microSD card. This involved selecting the downloaded image file, choosing the microSD card as the target, and clicking 'Flash' to begin the process.
Once the flashing was complete, we safely removed the microSD card and inserted it into the Raspberry Pi.
Connecting Peripherals and Booting RetroPie:

Next, we connected the Raspberry Pi to the required peripherals: a joystick, a keyboard, and a display using HDMI.
We powered on the Raspberry Pi, and as RetroPie booted for the first time, it prompted us to configure the joystick. Following the on-screen instructions, we mapped the joystick’s buttons and saved the configuration.
Establishing Network Connection:

To enable communication between the Raspberry Pi and our computer, we set up a Wi-Fi connection secured with WPA2:

We removed the microSD card, inserted it into our computer, and navigated to the boot partition.
Inside the boot directory, we created a file named wpa_supplicant.conf .

After saving the file, we reinserted the microSD card into the Raspberry Pi and booted it up.
The Raspberry Pi connected to the Wi-Fi network automatically. To confirm, we used a connected keyboard to run the hostname -I command in the terminal, which displayed the device's IP address.
We then established an SSH connection:

From our computer, we used PuTTY, a tool for accessing remote systems via SSH.
We entered the Raspberry Pi’s IP address in PuTTY, set the port to 22, and clicked 'Open' to connect.
After logging in with the default credentials (username: pi, password: raspberry), we had full access to the Raspberry Pi’s terminal remotely.
Configuring the LCD Screen via SSH:

Once connected via SSH, we worked on configuring the LCD screen:
We identified the LCD model and downloaded the required drivers by running the commands provided in the screen’s documentation.
After installing the drivers, we edited the configuration file /boot/config.txt using the nano text editor. This involved enabling SPI and I2C interfaces and adjusting the screen resolution settings to match the LCD.
We also modified the orientation settings to ensure the display appeared correctly.
Once these changes were made, we rebooted the Raspberry Pi to apply the new settings.
Loading Files onto the Raspberry Pi:

To add game files, or ROMs, we used FileZilla, an FTP client.
In FileZilla, we entered the Raspberry Pi’s IP address, username (pi), and password (raspberry) to connect to its file system.
We navigated to the ~/RetroPie/roms directory and uploaded the ROM files for various emulators, ensuring they were placed in their respective folders (e.g., NES games in the nes folder, SNES games in the snes folder).
Testing and Final Setup:

After transferring the files, we rebooted the Raspberry Pi to load the newly added games into RetroPie.
We tested the setup by playing several games, confirming that the joystick, display, and emulation worked perfectly.
Through this step-by-step process, we successfully built a functional RetroPie gaming device with a joystick and display, turning our Raspberry Pi into an all-in-one retro gaming console!"
