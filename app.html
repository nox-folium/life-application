<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <title>生活リズム改善アプリ</title>
    <link rel="stylesheet" href="all.css">
</head>
<body>
    <div class="waku">
        <h1 style="font-size: 30px; margin-top: 0;">今日のスケジュール</h1>

        <!-- 入力エリア -->
        <div class="form-area">
            <label>時間：<input type="time" id="zikan" required></label>
            <br>
            <label>予定：<input type="text" id="mokuhyou" placeholder="例：朝の散歩をする" style="width: 450px;" onkeydown="if(event.key==='Enter')tuika()"></label>
            <br>
            <!-- 追加ボタン　Enterキー押しても実行可能 -->
            <button class="add-btn" onclick="tuika()">＋ スケジュールを追加</button>
        </div>

        <hr style="border: none; border-top: 1px solid #cbd5e1; margin: 25px 0;">

        <div id="itiran"></div>
    </div>

    <script>

        // スケジュール保存
        // 時間と予定をオブジェクト格納
        let items = [];

        // localStrageに保存
        function hozon(){
            // JSON形式
            localStorage.setItem("schedule",JSON.stringify(items));
        }

        // localStregeから読み込み
        function yomikomi(){
            // scheduleを取得
            const saveData =localStorage.getItem("schedule");
            // データあったとき
            if(saveData){
                try{
                    // items配列に戻す
                    const data =JSON.parse(saveData);
                    // 配列であることを確認して読み込み
                    if(Array.isArray(data)){
                        items = data.filter(item =>
                            item && typeof item.time === "string" && typeof item.text === "string"
                        );
                    }
                }
                // 読み込みに失敗したとき
                catch(error){
                    // consoleに表示
                    console.error("保存データの読み込みに失敗しました",error);
                    items = [];
                }
            }
        }

        // スケジュール追加
        function tuika() {
            // 入力欄を取得
            const zikanInput = document.getElementById("zikan");
            const mokuhyouInput = document.getElementById("mokuhyou");

            // 入力を取得
            const zikan = zikanInput.value;
            const mokuhyou = mokuhyouInput.value.trim();

            // 時間の形式（00:00~23:59）に一致するか確認
            const timeRegex = /^([01]\d|2[0-3]):[0-5]\d$/;
            // 正しくないときは警告
            if (!timeRegex.test(zikan)) {
                alert("正しい時間を入力してください（例: 08:30）。");
                return;
            }
            // 予定が未入力のときは警告
            if (!mokuhyou) {
                alert("予定を入力してください。");
                return;
            }

            // itemに時間と予定を追加
            items.push({ time: zikan, text: mokuhyou });
            // 時間の早い順にスケジュールを整列
            items.sort((a, b) => a.time.localeCompare(b.time));
            // localStrageに保存
            hozon();
            // 画面に表示
            hyouzi();
            // 入力欄を空にする
            mokuhyouInput.value = "";
        }

        // スケジュール削除
        function sakujo(index) {
            // index番目の予定を削除
            items.splice(index, 1);
            // 
            hozon();
            hyouzi();
        }

        // スケジュール表示
        function hyouzi() {
            // 表示場所を取得
            const itiran = document.getElementById("itiran");
            // スケジュール0件のとき
            if (items.length === 0) {
                itiran.innerHTML = '<div class="empty-msg"></div>';
                return;
            }

            itiran.innerHTML = items.map((item, i) => `
                <div class="list-box">
                    <span style="${item.completed ? 'text-decoration: line-through; color:gray;' : ''}">
                        <b>【${item.time}】</b> ${item.text}</span>
                    <button class="del-btn" onclick="kanryou(${i})" ${item.completed ? 'disabled' : ''}>${item.completed ? '達成済み' : '達成'}</button>
                </div>
            `).join('');
        }
        yomikomi();
        hyouzi();
    </script>

</body>
</html>
