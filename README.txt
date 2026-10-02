EmoStream Pinboard — Firebase + GitHub Pages Edition
=====================================================

Included files
- index.html
- admin.html
- firestore.rules

Open locally
1. Extract this ZIP.
2. Open index.html in Chrome, Edge, or Firefox.

Publish with GitHub Pages
1. Upload index.html to the root of your GitHub repository.
2. Open Settings > Pages.
3. Select Deploy from a branch, main, /(root), then Save.

Implemented
- Real Google sign-in through Firebase Authentication
- Real Email registration and sign-in (8+ character password)
- Select, optimize, preview, upload, and save 1–5 photos per post from a
  computer or smartphone photo library; older single-photo posts remain supported.
- Persistent signed-in session and sign-out
- Nickname and avatar upload from phone or computer
- Avatar image URL option
- Create, delete, like, star, search, filter, and copy pins
- Photo upload, photo URL, image preview, and full-screen lightbox
- Cloud profile/pin synchronization, guest viewing, dark mode, and ESC closing

Required Firebase setup
1. Firebase Console > Build > Authentication > Get started.
2. Sign-in method: enable Google and Email/Password.
3. Authentication > Settings > Authorized domains: add YOURNAME.github.io.
   Enter only the domain, without https:// and without the repository path.
4. Build > Firestore Database > Create database > Production mode.
5. Firestore Database > Rules: replace the editor with firestore.rules and Publish.
6. Upload index.html to GitHub Pages. Firebase requires a web origin; opening
   index.html directly from file:// may not permit Google sign-in.

Admin panel
- Upload admin.html beside index.html.
- Open: https://akarenka.github.io/EmoStream_Website/admin.html
- Only hayashirika05@gmail.com is accepted as administrator.
- Admin can set the manager name, disable/restore users, delete individual
  posts, delete all posts by one user, and delete saved nickname/avatar data.
- A disabled user is blocked from posting by both the app and Firestore Rules.
- Static GitHub Pages cannot securely delete a Firebase Authentication user.
  "Delete profile data" removes the Firestore profile, not the Auth login.

Security note
- firebaseConfig is public web-app configuration, not an administrator secret.
- Never upload a Firebase service-account JSON or private key to GitHub.
- Uploaded avatars are compressed and stored with the user's Firestore profile.

中文版說明
1. 解壓縮後，使用瀏覽器開啟 index.html。
2. 發布到 GitHub 時，請把 index.html 上傳到儲存庫最外層。
3. 到 Settings > Pages，選 main 與 /(root) 後儲存。

Firebase 必須先啟用 Google、Email/Password 及 Firestore。請把
YOURNAME.github.io 加入 Authentication 的授權網域，並把 firestore.rules
貼到 Firestore 規則頁後發布。完成後，帳號、暱稱、Avatar 與貼文即可跨裝置同步。

請把 admin.html 與 index.html 一起上傳。管理頁網址為：
https://akarenka.github.io/EmoStream_Website/admin.html
僅限 hayashirika05@gmail.com 登入。管理員可停權／恢復使用者、逐篇刪除貼文、
刪除某位使用者的全部貼文，以及移除暱稱與 Avatar 資料。
