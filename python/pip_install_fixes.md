### Issues installing pyqt/qt on apple silicon, encountered long hangs, simplib etc not found [apple, m1, pyqt, silicon, qt, brew]

FIX: https://stackoverflow.com/a/72363753

```bash
#As I answered here, Rosetta is not required if you're willing to use Homebrew's pyqt@5. 
#Homebrew includes an arm64-compiled pyqt5, and one can leverage its installation in a 
#venv using the --system-site-packages flag to venv:

# Install pyqt5 via homebrew
brew install pyqt@5
# Note that it's installed in python3.9, not 3.10
brew cat pyqt@5 | grep 'depends_on.*python'
  depends_on "python@3.9"
# Make a python3.9 virtualenv with access to the system's site-packages
/opt/homebrew/bin/python3.9 -m venv --system-site-packages .venv
source .venv/bin/activate
```
