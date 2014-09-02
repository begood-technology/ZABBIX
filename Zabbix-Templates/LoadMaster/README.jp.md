LoadMaster Template
===================

このテンプレートはZABBIXでLoadMasterのシステム統計情報やVirtualService、RealServerなどのディスカバリ(自動登録)、監視を行えるものです。
IPVS-MIBと B100-MIBを元に作成しています。

Items
-----
  * CPU: System / User / SoftIRQ / Nice / Interrupt / Idle
  * Load Average: 1min / 5min / 15min
  * Memory: Used / Shared / Buffer / Cached / Free / Total
  * TPS: TPS / SSL TPS
  * Connections: LoadMaster全体のコネクション数。
  * Total Virtual Services: LoadMaster全体のVirtualService数。
  * HA State: HAの状態.
  * Network Traffic: LoadMaster全体の送受信のトラフィック量。
  * Discovery: ネットワークインターフェースをディスカバリ。
    * 取得項目 Packets / Traffic / Interface Speed
  * Discovery: VirtualServiceのディスカバリ。
    * 取得項目 Active Connections / Connections / Traffic / State
  * Discovery: RealServerのディスカバリ。
    * 取得項目 Active Connections / Connections / Traffic / State

Triggers
--------
  * **[WARNING]** => HA State Change.
  * **[INFORMATION]** => Discovery: Virtual Service State is Disabled
  * **[INFORMATION]** => Discovery: Virtual Service State is In Service
  * **[INFORMATION]** => Discovery: Virtual Service State is Redirect
  * **[WARNING]** => Discovery: Virtual Service State is Sorry
  * **[WARNING]** => Discovery: Virtual Service State is Errormsg
  * **[HIGH]** => Discovery: Virtual Service State is failed
  * **[HIGH]** => Discovery: Virtual Service State is Out Of Service


Graphs
------
  * CPU Util: CPU使用率 (SNMPの仕様によりCPU数 × 100 %となります。2CPUの場合は 最大200%となります)
  * Load Average: ロードアベレージ。
  * Memory: メモリ使用率。
  * Connections: LoadMaster全体のコネクション数。
  * TPS: TPS / SSL TPS。
  * Total Virtual Services: LoadMaster全体のVirtualService数。
  * Total Network Packets: LoadMaster全体のパケット量。
  * Total Network Traffic (Bit): LoadMaster全体のトラフィック量(Bit/sec)。
  * Total Network Traffic (Byte): LoadMaster全体のトラフィック量(Byte/sec)。
  * HA State: HA状態( 1 = HA構成, 0 = 非HA構成またはシングル動作 )
  * Discovery: ネットワークインターフェースをディスカバリ。
    * 取得項目 Packets / Traffic / Interface Speed
  * Discovery: VirtualServiceのディスカバリ。
    * 取得項目 Active Connections / Connections / Traffic / State
  * Discovery: RealServerのディスカバリ。
    * 取得項目 Active Connections / Connections / Traffic / State

インストール
------------

1. LoadMasterのSNMP設定。
2. ZABBIXへロードマスターのホストを登録。
3. 登録したホストへSNMPインターフェースを登録
4. テンプレートインポート。
5. テンプレート適用。

要件
------------

 このテンプレートはZabbix Server 2.2 以降、LoadMasterバージョン 7以降でテストしております。
 このテンプレートを使用するにはLoadMasterにSNMP設定が必要です。

ライセンス
-------

 Released under the [MIT license](http://opensource.org/licenses/mit-license.php).

### Copyright

  Copyright (C) 2014 BeGoodTechnology Inc. All Rights Reserved.


