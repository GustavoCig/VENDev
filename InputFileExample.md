This file serves to show an example of and explain the pattern used for the input file of VEN-GUI.

It is heavily based on the pattern for the input files used in NOIA for the creation of NoCs.

The first line represents the horizontal links between nodes, with each line in the NoC ending denoted by semicolon(;).
The second line represents the vertical links between nodes, with each column in the NoC ending denoted by semicolon(;).

The extra detail comes in the information store in each section. Before it was used only 0s and 1s to denote where there was a failure and where there was not.
Now, not only the number varies between 0 - 3, but also there is two numbers separated by a dot(.).
This signifies the protection level applied to each end of a link, since at each end of a link exists a buffer.

As an example here is a input file used in NOIA for a 5x5 NoC(the placement of 0s and 1s is random):

0 0 0 0; 0 0 0 1; 0 0 0 0; 0 0 0 0; 0 0 0 0; 
0 0 0 0 0; 0 0 0 0 0; 1 0 0 0 0; 0 0 0 0 0; 

And here is the input file used to implement the security in the buffers of a 5x5 NoC(the placement of the different securities is random):

0.1 0.2 2.3 0.0; 1.0 3.3 2.2 0.1; 1.1 0.0 0.0 3.3; 0.0 0.1 0.2 0.3; 0.0 0.0 0.0 0.0;
2.3 3.1 0.0 1.1 2.2; 0.0 0.0 0.0 0.0 0.0; 1.1 0.0 0.2 0.2 3.0; 0.0 1.1 0.1 0.0 2.2;

The different number between 0 - 4 signify:
0 - No protection
1 - Extended Hamming Protection
2 - Matrix Protection
3 - CLC Protection