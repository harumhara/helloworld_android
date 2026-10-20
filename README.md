# helloandroid_android  

## Android Studioという開発環境を使って『Hello Android!』アプリを作ってみる  

### Hello Android!アプリの作成  
+ 手順
    1. Welcome to Android Studioの画面からNew Projectを選択
    2. ProjectタイプからEmpty New Activityを選択
    3. projectの設定画面に遷移

+ projectの初期設定
    + Name:何でもOK（今回はTestApp001と設定しました）
    + Package name:そのまま（今回の場合はcom.example（←個人によって異なる）.testapp001）
    + Language:そのまま（JavaかKotlinで選択可能.今回の場合はkotlin）
    + Minimum SDK:そのまま（今回の場合はAPI24）
    + ※Minimum SDKとはアプリが動作をサポートする最低限のAndoroid OSバージョン（APIレベル）のこと.
    + ※数値を低くすると古いスマホを持つユーザでもカバーできる.端末対応が可能.
    + ※数値を高くすると新しいAPIやモダンな機能を利用しやすくなる.
    + 最後にFinishを押す → プロジェクトが作成される！

+ エミュレータで実行する
    + エミュレータとはパソコンの画面上にAndoroidの仮想のスマートフォンやタブレットを再現し,開発したアプリをテスト・実行できるソフトウェアのこと.
    + 手順
        1. 左上の4本線 → Tools → Device Managerを選択
        2. どの機種を使うか選択する（今回はSmall Phoneにしました）
        3. エミュレータを選択し緑の▷アイコンをクリックして実行「Run 'app'」
        4. Hello Android!と表示される
