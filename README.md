java c
School of Accounting, Economics and Finance
EXAMINATION
Semester 2, 2024
INVE6000 Investments and Fund Management
Section A: SAS exercise (A total of 13 marks)In this SAS exercise, you will examine how various variables influence the alphas of mutual fund portfolios. To do this, you will select 5 mutual funds (portfolios) of interest, check the data of the mutual funds selected, import Fama-French factors, estimate the alphas, merge the datasets and conduct a regression analysis.
In this exercise, you will utilize a SAS dataset of mutual fund portfolio holdings, named “Mutual_Fund.sas7bdat”, which includes information on the stocks held by various mutual funds from 2001 to 2005. In addition, you will work with a monthly stock file titled “Monthly_Stock.sas7bdat”, covering the period from 1996 to 2005. You will also have access to a CSV file named “FF5_202407.csv,” which includes the data for Fama-French 5 factors.
Please select 5 mutual fund portfolios using the portfolio identifier (variable name: CRSP_PORTNO) from “ Mutual_Fund.sas7bdat” . Make sure all those 5 portfolios end with the same last digit as your student ID. For instance, if your student id is 12236718, you may  select a mutual fund portfolio with CRSP_PORTNO as 1001618, and you should select a total of 5 such portfolios.
For those 5 selected mutual fund portfolios, do the following steps to complete the task:
Step 1: Check the portfolios [1 mark]
Please provide the CRSP_PORTNO (the identifier for the portfolio/mutual fund) for the 5 mutual funds you have selected. Additionally, indicate the number of observations for each mutual fund in your sample. Fill in the required information in the table below.
CRSP_PORTNO
# of observations










Step 2: A closer look at the data [2 marks]
For the 5 mutual funds you have selected, please indicate how many observations have a missing PERMNO (the identifier for individual stocks) for each fund. Additionally, specify the total number of unique stocks held by each mutual fund. Fill in the information in the table below.
CRSP_PORTNO
# of observations
with PERMNO missing
# of stocks with different PERMNOs















Step 3: Prepare the Fama-French factors [1 mark]
The Fama-French 5-factor data (“FF5_202407.csv”) is downloaded from Kenneth R. French’s website:http://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html .
Please import the data from CSV file into SAS.What are the 2 additional factors beyond the Fama-French 3 factors we have introduced in  this unit? How are these 2 additional factors calculated? Please provide a brief explanation. Hints: You may find relevant information from Kenneth R. French’swebsite.
Step 4: Estimate the alphas [3 marks]
Using the monthly stock returns data (Monthly_Stock.sas7bdat), calculate the Fama-French 3-factor alpha for each firmin each month from 2001 to 2005. Ensure that the betas are saved only for firms that have at least 48 non-missing observations in the regression.
Step 5: Merge the datasets [3 marks]
Please map the Fama-French 3-factor alphas you have calculated in Step 4 to the holdings data of the 5 mutual funds you have selected. Please make sure that the alpha corresponds   to one month ahead of the mutual fund holdings data. For example, if the mutual fund stock holdings data is from January 2002, map it to the alpha from February 2002.


Step 6: Check the data again [1 mark]
Using the merged dataset from step 5, please find the maximum, minimum, mean, and median values of the alphas for each of the 5 selected mutual fund portfolio. Fill in the table below with the resulting data.
CRSP_PORTNO
Alpha_FF3
Max
Min
Mean
Median

























Step 7: Run the regression [2 marks]
Run a regression using the model below:
Alpℎat+1  = β0  +  β1  × RANkt  +  β2  × PERCENTt  + β3  × NBRt
Where,
•   Alpha is the Fama-French 3-factor alpha you obtained from Step 4.
•    RANK refers to the variable SECURITY_RANK.
•    PERCENT refers to the variable PERCENT_TNA.
•    NBR refers to the variable NBR_SHARES.
Please make sure the standard error is clustered at the mutual fund level. Briefly interpret the results of the regression.




