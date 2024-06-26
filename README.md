LOW-DOSE
https://github.com/yfzzzzz/Low_dose/blob/main/Low_dose.mlx

Overview
The code enables loading desired columns of secondary electron data from Excel documents. It retrieves secondary electron signals and separates them. Providing further analysis including curve fitting, exponential coefficients estimating, separating the area of each pulse, plotting, and making histograms.

Installation
To download and install MATLAB, Simulink, and other MathWorks products:

1\ Sign in to your MathWorks Account or create a new one.

2\ Download your products from MathWorks Downloads.

3\ Follow the prompts to install the products for which you are licensed.

If you do not have a license for MathWorks products through an organization, such as a university or company, you can buy products or request a trial from the MathWorks Store.

How it works
Locating the address of Excel files and producing a script that can be automatically generated by MATLAB. After successfully loading the data, ensures the names of variables are correct. Then just play the ‘run’ button.

Running an example
Here is an example of importing table format in two Excel files:

tb1 = readtable("C\Desktop\excel1.csv",opts);
tb2 = readtable("C\Desktop\excel2.csv",opts);
Then read the desired column with its name in the Excel. The code below ensure the time is positive and continuous:

Time_1 = tb1.Var1+abs(min(tb1.Var1));
Time_2 = tb2.Var1+abs(min(tb2.Var1))+max(Time_1);
Time_1 = tb1.Var1+abs(min(tb1.Var1));
Repeating import other desired columns:

V_beam = [tb1.Var1;tb2.Var1];
V_SEY = [tb1.Var2;tb2.Var2];
V_SIY = [tb1.Var3;tb2.Var3];
Bugs & Feature Requests
Please report bugs and request features using the Issue Tracker.
