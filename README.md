# MATLAB2025-1
Learming Matlab - https://matlabacademy.mathworks.com/details/matlab-onramp/gettingstarted

You can save variables in your workspace to a MAT-file, a file format specific to MATLAB, by using the save command.
For example, to save all the variables in the workspace to a MAT-file named filename.mat, use the command:
>> save filename

Empty the workspace using the clear command.

Clear the Command Window using the clc command.

When you close MATLAB, it clears the workspace. Before closing MATLAB, you can use MAT-files to save your variables. You can then load the variables into the workspace when you reopen MATLAB.
To load or save only some of your variables, you can use additional inputs with the commands.
The provided file myData.mat contains multiple variables. Try loading just the variable k.
>> load myData k
Then try saving the variable k to a new MAT-file named justk.mat.
>> save justk k
