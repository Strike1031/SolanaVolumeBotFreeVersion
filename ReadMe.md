# This is an only free version.
New version is updated.
========================Project Plan & Algorithms==============================:
   - create admin wallet, and admin deposit ETH to this address. (app should wait while its' ETH balance > 0)
   - Ask User -> For only volume  OR  Increasing Holders? -- Y or N
      Y) create random 20 wallets and auto, buy and sell.
      N) 
      - First Stage - create random 10 wallets first, admin will send random ETH to these 10 address
      - Second Stage - In 10 random wallets, each wallet send random ETH to new 10 random address..
                      So, total supply of accounts: 10 * 10 = 100
      - First buy:
           In 100 accounts, each account swap 30% of its ETH balance to <token>
      - While (auto Buy OR  Sell)
           <1> Sell
              - tokenBalance == 0 ? swapETHToToken( 30% ETH to token)
              - RiseHolders = true? swapTokenToETH (80% token to ETH) & sendETH(newWallet)
              - RiseHolders = false? swapTokenToETH(100% token to ETH) & sendETH(new Wallet)
          <2> Buy
             swapETHToToken(30% ETH)
       
           time.sleep(60) // wait for 60 seconds
       :: newWallet LOOP to while
