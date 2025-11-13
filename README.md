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


<h2>built-in functions:</h2>


<h1>class2 code examples for graphs and plots:</h1>
<pre>
  The following commands were saved in an M-file:
% a)
t1 = -8:-4; x1 = zeros(size(t1));
t2 = -4:3; x2 = t2+2;
t3 = 3:8; x3 = t3-2;
t = [t1 t2 t3];
x = [x1 x2 x3];
subplot(221),plot(t,x)
xlabel(’Time (sec)’)
ylabel(’x(t)’)
title(’a)’)
% b)
t = t+1;
subplot(222),plot(t,x)
xlabel(’Time (sec)’)
ylabel(’x(t)’)
title(’b)’)
% c)
n1 = -6:1; x1 = zeros(size(n1));
n2 = 2:3; x2 = 2*n2-4;
n3 = 4:8; x3 = 4-n3;
n = [n1 n2 n3];
x = [x1 x2 x3];
subplot(223),stem(n,x)
xlabel(’n’)
ylabel(’x[n]’)
title(’c)’)
% d)
n = n-1;
subplot(224),stem(n,x)
xlabel(’n’)
ylabel(’x[n]’)
title(’d)’),subplot(111)
</pre>


<pre>
Here is an M-file that contains the script to plot generate these plots:
% a)
% period is 2/5, so 2 sec is long enough for plot
t = 0:.4/100:2;
x = 4*cos(5*pi*t-pi/4);
subplot(2,2,1),plot(t,x)
xlabel(’Time (sec)’)
ylabel(’x(t)’)
title(’a)’)
% b)
% period is n=2, so plot for n=0 to 10
n=0:10;
x = 4*cos(pi*n);;
subplot(2,2,2),stem(n,x)
xlabel(’Time (sec)’)
ylabel(’x[n]’)
title(’ b)’)
% c)
% not periodic, try plotting for various lengths to see how it looks
n=0:60;
x = 2*sin(3*n);;
subplot(2,2,3),stem(n,x)
xlabel(’Time (sec)’)
ylabel(’x(t)’)
title(’c)’)
% d)
% period is 2pi/4, so plot for 4 cycles
T = 2*pi/4;
t = -T:T/50:3*T;
x = cos(4*t)+2*sin(8*t);
subplot(2,2,4),plot(t,x)
xlabel(’Time (sec)’)
ylabel(’x(t)’)
title(’d)’)
% e)
% not periodic, see how it looks for various lengths
t = 0:.02:20;
x = 3*cos(4*t)+sin(pi*t);
figure(2) % opens new window
subplot(2,2,1),plot(t,x)
xlabel(’Time (sec)’)
ylabel(’x(t)’)
title(’e)’)
subplot(1,1,1)
  
</pre>

