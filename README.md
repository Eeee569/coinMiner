# coinMiner
#3 objects, a sender, recorder and a trader
#sender:
#   -becuase kraken has a request timer this will have a weighted queue of requests to be sent on a timer
#    trading requests are higer on the queue
#    for testing a trading request will just get the current price and fill the order
#   -in a seperate thread
#recorder:
#   -has a queue of actions
#   -hold array of all curency currently being recorded
#   -update array when new currency needed
#   -update all currency in array at different time intervals( smallest possible to a set max) and store in some file
#   -return a currency pair when asked for
#       -rturns all data recorded so far
#
#   -in seperate thread
#trader:
#   -hold only two currencies and amouunt held of two currencies
#   -hold  all data comparing two currencies
#   -functions that determin short term mid term longterm... profitabiliteis of trading and if determined profitable then trade currencie
#   - the current trader will just test the profitablility functions so each function will have its own amount of each currency and
#   -end of day function will determin the most profitable moments of the day/ month/... and return which function was profitable
#     trade between the two
#       -a trade should have a range of values to accept as a trade
#   - in own thread
#   - when getting