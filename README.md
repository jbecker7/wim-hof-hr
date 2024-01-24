# Wim Hof HR

## About 

I have made a few adjustments to [this project](https://github.com/kbre93/dont-hold-your-breath) to make it suitable for usage in a small experiment setting. First, I added a GUI to allow users to select the specific Polar monitor they wish to connect to. Then, I changed the data output to use the format `serialnumber-date-time`, ensuring anonymity but also allowing the researcher to differentiate between the different trials.


## Features

- Connect to a Polar H10 heart rate monitor, simultanesouly record accelerometer and heart rate data (interbeat interval)
- Use a GUI to choose the specific monitor you wish to use
- Calculate and breathing rate and heart rate varability
- Visualised trends in breath rate and heart rate varability to explore the br-hr relationship

## Installation

1. Check if Python is Installed:
   - Open the Terminal application
   - In Terminal, type `python3 --version` and press Enter. This checks if Python 3 is installed on your Mac.
   - If Python 3 is installed, you'll see a version number. If not, you'll get a message saying "command not found."

2. Install Python (if not installed):
   - Go to the official Python website: https://www.python.org/downloads/
   - Download the latest Python 3 installer for macOS.
   - Open the downloaded file and follow the installation instructions.

3. Download the Code from GitHub:
   - Go to https://github.com/jbecker7/wim-hof-hr
   - Look for the green “Code” button and click it. Then, click “Download ZIP”.
   - Once the download is complete, find the ZIP file (likely in your Downloads folder) and double-click it to unzip it. This will create a folder named "wim-hof-hr-master" with the code.

4. Set Up the Python Virtual Environment and Install Dependencies:
   - Go back to terminal
   - Navigate to the directory where you unzipped the code: `cd path/to/wim-hof-hr-master` (so like if it's on your Desktop it is probably just `cd Desktop`)
   - Create a virtual environment: `python3 -m venv venv`
   - Activate the virtual environment: `source venv/bin/activate`
   - Install required packages: `pip install -r requirements.txt`

5. Run the Script:
   - Make sure the sensor has the strap wet and is on the participant.
   - In Terminal (inside the "wim-hof-hr-master" directory), type `python3 DHYB.py --record-len 60` to run the script (60 is the number of seconds for the recording length; you can change this to your desired duration).
   - If you want to run more than one, you can either do this in multiple Terminal windows or chain the commands together with `&`, for example, to run it twice without opening a new window, you could do:
	   - ```python3 DHYB.py --record-len 60 & python3 DHYB.py --record-len 60```
   - Follow the on-screen instructions in the popup GUI to choose the sensor.

6. Accessing Data:
   - Once the script has run, it will ask you if you want to save and then it will save the data files in the "data" folder inside the "wim-hof-hr-master" directory as two CSVs, which are named according to this pattern:
	   - `serialnumber-date-time-{acc/icc}``
	with the last part changing based on if it's the accelerometer and interbeat interval


