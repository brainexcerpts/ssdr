# Computer Graphics Gems JP 2015:5. "Skinning Decomposition" sample code
This is a sample implementation of the algorithm "Smooth Skinning Decomposition with Rigid Bones" presented in Chapter 7 of [Computer Graphics Gems JP 2015] (http://www.borndigital.co.jp/book/5498.html, "Computer Graphics Gems JP 2015")

## How to Build and Run.
This is a Visual Studio 2013 Professional project. You will need the libraries [Eigen] (http://eigen.tuxfamily.org/ "Eigen") and [QuadProg++] (http://quadprog.sourceforge.net/ "QuadProg++"). Eigen 3.2.4 and QuadProg++ 1.2.1 were used to build and run tests.

You can download the mesh animation data from [Mesh Data from Deformation Transfer for Triangle Meshes] (http://people.csail.mit.edu/sumner/research/deftransfer/data .html and place it in the designated folder.

The easiest way to build and run is as follows.

Pass the include path to the Eigen installation folder.
Download QuadProg++ and copy the following four files to the ssdr folder.
 * QuadProg++.hh
 * QuadProg++.cc
 * Array.hh * Array.cc
 * QuadProg++.hh * Array.cc
 
3. [Mesh Data from Deformation Transfer for Triangle Meshes](http://people.csail.mit.edu/sumner/research/deftransfer/data.html "Mesh Data From. 
Download "Horse gallop animation from the video." from "Deformation Transfer for Triangle Meshes") and use "horse-gallop-01.obj" from "horse-gallop-01.obj" in the compressed archive. Copy all obj files of "gallop-reference.obj" to the ssdr/data folder.
4. build and run with Visual Studio

## Adjustment of calculation parameters.
The main parameters of SSDR are specified in the ssdrParam structure around line 339 of HorseObject.cpp in HorseObject::OnInit.
* numIndices: Maximum number of bones allocated per vertex.
* numMinBones: The minimum number of bones used to approximate a vertex animation.
* numMaxIterations: maximum number of iterations.

By changing these three parameters, you can see the changes in the calculation results.

## References.

1. Binh Huy Le and Zhigang Deng, Smooth Skinning Decomposition with Rigid Bones, ACM Transactions on Graphics, 31 (6), (2012), 199:1-199:10.
2. Binh Huy Le and Zhigang Deng, Robust and Accurate Skeletal Rigging from Mesh Sequences, ACM Transactions on Graphics, 33 (4), (2014), 84:1-84:10.

## Change history.
1. 24/08/2015 First published on 24/08/2015

Translated with www.DeepL.com/Translator (free version)
