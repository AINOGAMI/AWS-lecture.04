- VPCと一緒にサブネット作成。VPCは家の外壁、サブネットは部屋と部屋の仕切りのイメージ。

<img width="1454" alt="VPC" src="https://user-images.githubusercontent.com/113970809/202839814-5d086751-5311-415c-b6c6-d2610c5cd98c.png">





- EC2作成。EC2は外部とつながるネットワークなので、応接室みたいなイメージ。キーペアの確実な保存と料金に注意。
<img width="1445" alt="EC2" src="https://user-images.githubusercontent.com/113970809/202839849-aaef48b5-601d-43da-abe8-19489311f135.png">





- RDS作成。RDSは構成図を家に例えると、外部と接続してないので寝室みたいなイメージ。
<img width="1447" alt="RDB" src="https://user-images.githubusercontent.com/113970809/202839909-3357747a-7cd2-4271-9416-6dddc765c5fd.png">






- EC2をSSHに接続。EC２のコンソールの「接続」と言うところにコマンドが書いていた。最初の設定をミスしなければ上手くいく。
- chmod 400 キーペア.pem.   
- ssh -i "キーペア" ec2-user@パブリックIP
- ＜参考サイト＞　https://qiita.com/takuma-jpn/items/b2c04b7a271a4472a900
<img width="885" alt="ECをSSHに接続" src="https://user-images.githubusercontent.com/113970809/202839992-eb9e7454-8d7a-4766-be70-4af4cb69f478.png">








- EC2とRDSを接続。まずはSSHでMySQLをインストールする。
- mysql -u admin -p -h ＜RDSのエンドポイントを張り付け＞でRDSのパスワード入力で完了。
- ＜参考サイト＞https://dev.classmethod.jp/articles/sales-rds-ec2-session/
<img width="1338" alt="EC2とRDB接続" src="https://user-images.githubusercontent.com/113970809/202840096-d8975578-fa62-4a5f-8395-e2970cfed382.png">
