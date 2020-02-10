# automation-report

Python package to generate HTML report of your automation cases and its steps with its valid status.


### Installation
```
$ pip install automation-report
```

### Code Example
```
# Importing package
from automation_report import report

# Use starttest() method to start a new case with its name given as parameter
report.starttest("CASE 0001: Test the screen")

# Populate the various steps status with info(), success(), fail() methods for particular case
report.info("Page is opened")
report.success("It works")
report.fail("Well, it didn't worked.")

# End above started case
report.endtest()

# Create yet another case as following
report.starttest("CASE 0002: Another case")
report.info("DOnet screen")
report.success("It works")
report.endtest()
# User close method to finally complete whole report generation
report.close()
```