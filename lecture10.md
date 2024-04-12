# 課題10  
## 課題内容  
CloudFormationを利用して、現在までに作った環境をコード化  
コード化ができたら実行し、環境が自動で作られることを確認  

## 構造  
Network: VPC サブネット インターネットゲートウェイ  
Application: EC2 RDS ELB S3   
Security: セキュリティグループ  

## テンプレート  
[Network](Task10-CF/Task10-NetworkLayer.yml)  
[Application](Task10-CF/Task10-ApplicationLayer.yml)  
[Security](Task10-CF/Task10-SecurityLayer.yml)  
