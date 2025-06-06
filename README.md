# stat on pixel

## An easy to use cv2 based procedure to automate the counting of micro plastics

To increase the efficiency of microplastic monitoring, we propose an automated counting method for micro-plastics which are fluorescent stained using Nile Red (NR) dye. NR dye treatment is found to be the most effective in terms of adsorption and fluorescence intensity for micro-plastics (Maes et al.2017) making it easier to identify in an image taken over an orange filter.
The method we propose has 5 main steps. 

<ol>
  <li>Raw image is split into the respective red, green and blue bands</li>
  <li>Gaussian blur is applied with a user defined kernel size and an in-situ variance depending on the kernel size</li>
  <li>An adaptive thresholding step where the image is segmented to a binary image based on the object pixel intensity within a user defined neighbourhood</li>
  <li>A contour extraction algorithm based on border following (Suzuki et al. 1985) is used on the binary image to extract the outer contours of the objects</li>
  <li>A filter based on the contour size specified by the user is applied to count the appropriated objects within a certain size range</li.
</ol>
 
This code was developed by Rajitha Athukorala as part of his PhD internship program with [DCCEEW](https://www.dcceew.gov.au/)

If you intend to use it and is keen to know more about future developments of 'stat on pixels', reach out to me at rajitha.athukorala@sydney.edu.au 
