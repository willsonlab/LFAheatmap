# LFAheatmap
Python code to generate greyscale heatmap for displaying results of antibody screening in lateral flow assay.
Background shade represents the ratio of test-line signal to control-line signal for antibody pairs tested with 0 analyte. This is often referred to as non-specific-binding (NSB).
The lowest value in the NSB matrix is represented as white, while the highest value in NSB matrix is set as black. On the right side of the output a gradient bar is displayed that indicates what the high and low values of the set are.
The values displayed inside the heatmap cells display the ratio of the test-line signal to control-line signal for the positive analyte strip subtracted by the corresponding NSB value.  That is, the difference between positive analyte and zero analyte signal. The difference is used to keep the scales of interaction more comparable. The positive analyte strips are expected to have the same level of non-specific-binding as the 0 analyte strips. Since the 0 analyte values are already represented as the shade, we find it more informative to subtract these values when displaying the positive interaction for the antibody pair. 
Data is input via excel sheets. When ran the the shell will prompt you to select a file via the file browser. After selecting your excel sheet, it will list the names of each of the sheets in the workbook and prompt you to select the sheet that contains the NSB data. After this it will prompt you to select the sheet containing the positive analyte data. 
In making your spreadsheet it is expected that you will calculate the difference between positive and 0 analyte for the second sheet within excel itself. The code will not do this. 
The labels for the heatmap are hard-coded in. Edit the code as necessary to fit your labels.
It is hard coded to input a 6 by 6 matrix, skipping the first row and the first column (i.e., cells 2 to 8 in each direction). Adjust it as necessary to match your screening.


The code was written by Austin Hahn with assistance from ChatGPT. Contact willsonlab for any inquiries.
