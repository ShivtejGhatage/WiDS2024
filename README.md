# WiDS2024_Investron

## Description
Investron is a digital stock-picking assistant that scans the market each day to find the best stocks to buy and sell. It uses a model called LSTM, which can recognize patterns in past prices to predict which stocks are likely to rise. Investron checks specific indicators like MACD, RSI, Bollinger Bands, and Fibonacci levels for clues on market behavior. Based on these, it buys the two stocks it thinks are likely to go up the most and sells anything it's holding to free up funds. Running on a mock investment of 100,000 rupees over two years, it ended up with a total of about 158,000 rupees, showing a solid gain without using real money.

## Week 1 Resources


[Python in 1 Hour](https://www.youtube.com/watch?v=kqtD5dpn9C8)


[Introduction to Numpy](https://www.youtube.com/watch?v=QUT1VHiLmmI)


[Introduction to Pandas](https://www.youtube.com/watch?v=vmEHCJofslg)


[Introduction to Stock Market](https://www.youtube.com/watch?v=yzRP-mA2eiE&list=PLX2SHiKfualH_xMbGM-3zWC47s9gUjGR_)

## Week 2 and 3 Resources

[Matplotlib](https://www.youtube.com/watch?v=DAQNHzOcO5A)
(Can learn Plotly as well which is just interactive Matplotlib)
(Just understand the basics, Even the docs can help you plot your graphs)

[TVDatafeed](https://github.com/rongardF/tvdatafeed?tab=readme-ov-file)
This is the library to fetch your data. 
Just install it the way the repo says.
All it takes to fetch is the tvdatafeed object and then run the below command

            tv = TvDatafeed()
            df = tv.get_hist(symbol="ADANIPORTS", exchange="NSE", interval=Interval.in_daily, n_bars=10000)


[The Longer way (The first two courses)](https://www.coursera.org/specializations/machine-learning-introduction)
(If you apply for a financial aid, you can get some certificates for your resume)
A good teacher but an easy course. Would recommend to watch in 2x

[The Shorter Way](https://www.youtube.com/watch?v=zxagGtF9MeU&list=PLblh5JKOoLUIxGDQs4LFFD--41Vzf-ME1)
Watch upto video 16


## Week 4 

Build the bot. You are expected to try out different features(Indicators). We recommend making a bot that makes day to day trades. You can try to classify whether the price of a stock would go up or down. You can also try to predict the percentage change in the stock price (Recommended). After you get satisfactory results you need to find ideas with what to do with your predictions. You have to get creative with the buy and sell strategies of your bot. An elementary example is buying the highest percentage predicted stock with half the money (To reduce risk). We are giving you the time to have fun with this.

### Just to make things Interesting
   While making your bot, train it on anything but the latest 500 candles. This will serve as your testing set. Run your bot on this giving it 100000 as initial investment (we are taking about fake money here) and figure out how much total money it has made. Calculate your CAGR (500 stock candles days is 2 years) and we will rank the top mentees with their CAGR.

To be eligible for the certificate we expect a LSTM ( or decision trees or anything ) based bot with a working simulation with the MockBroker class.
(Just a simulation, Not something deployed on the market)

( Resources to actually deploy your bot on the stock market will be released later and we dont expect this part for the certificate)


## Assignments
We wont be checking the assignments but you are expected to do them as steps to build your project.

Use only NIFTY50 for the following

1. Fetch data using tvdatafeed and implement buy and sell positions. Save the csv files for all 50 stocks. Calculate the MACD for each row entry (Not the first 26 days) and use the signal line to generate buy and sell signals. Add a column to the stocks named position with has these integers -1 to sell, 0 to hold, 1 to buy. You are encouraged to try out other stock market indicators to generate buy and sell signals as well. The csv for each stock at the end should have the columns open, high, low, close, MACD,RSI,position along with other indicators you wish to use.
2. Make a MockBrocker python class. The MockBroker class is like a fake stockbroker. It maintains your holdings and balance as attributes. It should have the methods of buy and sell which should get reflected in the attributes it holds. Printing it using \_\_str\_\_ should give you your balance, holdings and networth(balance + value of holdings). It should have the arguments of Balance (the initial investment) and a price dictionary which has the symbol name as key and the list of everydays closing price as value. You can use the csvs you saved in assignment 1 to make this price dictionary. We will share our MockBrocker class at the end of this.
3. Figure out features to use, make a neural network and implement with the MockBroker ( You might not get promising results with a neural network, but try it out). (Tensorflow is recommended)
4. Week 4 Final Project.


