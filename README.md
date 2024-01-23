# Wim Hof HR

## About 

I have made a few adjustments to [https://github.com/kbre93/dont-hold-your-breath](this project) to make it suitable for usage in a small experiment setting. First, I added a GUI to allow users to select the specific Polar monitor they wish to connect to. Then, I changed the data output to use the format `serialnumber-date-time`, ensuring anonymity but also allowing the researcher to differentiate between the different trials.


## Features

- Connect to a Polar H10 heart rate monitor, simultanesouly record accelerometer and heart rate data (interbeat interval)
- Use a GUI to choose the specific monitor you wish to use
- Calculate and breathing rate and heart rate varability
- Visualised trends in breath rate and heart rate varability to explore the br-hr relationship

## Installation
    
    python -m venv venv
    source venv/bin/activate  # On Windows, use `my_project_env\Scripts\activate`
    pip install -r requirements.txt

## Usage

    python DHYB.py --record-len 60 (this would run it for one minute)

    options:
    --use-sample-data     Use sample data loaded from a file
    --record-len 60       Length of recording in seconds

The program will show a GUI allowing the user to select which monitor they wish to use.
For best breathing detection, ensure the Polar H10 is fitted around the widest part of the ribcage


