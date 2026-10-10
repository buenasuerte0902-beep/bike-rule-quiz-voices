# bike-rule-quiz-voices

車ナビ(bike-rule-quiz)の交差点名・道路名を読み上げる Google の声(ja-JP-Neural2-B)の置き場。

- `audio/<sha先頭2文字>/<sha>.mp3` … sha は `sha256("ja-JP-Neural2-B|語句")`。32kbps に縮めてある
- `index.txt` … 置いてある音声の sha の一覧(1行に1つ)

本番サーバーは手元に無い音声をここから取り、ここにある語句は Google で作り直さない(server/app.py の TTS_STORE_URL)。
追加は bike-rule-quiz の `car/tools/tts_store.py` で行う。ここへのプッシュは本番のデプロイにならない。

語句は OpenStreetMap の名前から作っている。© OpenStreetMap contributors
