# pandas_tricks

1. Shift pandas dataframe down in a cyclical manner
   a)you can combine reindex with np.roll:
      X = X.reindex(np.roll(X.index, 1))
   b) Another option is to combine concat with iloc:
      shift = 1
      X = pd.concat([X.iloc[-shift:], X.iloc[:-shift]])
