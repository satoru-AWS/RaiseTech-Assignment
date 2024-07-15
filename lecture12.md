# 課題12  
## 内容  
CicleCIの[サンプルコンフィグ](sample-config.yml)を使用して、正しく動作するようにリポジトリに組み込む。  
>[!NOTE]  
>cloudformation/*.ymlを自分のディレクトリ名に変更する  
>cloudformation/*.yml→Task10-CF/*.yml  
## 処理結果  
### エラーの発生 
<dl> 
 <dt>エラー内容</dt>
 <dd>1. RDSのパスワードを動的参照にすること</dd>
 <dd>2. プロパティの誤り</dd>
</dl>  
<details><summary>参考画像</summary>
  
```rb
![エラー](img3/lecture12-1.png)
```
</details>  

### エラーの解消  
エラー内容を解消後、再度CircleCIを実行  
![成功](img3/lecture12-2.png)  
## 所感  
当初テストの自動化という意味が理解できなかったが、実際にCircleCIを実行することで非常に便利なツールであると驚かされた。また、それと同時に自らが作成したCloudFormationの記述コードの誤りが非常に多く発見されたことに少しショックであった。また、ハードコーティングやパスワードの動的参照も指摘されたことでセキュリティの観点からも非常に有用であると感じた。