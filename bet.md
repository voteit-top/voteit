# introduction
The Bet game is based on smart contract of TRON network. it can only use VOTEIT to bet. to simplify the logic, we currently support only a few modes.
but all modes are 100% fair in a mathematics point of view. Unlike traditional casino games, which seeks to win profit.this is only for fun, for increasing liquidility of VOTEIT,good luck :)
# what to bet?
Block ID (block hash) of future block.like:"blockID":"0000000001a6b073cab4f0fe90d687c50dfeab80e56d889480c0071c351f4ba3". you can get lastest block by accessing: https://sun.tronex.io/wallet/getnowblock

all bet modes are based on the last 5 characters of Block ID, we name it as L5BID for easy description. While you are reading this, the block number keeps increasing, you cannot bet on existing block, you can only bet on future block.
## Support modes
L5BID (last 5 characters of block ID)
1. ODD  means L5BID is ending with characters:(1,3,5,7,9,b,d,f)
2. EVEN  means L5BID is ending with characters:(0,2,4,6,8,a,c,e)
3. TWIN-D means L5BID is ending with Two identical contiguous characters.(eg:aa,11,00,33)
4. TRI-D means L5BID is ending with three identical contiguous characters.(eg:bbb,aaa,000,666)
5. QUA-D means L5BID is ending with four identical contiguous characters.(eg:bbbb,aaaa,2222,3333)
6. FIVE-D means L5BID is ending with five identical contiguous characters.(eg:eeeee,aaaaa,22222,33333)
## Probability and odds
we assume L5BID is random completely.
1. ODD: 1/2, so bet 1 win 2
2. EVEN: 1/2, so bet 1 win 2
3. TWIN-D: 1/16, so bet 1 win 16
4. TRI-D: 1/256, so bet 1 win 256(rare)
5. **QUA-D**: 1/4096, so bet 1 win 4096 (very rare)
6. **FIVE-D**: 1/65536, so bet 1 win 65536(extemely rare)

eg: if you bet TWIN-D with amount 1 VOTEIT, if you win, you will get 16VOTEIT. 

## what is 'Batch'?
instead of beting on only one block, 'batch' help you bet multiple contiguous block with same strategy.so far, the max acceptable batch is 5.
## how it works?
1. you must specify your bet amount of VOTEIT.
2. you must opt for mode to bet.
3. specify Batch(default:1, max:5)
4. commit your bet via tronlink.
5. wait for your block to come.
6. check bonus if you win.(**if you dont check, you will lost your reward**)
7. if you dont win, 'check bonus' will clear your bets.

NOTE: your bet wont be bound with block where you commited.but it will be bound to next 1~5 blocks to avoid cheating.
## how about blockhash cheating? 
In TRON network, SR has the ability to change blockhash when it package transactions in theroy. but as you know there are 27 SRs to package transactions in turn. let's think several facts:
1. if SR do the fact of manipulating blockhash, that will lost his credibility.
2. normal users cannot control SR.
3. Even as a SR, he cannot guarantee his bet will be bound to the block which will be assigned to him to package.
4. gain is not so bigger than lost. 

so, our conclusion: blockhash cheating is possible, but it will not happen.
## check bonus
Due to technical limitation,  the contract cannot transfer bonus automaticly. so user have to claim bonus when the block number arrives.
if use doesn't claim bonus in 255 blocks,  **you bonus will lost**. 
usually, VOTEIT webset will show you the result of your bets. the button will beat, you should click 'check bonus' to claim your bonus.
but if expericing network timeout, the results may not be updated in time. in this case, you needn't wait the button to beat, you can click the 'check bonus' button when your betted block number arrives. (3 seconds/block in tron network)

