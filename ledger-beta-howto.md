# Ledger Open Beta Howto

This guide will help you installing the Qubic Ledger app on your device.

> [!IMPORTANT]
> Tests are only possible on the following devices: Nano S Plus, Flex and Stax 
> In production, Nano X will also be supported, unfortunately Nano S won't as it's discontinued by Ledger.

> [!CAUTION]
> The installation requires technical knowledge (using the terminal).
> Install only on devices which are NOT used for relevant crypto holding.
> Installation at your own risk.

## Installation Steps

1) download and install python (https://www.python.org/downloads/)
2) download the zip file: https://github.com/LFG-Qubic/ledger-wallet-howto/blob/main/files/0.1.5.zip
3) your physical device must be connected, unlocked and the screen showing the dashboard (not inside an application)
4) Run these commands on your host from the app's folder (need to choose the device folder you're using):
```
IMPORTANT: Commands may be different based on OS etc.
# Install Python virtualenv
python3 -m pip install virtualenv 
# Create the 'ledger' virtualenv
python3 -m virtualenv ledger
```

Enter the Python virtual environment
on macOS : `source ledger/bin/activate`
for other environments: https://docs.python.org/3/library/venv.html#how-venvs-work

```
# Install Ledgerblue (tool to load the app)
python3 -m pip install ledgerblue 
# Load the app.
python3 -m ledgerblue.runScript --scp --fileName bin/app.apdu --elfFile bin/app.elf
```
5) Go to https://hw.qubic.org/ and interact with the device, create new addresses, send QUBIC back and forth. If you'd like to received some test tokens, let us know in the LFG channel in Discord.


Please let us know any issues and feedback.
Feel also free to spread the word on X ;-)

Thanks a lot, LFG!
