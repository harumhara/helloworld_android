# helloworld_android  

## Android Studioという開発環境を使って『Hello Android!』アプリを作ってみる  

### Hello Android!アプリの作成（エミュレータでの表示まで）  
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

### 実機(自分のスマホ)での表示  
使用する実機は各々のAndoroidデバイスで.（今回私が使用したのはarrows We3）  
実機での表示方法は2つある.  
1. USB接続
2. Wi-Fiでペアリング  

今回はUSB接続で行う
+ 手順(Andoroid Studio側)
    1. Tools → SDK Manager
    2. SDK Toolsのタブをクリック
    3. その中から「Google USB Driver」を探す
    4. チェックを入れて,【OK】ボタンをクリック.
    5. 確認メッセージでも【OK】をクリック
    6. インストール完了後,【Finish】ボタンをクリック.

+ 手順(実機側)
    1. 設定 → 端末情報 → ソフトウェア情報 → ビルド番号を7回タップ → デベロッパーモードが有効になる
    2. 設定 → 開発者向けオプション
    3. 【USBデバッグ】トグルボタンをオフ → オン
    4. 「USBデバッグを許可しますか？」で【OK】を選択

+ 実行方法
    1. Android Studio(パソコン)と実機をUSB接続  
    2. 確認メッセージは【OK】を選択  
    3. Android Studioのデバイス選択のドロップダウンリストに,実機が追加されている.  
    4. 緑の▷アイコンをクリックして実行「Run 'app'」  
    5. 実機にHello Android!と表示される  

プロジェクトを終了する時は『左上の4本線 → File → Close Projectを選択』

### おまけ(エラー編)  
エミュレータでの実行の時に,実行ボタンを押すと「Error running 'app' Small Phone is already running as process 任意の数値」というエラーメッセージが表示された.この時のエミュレータのSmall Phoneはホーム画面のまま変化はなかった.  
このエラーに随分悩まされたので解決方法をここに残しておく.  
+ エラーの意味
    + Small Phoneのエミュレータがすでに起動しているため,Android Studioが実行処理を正常に進められていない可能性があるという意味.  

解決方法を以下のステップごとに示す
+ 方法1：エミュレータを再起動する
    1. 左上の4本線 → Tools → Device Manager
    2. Small Phoneを停止する(停止ボタン（■）を押す.見当たらない場合は,端末のメニュー（⋮）を開いて停止操作を探す.)
    3. 再び起動(緑の▷アイコンをクリックして実行「Run 'app'」)

+ 方法2：再起動してもエラーが出る場合【エミュレータの起動状態をリセット】
    1. 左上の4本線 → Tools → Device Manager
    2. Small Phoneのメニュー（⋮）を開く
    3. Cold Boot もしくは Cold Boot Now があれば選択
    4. エミュレータが起動したら,もう一度Runボタンを押す.

+ 方法3：それでも解決しない場合
    1. Ctrl + Shift + Esc でタスクマネージャーを開く.
    2. 「プロセス」一覧から emulator.exe や qemu-system-... など,エミュレータ関連のプロセスを探す.
    3. Small Phoneを停止しても残っている場合に限り,その関連プロセスを終了.
    4. Android Studioに戻り,Device Managerを開く.
    5. Cold Boot もしくは Cold Boot Now があれば選択
    6. エミュレータが起動したら,もう一度Runボタンを押す.
 
ちなみに私は方法3で無事に解決した.










