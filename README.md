# STL-to-Point-Cloud-Dataset-Generator-
There are a number of freely available datasets of STL files (for example the Thingi10k https://ten-thousand-models.appspot.com/). These are datasets are useful for creating training datasets for machine vision experimentation. It is intended that the notebook provided can be used to generate a training dataset from a folder of stl files

Specifically, the notebook contains the code that does the following

1) It opens a working directory subfolder of STL files (/STL_Data), randomly selects an stl file within the folder and generates an array of the vectors of that STL file
2) Using the vectors of the STL file a number of randomly generated points over the surface of 3D model are generated
3) The randomly generated points are rotated by a random number of degrees about a randomly generated axis originating from the origin.
4) The randomly generated points are scaled such that the 3D model will fit within a cube of predefined size
5) Steps 1 to 4 are repeated a number of times. Each time that this process is repeated the x,y & z coordinates of the randomly generated surface samples are appended as a row of an array. Upon completion this array is saved as a csv file within the working directiory.
