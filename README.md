# Run Opentrons Thermocycler Stand-alone
This is a small python script to operate the [Thermocycler Module](https://www.opentrons.com/modules/#thermocycler)  WITHOUT OT-2 Robot.

## Background
I wanted to install a PCR device to the [LabDroid Maholo](https://rbi.co.jp/en/) to implement varieties of protocols that require PCR process.
There are few options of PCR devices which support robot arm interactions.
The Opentrons Thermocycler Module is available at very affordable price (Kudos to Opentrons!).
I ordered this module, connected to a Raspberry Pi, and wrote a python script to validate this module for serious biological protocols.

![A scene of experiment](https://github.com/mtoutai/ot_thermocycler_standalone/blob/master/photo.jpg)

## License
Apache-2.0

## Disclaimer
THIS SOFTWARE IS PROVIDED BY THE AUTHOR ``AS IS'' AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

## Requirements
- Raspberry Pi any model with at least 1 USB port.
- Python version >= 3.6
- PySimpleGUI

## How to install
```
mkdir -p Documents # Or you can specify whatever useful directory for you.
# clone opentrons
git clone https://github.com/Opentrons/opentrons.git
# clone this project
git clone https://github.com/mtoutai/ot_thermocycler_standalone.git
# change directory to execute the program
cd ot_thermocycler_standalone
# make a symbolic link to the thermocycler driver
ln -s ../opentrons/api/src/opentrons/drivers/thermocycler/driver.py
# install PySimpleGUI if it is not installed yet.
pip3 install PySimpleGUI
# Run the program
python3 ./pcr_gui.py
```
![A simple graphical user interface](https://github.com/mtoutai/ot_thermocycler_standalone/blob/master/screenshot.jpg)

## How to perfrom PCR
