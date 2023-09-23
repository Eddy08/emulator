### Minimal Setup of Emulator on Windows

Step 1: Download the cmd-line tools from official google site.
Step 2: extract the zip content of the above downloaded file to let's say cmdline-tools.
Step 3: inside the cmdline-tools create a new folder as latest
( Previously getting error when simply running avdmanager and sdkmanager commands for downloading )
Step 4: go to the latest > bin directory and run the following commands:
H:\Android\software\cmdline-tools\latest\bin>sdkmanager emulator
H:\Android\software\cmdline-tools\latest\bin>sdkmanager 'system-images;android-28;default;x86_64'
H:\Android\software\cmdline-tools\latest\bin>sdkmanager 'platform-tools'
H:\Android\software\cmdline-tools\latest\bin>sdkmanager 'build-tools;28.0.3'
H:\Android\software\cmdline-tools\latest\bin>sdkmanager 'platforms;android-28'

Step 5: Create AVD
avdmanager -s create avd -n Pixel -k “system-images;android-28;default;x86_64”

Step 6: Run Emulator: by going to emulator directory

H:\Android\software\emulator>emulator -list-avds
Pixel

H:\Android\software\emulator>emulator -avd pixel

Reference: <https://ksrk.medium.com/install-flutter-without-android-studio-on-window-9d3781172912>
