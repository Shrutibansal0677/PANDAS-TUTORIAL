import pandas as pd
import numpy as np
df=pd.read_csv('C:/Users/Vansh Bansal/Downloads/fb.csv', index_col=['Date'])
df
df.shift(1)
df.shift(5)
#to have 5 day percentage change

df['5 day % chnage']= (df['Price']-df['Price'].shift(5))*100/df['Price'].shift(5)
df
# to shift dates

df.index
df.index=pd.DatetimeIndex(df.index)
df.index
df.index=pd.date_range(start='2017-08-15', end='2017-08-28', freq='B')
df.index
df.tshift(1)
