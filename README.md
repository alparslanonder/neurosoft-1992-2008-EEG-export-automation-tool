**Repository Name:** neurosoft-1992-2008-EEG-export-automation-tool

**Description:** Dearest Prof. Dr. Atilla Altunel, who is a retired neurologist, wanted to share his retrospective EEG recordings with us. He shared a Neurosoft “data-base” with us. We got the data, and we contacted the Neurosoft distributor in Turkey, who loaded the optimal application to our computer to make us open this database. However, since this application is an old one that ended in 2008, there were no multiple export options for EEG recordings. With this code, we exported all recordings, annotations, and internal EEG reports.

This repository contains an automation tool designed to streamline the process of exporting EEG data from Neurosoft software for the years 1992 to 2008. The tool uses image recognition and OCR to navigate the software's interface and extract relevant data, saving significant time and effort in data management tasks.

**Prerequisites:**
1. **Python 3.x** - Ensure you have Python 3.x installed on your system.
2. **Libraries:**
   - `pyautogui` - For automating GUI interactions.
   - `opencv-python` - For image processing.
   - `numpy` - For numerical operations.
   - `pytesseract` - For optical character recognition (OCR).
   - `pillow` - For image handling.
3. **Tesseract OCR:**
   - Install Tesseract OCR on your system.
   - Ensure the Tesseract executable is in your system's PATH.
4. **Neurosoft Software:** 
   - Ensure the Neurosoft software is installed and configured on your system.
5. **Operating System:**
   - Compatible with Windows (tested) due to the use of GUI automation which may vary across different operating systems.

**Installation:**
1. **Clone the repository:**
   ```sh
   git clone https://github.com/alparslanonder/neurosoft-1992-2008-EEG-export-automation-tool.git
   ```
2. **Navigate to the project directory:**
   ```sh
   cd neurosoft-1992-2008-EEG-export-automation-tool
   ```
3. **Install the required Python libraries:**
   ```sh
   pip install -r requirements.txt
   ```
**Usage:**
1. **Run the Automation Script:**
   - Execute the main Python script to start the automation process:
   ```sh
   python neurosoft_automation.py
   ```
2. **Monitor the Process:**
   - The script will automatically interact with the Neurosoft software, navigating through the interface, and extracting EEG data.
   - The extracted data will be saved in appropriately named folders on your desktop.
3. **Customize as Needed:**
   - Adjust the paths to image assets or modify the script logic as needed to accommodate any changes in the Neurosoft software interface or specific requirements.

**Example Workflow:**
1. **Run the Script:**
   ```sh
   python neurosoft_automation.py
   ```
2. **Wait for Completion:**
   - The script will take control of the Neurosoft software, navigating through the interface, performing OCR, and exporting data as per the specified logic.

3. **Review Exported Data:**
   - Once the script completes, review the exported data in the created folders on your desktop to ensure all required information has been captured and exported correctly.

## Process:
1. **Navigate to the Checkup Selection Screen:**
   - The script uses another shortcut to open the checkup selection screen.
2. **Locate Initial Subfolder:**
   - The script locates the initial subfolder using an image of the "Archive" folder.
3. **Extract Text:**
   - The script captures a screenshot of the region containing the subfolder list and uses OCR to extract the names of the subfolders.
4. **Create Folders:**
   - For each subfolder, the script creates a corresponding folder on the desktop.
5. **Navigate and Extract Data:**
   - The script navigates through each subfolder, lists the files, and counts the number of EEG records.
6. **Export Data:**
   - The script automates the export of EEG recordings, annotations, and internal EEG reports for each individual.

## Notes:
- **Accuracy of OCR:** Ensure that the Tesseract OCR is properly configured and trained to recognize text accurately from the Neurosoft software interface.
- **Screen Resolution:** The script relies on specific screen coordinates and image recognition. Ensure your screen resolution and layout are consistent with the script’s configuration.
- **Error Handling:** The script includes basic error handling, but further enhancements might be needed to handle unexpected pop-ups or changes in the Neurosoft software interface.
- **Customization:** You may need to adjust image paths and other configurations according to your specific setup and requirements.

