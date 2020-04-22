# tec-tweet

# 概要
　簡単なつぶやきと、メモTODOリストとして使用出来る
 
# 本番環境
  デプロイ先　Heroku
  https://radiant-springs-14680.herokuapp.com/users/sign_in
 
# 制作背景
  紙媒体で保存するのではなく、デジタルでTODOリストやメモを保存出来るようにしたかった。
  仕事やプライベートの作業勉強の優先順位をつけるため、気軽にメモがわりに使用できるアプリを作成したかった。
  
# 工夫したポイント
  TODOリストやメモ機能を重視したため、デザインや色味はシンプルに作成。
  また、いつtweetしたか明確にしたかった。
  アナログでは不可能な画像も保存できる。
  
# 用技術(開発環境)
  Herokuにてデプロイ
  
# 課題や今後実装したい機能 
  削除機能を追加したい
  
# DB設計
  tweetテーブル
    belongs_to :user
    validates :text, length: { maximum: 140 }
    
  Userテーブル
    has_many :tweets, dependent: :destroy
  


