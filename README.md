Create KML file (and/or CSV file)for all geo-tagged images (jpg or tif) in a directory. Author: Gerry Gabrisch GISP (gerry@shuksangeomatics.com) Python v3.6 Tested and working on: Ubuntu 22.04.  This tool will create a KML with an arrow showning drone camera angle.  This tool requires the libxmp library and is based on exempi.  exempi is not compiled for Windows.  This tool will likely work on Appl OS X but is untested.  See here for more details on libxmp and exempi:  https://python-xmp-toolkit.readthedocs.io/en/latest/installation.html

As of this writing Google Earth does not support relative paths in a KML.  So moving the directory of images will make them not display in Google Earth. The point, arrow location, and other EXIF and XMP values will still be in the popup if you click the arrow icon in Google Earth.

This tool will take a directory of geo-tagged images (including images in any subdirectories) and it will create a KML file and/or a CSV file in that directory.  The tool exploits XMP data for camera azimuth and produces a KML file pointing in the direction of the camera yaw value.  Tested on DJI P3P, DJI P4P, DJI P4Pv2, DJI Mini Pro 3, Parrot Sequoia, and OpenCamera on Android.

The output KML file can be opened in Google Earth and each image will be referenced by a Google Earth icon (arrow). Each icon is labeled with the image name.

Clicking on an icon in Google Earth will open a balloon box displaying the image. The balloon box will also include metadata including the image path relative to the KML, the image capture date, camera azimuth, and GNSS elevation. You can then select to view the full sized image in Google Earth

The CSV file can be imported into a GIS using WGS84 with elevation is height above the WGS84 elipsoid (if your images also include elevation in the EXIF).

Installation Download the project and run at a bash or cmd in the same directory as setup.py $python setup.py install

How to Execute:

The easy way is to furn geotag_gui.py from your favorite IDE.  This will open the GUI for you.

 Or from a command line 0pen in an new bash or in your favorite Python IDE */Geotagged_Image_Tools/geotagged_image_tools and run $python geotag_gui.py


Image location accuracy is affected by terrain, atmosphere, satellite availability and electronics quality. The positions displayed by this tool are extracted from the positions recorded by your GPS enabled camera. You can improve your location accuracy by letting your GNSS run prior to capturing images. 

This software is provided AS-IS, without warranty of any kind, expressed or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose and noninfringment. In no event shall the authors or copyright holders be liable of any claim, damages, or other liability, whether in an action of contract, tort or otherwise, arising from, out of or in connection with the software of the use or other dealings in the software. It is a copyright violation to distribute this program without permission of the author.
