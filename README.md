# BoltExercise - 像素鳥

Bolt 目前(2020/05/07) 被Unity收購，但現在Bolt正在開發 2.0版，

所以現在Bolt有點尷尬，學舊版怪怪，新版又不穩定，所以要學自行考慮

# Bolt並非萬能，再怎麼厲害，用C#寫腳本才是原本的作法

# Bolt如果太多後期很難維護，去查查[Unreal藍圖](https://blueprintsfromhell.tumblr.com/)就知道

之前做完 PlayMaker 後，用Bolt仿造一下

現在分析下兩個比較

- PlayMaker

因為著重狀態，所以可以利用狀態來進行分段，不用像Bolt要實現功能結果，必須加bool之類的

在表現上，我認為確實輸給Bolt ，Bolt完全是Unity本身API 不像PlayMaker是自己的API，我認為這點很重要

- Bolt

功能上因為使用Unity API 對後期學習銜接很棒，但問題也在此

雖然Bolt 使用Unity API但也不是全部都有，所以有時會出現 **"!?，Bolt沒這API ，只好繞個圈子"** 而且這還不是一次

舉個例子: 以1.5秒為單位，生成水管，

用PlayMaker寫就是弄個狀態機，然後指向自己，重複執行

用C# 寫，就放在 Update裡，時間到就生成

用Bolt寫，時間控制花了整個下午才搞懂，放Update不對，放Start也不對，最後原來要先觸發時間控制一下，再用個迴圈轉回去

Bolt 雖然建構遊戲邏輯很煩人，但建構狀態機(FSM)，堪稱神器不為過，

PlayMaker建構 FSM 也不錯，但畫面就是亂糟糟，很混亂

Bolt 直觀方便，所以目前Bolt給我用，我會拿去做FSM，比用C#打腳本方便多了

# 結論

基本上PlayMaker 跟 Bolt 各有優缺，看自己喜歡哪種，


![](https://github.com/PeterLukGit/BoltExercise/blob/master/00.PNG)

![](https://github.com/PeterLukGit/BoltExercise/blob/master/01.PNG)

# 注意

附贈的 unitypackage 並無 Bolt

請自行購買後，再導入 Bolt 即可

[購買連結](https://assetstore.unity.com/packages/tools/visual-scripting/bolt-163802)


# 教學來源

[BoltFSM](https://www.youtube.com/watch?v=u_7dgkM-DNg)

[Bolt教學](https://www.youtube.com/watch?v=xAlf6Jb5XFI)

[Bolt Event](https://www.youtube.com/watch?v=jEHn6hU6VEg)


# 責任聲明：

[Blog位置](https://peterlukgit.github.io/)

本Blog裡部分資料如為外部引用，版權為原著作者所有

若非，版權歸本Blog所有，

若是有侵權之於，請聯繫Emall:peterlukgit@gmail.com

若是並未第一時間回復，請稍等數日，或是再寄一封確認

本Blog意在製作遊戲教學，

若轉載請保留標示姓名，原出處，禁止商用
