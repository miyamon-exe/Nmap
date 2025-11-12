# Nmap

## よく使うオプション
-vv (詳細度を上げる)
-n (DNS 解決を行わない：これによりスキャン速度が上がる)高速化
-sn (ポートスキャンを行わない)
-F (通常1000ポートのところ100ポートのみスキャン）高速化
-O OSスキャン
-A (-O -sV -
-sV (servicenのver調査）
-oN filename(結果のファイル出力）
-sU (UDP scan)

## PING系
-Pn	:ping スキャンを完全に無効化
-PS	:TCP SYN (デフォルトはポート 80)
-PA	:TCP ACK (デフォルトはポート 80)
-PU	:UDP
-PY	:SCTP INIT
-PE	:ICMP エコー (Echo)
-PP	:ICMP タイムスタンプ (timestamp)
-PM	:ICMP アドレスマスク (mask)
-PO	:他 (Other) の IP プロトコル
-PR	:ARP スキャン


## host scan
sudo nmap -sn -n -v -T4 192.168.1.0/24　#PINGスキャンをなるはやで！
#ポートスキャンを行わず名前解決もせずに詳細を表示してデフォルトより早く実行する。


## port scan
sudo nmap -sS -n -v -T4 192.168.1.0/24


## 役立つかもしれないオプション
スキャンの対象から除外
$ nmap 10.1.1.1-10 --exclude 10.1.1.5,7 
