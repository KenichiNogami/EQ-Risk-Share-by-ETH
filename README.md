プロジェクト概要

このプロジェクトは、伝統的な保険では対応できないような巨大なリスクや未知のリスクに対し、特許を取得している非中央集権的なリスクシェアの仕組みでソリューションを提供するものです。
保険に加入できない高齢者の死亡リスクに加え、今回のハッカソンに応募した巨大地震リスク、原子力事故リスク、空き家リスク、認知症のリスク、パンデミックのリスク、ハリケーンリスク等も対象にしていく予定です。

基本的仕組みは、助け合い精神に則り、参加者が拠出した資金をプールし、リスクが発生した時に対象者で資金をシェアするものです。保険の源流の仕組みに近いものになっています。

原子力事故などは、日本国内だけでシェアするのはリスクマネーが不足しているため不可能です。このプロジェクトを世界に広げていく必要があります。

現在、世界的に人々が対立し、分断しようとしていますが、このプロジェクトの実現を通じて、人々のコミュニケーションを活発にし、世界の人々が助け合うことによってより良い世界の実現に貢献したいと思っています。




Smart Contractの説明（日本語）

このスマートコントラクトは、グローバルな再保険会社が引き受けるには大きすぎる、グローバルな地震リスクをシェアするために使用されます。
言い換えれば、これはretrocession市場の非中央集権的代替です。
また、現在の中央集権的なretrocession市場ではカバーできないレベル7の原子炉事故もカバーしています。

このスマートコントラクトは、日本と米国に拠点を置く inSharerance Co の特許に基づいています。
この契約は、地球上で年間平均約13回発生するマグニチュード 7/+ の地震を対象としています。これらの大地震は4つのスレッドに分類されます。

Level_4 10000 人以上の死者または深刻な(カテゴリ7) 原子炉事故（理由を問いません。戦争による事故を含む）。 
Level_3 1000 ～ 9999 人の死亡 
Level_2 100 ～ 999 人の死亡 
Level_1 0 ～ 99 人の死亡

リスクシェアリングはラウンドごとに実行されます: ETHネットワークの２００,000ブロックが１ラウンドになります。 約365.24/13 日
新しいユーザーは、次のラウンドからリスクシェアリングに参加しなければなりません。
言い換えれば、現在の実行中のラウンドからではありません。
それまでに、0.01*n ETH のプレミアムを支払い、地震のスレッドを選択する必要があります。
ラウンド中に地震・原子炉事故が発生しなかった場合、保険料は全額次のラウンドに繰り越されます。
次のラウンドに繰り越されたETHは新しい参加者とのリスク共有に使用されます。
キャンセルの場合の返金はございません。
手数料/リスクマージンはありません。すべてがリスクシェアに使用されます。
ただし、ETH ネットワークにはガスが必要です。
運営のための寄付等よろしくお願いします。

マグニチュード7以上の地震等が発生した場合、支払われたすべての保険料は、その特定のスレッドを選択した参加者によって共有されるものとします。
複数の地震が発生した場合、資金は最も深刻なレベルの参加者によってのみシェアされるものとします。
例えば。 Level_1 と Level_4 の地震が発生した場合、Level_4のみによってシェアされます。

スマートコントラクト「riskShare」には、ユーザー向けの2 つの関数があります。

1 buy 

INPUT:(#買いたいラウンド、#カバーしたいレベル。)
レベル 1 と 4 でラウンド 20 と 21 を購入する場合は、4 つのメッセージを送信する必要があります。 
buy(20,1), buy(20,4), buy(21,1), buy(21,4) 
さらに、プレミアムのために ETH=n*0.01 HTH を追加する必要があります。 n は正の整数です。

2 claim 

INPUT:(主張したい#round)ラウンド 
20 と 21 を請求する場合。 
claim(20), claim(21)

その他の詳細事項はプログラムの通りです。両者に矛盾がある場合は、プログラムが優先されます。





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



