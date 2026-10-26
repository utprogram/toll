高速料金アプリ(ホーム画面に追加できる版)

【中身】
index.html / manifest.webmanifest / sw.js / icon-*.png / apple-touch-icon.png
すべて同じフォルダに置いてください。

【使い方】
1. このフォルダごと、https で配信できる場所に置く(社内サーバー、GitHub Pages、Netlify、Cloudflare Pages など)。
2. スマホでそのURLを開く。
   - iPhone(Safari): 共有ボタン →「ホーム画面に追加」
   - Android(Chrome): メニュー →「ホーム画面に追加」または「アプリをインストール」
3. ホーム画面のアイコンから開くと、アドレスバーのない全画面で起動します。

【パソコンで試すだけなら】
フォルダの中で  python3 -m http.server 8000  を実行し、ブラウザで http://localhost:8000/ を開く。

【料金を直したとき】
index.html の中の prices を書き換え、sw.js の VERSION を変える(例: toll-v2)。
VERSION を変えないと、利用者の端末が古い料金を使い続けることがあります。

【注意】
index.html をダブルクリックして開く(file://)と、ホーム画面への追加とオフライン動作は使えません。画面そのものは動きます。
