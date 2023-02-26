     
## Setup when bootstrapping using my own node

- run a first node 

      ./node -l 9000
      
      2020/05/19 06:43:13 My ID is : Qme1tMLGtBfbWibguT8VaKdPdLgVrtrs6xW1mSHM6KpdkH
      2020/05/19 06:43:13 I can be reached at:
      2020/05/19 06:43:13 /ip4/127.0.0.1/tcp/9000/p2p/Qme1tMLGtBfbWibguT8VaKdPdLgVrtrs6xW1mSHM6KpdkH


- run a second node with the first node as bootstrap (use one of its multiaddrs)
      
      ./node -l 9001 -b /ip4/127.0.0.1/tcp/9000/p2p/Qme1tMLGtBfbWibguT8VaKdPdLgVrtrs6xW1mSHM6KpdkH
      
      2020/05/19 06:43:13 My ID is : QmQacZT1cWoaYV4oUwaRduj4Kdt6JUEzTqX5M82AJD3REf

      
- run a third node with the first node as bootstrap, and instruct it to dial the second node
      
      ./node -l 9002 -b /ip4/127.0.0.1/tcp/9000/p2p/Qme1tMLGtBfbWibguT8VaKdPdLgVrtrs6xW1mSHM6KpdkH -d QmQacZT1cWoaYV4oUwaRduj4Kdt6JUEzTqX5M82AJD3REf
      