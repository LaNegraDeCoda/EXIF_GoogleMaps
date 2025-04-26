EXIF Metadata Viewer
A simple web-based tool for viewing EXIF metadata from image files. This tool allows users to upload an image, view its GPS information (if available), and explore all of its EXIF metadata. It also provides an option to download the EXIF data in JSON format.

Features
View EXIF Metadata: Automatically displays EXIF metadata such as image orientation, camera settings, and more.

GPS Coordinates: If GPS data is available, it shows the latitude and longitude with a link to view the location on Google Maps.

Auto Rotation: If the image has an orientation tag indicating it's rotated, the tool will automatically display the image in the correct orientation.

Download EXIF as JSON: Allows users to download the metadata of the image as a JSON file for further use.

Demo
You can try the tool live by visiting the Demo Link.

Installation
Clone or download the repository.

git clone (https://github.com/LaNegraDeCoda/EXIF_GoogleMaps.git)
Open the index.html file in your browser.

Usage
Upload an image using the file input.

The EXIF metadata for the image will be displayed below the upload button.

If GPS data is available, the coordinates will be shown along with a link to view the location on Google Maps.

All available EXIF metadata is shown in a neat table.

The image will be displayed with correct orientation if the EXIF orientation tag is present.

You can click the Download EXIF as JSON button to save all the EXIF data in a JSON file.

Code Walkthrough
HTML Structure
The HTML consists of:

A file input (<input type="file" id="fileInput" accept="image/*">) for selecting an image.

A div (<div id="output"></div>) where the EXIF data and image preview will be displayed.

A Download EXIF as JSON button (<button id="downloadJson" style="display:none;">Download EXIF as JSON</button>).

JavaScript
The JavaScript code does the following:

Event Listener: Listens for changes to the file input (#fileInput). When an image is selected, it reads the file using the FileReader API.

EXIF Data Extraction: Uses the EXIF.js library to extract the metadata from the image. It then processes the GPS data, if present, and displays it.

Auto Rotate: If the image has an orientation tag, it adjusts the image's orientation using CSS.

Download JSON: If you click the "Download EXIF as JSON" button, it generates a downloadable file containing the EXIF data in JSON format.

GPS Data
If GPS coordinates are available, the tool will display:

Latitude

Longitude

A clickable link to open the location in Google Maps.

Convert DMS to Decimal Degrees
GPS coordinates are often stored in Degrees, Minutes, and Seconds (DMS) format. The function convertDMSToDD() converts these to Decimal Degrees for easier use and display.

Download EXIF as JSON
The Download EXIF as JSON button allows users to download the metadata of the image as a JSON file. This can be useful for saving, analyzing, or sharing the metadata.

Dependencies
EXIF.js: A JavaScript library for reading EXIF data from image files.

EXIF.js GitHub Repository

Contributing
Fork the repository.

Create a new branch for your feature or bug fix.

Make your changes and test them.

Submit a pull request with a description of your changes.

License
This project is licensed under the MIT License - see the LICENSE file for details.# EXIF_GoogleMaps
