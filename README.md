# test-esp32-c3
Test ESP32-C3 with Arduino CLI

# Steps

Initialize the configuration file
```
arduino-cli config init --dest-dir .
```

Add the boards definition to the config file [URL from GitHub](https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_dev_index.json).

Install the board
```
arduino-cli core update-index --config-file arduino.yaml
```

Add the ESP32 core, prepare for compilation
```
arduino-cli core install esp32:esp32 --config-file arduino-cli.yaml
arduino-cli board search c3 --config-file arduino-cli.yam
arduino-cli board 
```

Compile
```
arduino-cli compile -b esp32:esp32:esp32c3 --verify
```
or, to get the bin files
```
arduino-cli compile -b esp32:esp32:esp32c3 --build-path $PWD/.cache/
```
