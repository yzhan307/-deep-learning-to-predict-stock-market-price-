Load data from the “ HW1_DATAuse” file. It includes eight stocks prices from Chinese Stock Market.
Eight data sets (1st_stock.csv, 2nd_stock.csv, …, 8th_stock.csv) were selected for this homework project. Each data set has 240 rows and 896 columns. 240 rows are 240 prices recorded every minute per day, 896 columns represent 896 days. 
Read the 8 data sets in the list A. A[0], A[1], A[2], A[3], A[4], A[5], A[6], A[7] corresponding to  8 stocks. List A includes 8 numpy arrays, and each array has 240 rows and 896 columns. Each A[j] has 896 days, t=896,and A[j](t)  is the sequence of day t prices recorded every  minute. 
These 8 market price data have relative low percentage of missing values( shown as NAN in excel) comparing to other data available in the Chinese data set. 
Denote data set B the closing price of asset Aj. (B=A[j][-1]), B has 8 arrays, each B[j] is the closing price of A[j] on day t. B[j] has 896 days closing prices of stock j.
In this homework, on day t, we concatenated all 8 line vectors Aj(t) into a long line vector A(t) = [A[0](t), … , A[7](t)]. Each line vector A(t) has dimension of 8*240 = 1920. On day t  we want to use the known 3 long line vectors { A(t) , A(t-1),  A(t-2) } to  predict  the still unknown target vector Y(t) = [B1(t+1), B2(t+1), B3(t+1), B4(t+1), B5(t+1)].

Question 0: Graphic displays
Q0 part 1:
Dataset B is the closing prices for 8 stocks in 896 days. Select 5 stocks’ closing prices that we want to predict B1, B2, B3, B4, B5. Then normalized their values nBj = Bj(t)/Bj(1). Plot 5 curves to display the time evolution of the five closing stock prices nB1~nB5 . We can get better readability of the graph, when we use the normalized values nBj to display the graph. Use the function(plt.plot()) to display the 5 stocks which we want to predict in this homework.Their closing prices in 896 days are shown as below.
