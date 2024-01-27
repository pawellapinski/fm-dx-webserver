# FM-DX Webserver 📻🌐

FM-DX Webserver is a cross-platform web server designed for FM DXers who want to control their TEF6686 / F1HD receiver through a web interface.

## Features

- 🌐 **Web-Based Control:** Access and control your TEF6686 / F1HD receiver from any device with a web browser.
- 📻 **FM DXing:** Enhance your FM/AM DXing experience with a user-friendly web interface.
- **Cross-Platform:** You can run this on both Windows and Linux servers along with xdrd.
- **Tuner control:** Control your FM tuner on the go. Phone? Tablet? No problem.
- **Low-latency streaming**: Built in directly into the webserver, no external apps needed for users

##  Features to be added
Check here for an up to date task list: https://github.com/NoobishSVK/fm-dx-webserver/issues/3

## Getting Started
Please install **node.js version 21.5.0** or older to make this work. 
Version >=21.6.0 is currently not working correctly. 

1. Download or install ffmpeg (optional, but needed if you want the audio stream to work)

    ```bash
    Linux (Ubuntu/Debian): 
    sudo apt install ffmpeg

    Windows: 
    https://www.geeksforgeeks.org/how-to-install-ffmpeg-on-windows/
    ```

2. Clone the repository (or alternatively download it manually):

    ```bash
    git clone https://github.com/NoobishSVK/FM-DX-Webserver.git
    ```

3. Nagivate to the fm-dx-webserver folder in your terminal and run this command:

    ```bash
    npm install
    ```

4. Update your config in userconfig.js:

    ```js
    const webServerHost = '0.0.0.0'; // IP of the web server
    const webServerPort = 8080; // web server port
    const webServerName = "Noobish's Server"; // web server name (will be displayed in title, bookmarks...)
    
    const audioDeviceName = "Microphone (High Definition Audio Device)"; // Audio device name in your OS 
    const audioPort = 8081; // Port for the audio stream
    
    const xdrdServerHost = '127.0.0.1'; // xdrd server IP (if it's running on the same machine, use 127.0.0.1)
    const xdrdServerPort = 7373; // xdrd server port
    const xdrdPassword = 'password'; // xdrd password (optional)
    
    const qthLatitude = '50.123456'; // your latitude, useful for maps.fmdx.pl integration
    const qthLongitude = '15.123456'; // your longitude, useful for maps.fmdx.pl integration
    
    const verboseMode = false; // if true, console will display extra messages

    ```


4. Start the server:

    ```bash
    node .
    ```

4. Open your web browser and navigate to `http://web-server-ip:web-server-port` to access the web interface.

## Dependencies

This project utilizes the [librdsparser](https://github.com/kkonradpl/librdsparser) library for RDS parsing. Make sure to check out the library for more information.

## Contributing

Feel free to contribute to the project by opening issues or submitting pull requests. Your input is valuable!

## License

This project is licensed under the [GNU-GPL v3 License](LICENSE.md).

## Acknowledgments

- Thanks to [librdsparser](https://github.com/kkonradpl/librdsparser) for providing the RDS parsing functionality.

Happy DXing! 🎶📡
