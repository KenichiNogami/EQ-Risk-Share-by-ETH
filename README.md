プロジェクト概要

このプロジェクトは、保険では対応できないような巨大なリスクや未知のリスクに対し、特許を取得している非中央集権的なリスクシェアの仕組みでソリューションを提供するものです。
保険に加入できない高齢者の死亡リスクに加え、今回のハッカソンに応募した巨大地震リスク、原子力事故リスク、空き家リスク、認知症のリスク、パンデミックのリスク、ハリケーンリスク等も対象にしていく予定です。

基本的仕組みは、助け合い精神に則り、参加者が拠出した資金をプールし、リスクが発生した時に対象者で資金をシェアするものです。保険の源流の仕組みに近いものになっています。

原子力事故などは、日本国内だけでシェアするのはリスクマネーが不足しているため不可能です。このプロジェクトを世界に広げていく必要があります。

現在、世界的に人々が対立し、分断しようとしていますが、このプロジェクトの実現を通じて、人々のコミュニケーションを活発にし、世界の人々が助け合うことによってより良い世界の実現に貢献したいと思っています。


Smart Contractの説明（日本語）





Smart contract Overview


This contract shall be used for sharing global earthquake risk, which is too large for global reinsurers to take.
In other words, this is the decentralized replacement of retrocession market.　
Additionally this also covers nuclear reactor accident of level 7, which current centrarized retrocession market can not cover.  

This smart contract structure is based on patents of inSharerance　co, based in Japan and USA.
This smart contract covers earthquakes of magnitude 7/+, which occur around 13 times on average per year on the globe.
These big earthquakes are categorized into 4 threads;

   Level_4 10000/+ people deaths or severe(level 7) nuclear reactors accidents (by any reason including war).
   Level_3 1000 to 9999 deaths
   Level_2 100 to 999 deaths
   Level_1 0 to 99 deaths

Risk sharing is executed every round: 200,000 blocks of ETH network, which is round 365.24/13 days
New users shall participate risk sharing from the next round. In other words not from current runnning round.
By then, they must pay premium of 0.01*n ETH and choose (one) thread(s) of earthquake.
If no earthquake/nuclear reactor accident occurs in the round, all premium shall be carried forward to the next round.
In the next round this will be used for risk sharing with new participants.
There is no payback in case of cancellation. There is no fee/risk margin. Everything is used for risk sharing.
But gas is required by ETH network to operate this smart contract. Your donation etc. are very appreciated. 
If magnitude 7/+ earthquake(s) occur, all paid premiums shall be shared by those participants who chose that specific thread.
In case more than 1 earthquakes occurred, the fund shall be shared only by the most severerest level participants.
E.g. if Level_1 and Level_4 EQ occurred, the fund shall be shared only by the Level_4.

In the smart contract "riskShare" there are two functions for users;

1 buy
  INPUT:(#round you want to buy, #level you want to be covered.)
  e.g. If you want to buy round 20 and 21, on Level 1 and 4. You must send 4 messages.
      buy(20,1), buy(20,4), buy(21,1), buy(21,4)
  Additionally you must add some ETH=n*0.01 HTH for premium. n is positive integer.  
  

2 claim
  INPUT:(#round you want to claim)
    e.g. If you want to claim round 20 and 21.
      claim(20), claim(21)
  
Other detail matters are as smart contract. This notation is only for your reference use. If there is a contradiction between the two, smart contract takes precedence.



