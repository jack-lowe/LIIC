
****************
* Introduction *
****************

This code generates a sets of linearly interpolated coordinates from two .xyz files and prints as a Gaussian09 input file (ORCA, GAMESS and QChem 5.0 coming soon)

****************
* Instructions *
****************

1) $ ./LIIC input.txt 1.xyz 2.xyz

2) Follow instructions

'input.txt' is the input block NOT containing coordinates BUT containing charge/multiplicity of the system. There should be no blank line above and below the text.


Example:

****************
#p b3lyp/cc-pvdz

Title

0 1
****************

'.xyz' must be in the format of cartesian coordinates (in either Angstrom or Bohr)

!!!!!!!!!!!!!
! IMPORTANT !
!!!!!!!!!!!!!

You must ensure that the coordinates are ordered in the same way in both 1.xyz and 2.xyz. If not, then the results will be meaningless and you will more than likely obtain an error when you go to run the calculation.

For example, the two sets of coordinates will work:

1.xyz
6         -1.61259       -1.28358        1.17087
6         -1.06326       -0.17969        0.57288
6          0.28829        0.10154        0.26876
6          1.39969       -0.66587        0.49882
6          1.51713       -2.00647        1.12641
8          2.67888       -2.43902        1.18980
6          0.39572       -2.75314        1.62225
6         -0.93479       -2.43765        1.63780
8          2.59287       -0.21906        0.13725
1         -2.69582       -1.28051        1.30694
1         -1.76525        0.60688        0.28355
1          0.49605        1.05829       -0.21551
1          0.69651       -3.71479        2.04381
1         -1.58203       -3.19931        2.08255
1          3.18745       -0.96815        0.42362

2.xyz
6         -1.60824       -1.39990        1.04705
6         -0.97142       -0.09152        0.70439
6          0.26774        0.10297        0.30486
6          1.34095       -0.91940        0.21510
6          1.39903       -1.97278        1.13985
8          2.76947       -2.54497        1.32404
6          0.42870       -2.62266        1.86263
6         -1.02360       -2.45017        1.58568
8          2.45856       -0.44466       -0.42184
1         -2.66312       -1.46204        0.83810
1         -1.61545        0.76707        0.78961
1          0.60312        1.10119        0.08182
1          0.73510       -3.41193        2.51960
1         -1.62585       -3.32047        1.78622
1          3.15453       -1.08574       -0.40124


Whereas the following will produce garbage:

1.xyz
6         -1.61259       -1.28358        1.17087
6         -1.06326       -0.17969        0.57288
6          0.28829        0.10154        0.26876
6          1.39969       -0.66587        0.49882
6          1.51713       -2.00647        1.12641
8          2.67888       -2.43902        1.18980
6          0.39572       -2.75314        1.62225
6         -0.93479       -2.43765        1.63780
8          2.59287       -0.21906        0.13725
1         -2.69582       -1.28051        1.30694
1         -1.76525        0.60688        0.28355
1          0.49605        1.05829       -0.21551
1          0.69651       -3.71479        2.04381
1         -1.58203       -3.19931        2.08255
1          3.18745       -0.96815        0.42362

2.xyz
6         -1.62732       -0.55134        0.48589
6          0.88046       -0.34144       -0.16030
6          0.67952        1.08958       -0.16279
6         -0.69058        1.62829       -0.23487
6         -1.74862        0.87178        0.09813
1         -1.80639       -0.86554        1.50773
1         -0.78937        2.65766       -0.54781
1         -2.76047        1.25438       -0.00201
6         -0.02762       -1.47799       -0.37211
1          0.49501       -2.41597       -0.20590
6         -1.41796       -1.50565       -0.58887
1         -1.89551       -2.47495       -0.60523
8          2.13818       -0.72782        0.06389
1          2.65825        0.06924        0.14302
8          1.65424        1.81141       -0.10132

****************
*    To-Do     *
****************


- Add in functionality for GAMESS-US, ORCA and QChem (maybe others, but we'll see)


Queries, questions and bugs should be directed to: jacklowe_@outlook.com 