Section B: QA questions (atotal of 12 marks)
Question 1 [4 marks]
Sam is doing a tutorial question about calculating a mutual fund’s net asset value (NAV).
The composition of Vangarp Fund portfolio is as follows:
Stock
Number of Shares Holding
Share Price
A
10代 写INVE6000 Investments and Fund Management Semester 2, 2024R
代做程序编程语言0,000
$26
B
350,000
$18
C
260,000
$35
D
700,000
$5.96
The fund has not borrowed from any other funds. However, the fund has liabilities totals at $45,000. As the fund finished its IPO process 5 years ago, there are currently 3.5 million shares outstanding. What is the net asset value (NAV) of the fund?
Sam’s answer is as following:
The stock value held by the fund:
100,000 * $26 + 350,000 * $18 + 260,000 * $35 + 700,000 * $5.96 = $22,172,000
So, the NAV for the fund is:
NAV = ($22,172,000 - $45,000) / (100,000 + 350,000 + 260,000 + 700,000) = $15.6929
1) Whether Sam’s calculation is corrector not? Please briefly explain. [1.5 marks]
2) What information is required for a fund accountant to calculate the NAV of a fund? Where can the information be sourced from?  [1.5 marks]
3) Instead of holding stocks and bonds that are most probably actively traded on financial markets, the mutual fund could also hold some infrequently traded investments (e.g., collateralized mortgage obligation). Briefly explain the valuation procedures for those investments. [1 mark]




Question 2 [4 marks]
Below is a picture obtained from module 4 of our lecture notes:

The graph showshow financial institutions transfer loans into different tranches of securities via the special purpose entity. In this manner, financial institutions transfer loans into securities and sell them to different classes of investors. Every month homeowners make principal and interest payments to the loan, and the cash flows will transfer to the investors who purchased different tranches of securities. Bond funds could be the potential investors of securities in Tranche A to D.
We focus on Tranche A, B, C and D in this picture. Securities of Tranche A has a face value of $100 million and pays 5% interest annually to investors. Tranche B hasa face value of $200 million and the interest is 7% per year. Tranche C has a face value of $150 million and the interest is at 9% annually. Tranche D has a face value of $180 million and the interest is 11%  per year. To simplify the question, we assume payments of cash flows are made only once in ayear.
1) If at the end of the first year, investors of different tranches receive total cash flow of $60 million, determine how the cash flow is distributed among different tranches. [1.5 marks]
Hint: Interest payments of different tranches will be paid first in every year. Then the principal will be paid to Tranche A first. After all the face value of Tranche A has been paid (which could last for more than several years), the principal payment will continue to Tranche B. The process will continue and after all the principals been paid to B, then goes to C, and soon to D. That’s why in the picture above, Tranche A has the highest rating with lowest return as it is the safest portion with the priority of principal payment, and Tranche D has the lowest rating with highest interest rate as it is very risky.


2) If in the second year, investors of different tranches receive a total cash flow of $67 million, how are they distributed among different tranches? [1.5 marks]
3), Suppose we are at the start of the 10th year and Tranche A has 5 million principal outstanding. Investors of different tranches receive total cash flow of $65 million. How will the cash flows be distributed among different tranches? [1 mark]
Question 3 [1.5 marks]What are the risks associated with investing overseas? Please provide a brief explanation of  each. As an Australian investor, do you think the potential benefits would outweigh the risks of investing overseas? Any reason for this?
Question 4 [1.5 marks]
A leveraged ETF is an exchange-traded fund (ETF) that uses debtor derivatives as leverage   to amplify the returns of a benchmark index. Leveraged ETFs can generate significant short- term gains/losses, often achieving 2x or even 3x the daily performance of the underlying benchmark index. For instance, a 2x leveraged ETF on SP 500 index, can have 2x the daily performance of SP 500 index. I.e., if SP 500 index gains 1% in one day, then the 2x leveraged ETF will gain 2%; similarly, if the SP 500 index loses 1% in one day, then the 2x leverage ETF will lose 2%.Now assume the SP 500 index gains 10% in the next year; do you expect the corresponding 2x leveraged ETF will increase by 20% within the sametime period? Why? If needed, a brief numerical example may help.
Question 5 [1 mark]
What are the pros and cons of incorporating performance fees into fund management structures? Please provide a brief explanation of two advantages and two disadvantages.




         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
