# Hebrit 2

A mobile web app for learning Hebrew (demo for user testers).

- `index.html` – the app. Each page is a section switched by the URL hash:
  `#disclaimer` (00_Disclaimer), `#intro-logo` (00_Intro Logo), `#intro-01` (00_Intro_01), `#login` (00_Login), `#welcome-user` (00_Intro_Welcome Username, shown after login, moves on after 2 s), `#level` (00_Intro_What is your level?), `#alphabet` (00_Intro_do you want to learn the alphabet?), `#home` (the mother page: streak, avatar, current lesson, exercise bar), `#l01-001` (L01_001, opened by tapping Lesson 1), `#l01-002` (L01_002: learn and say shalom, with a microphone that records you and plays it back).
- `img/` – icons cut from the mockups (flame, default avatar, five exercise icons).
- People who already finished onboarding go from the welcome page straight to `#home`.
- `cat.png` – placeholder cat illustration.
- Testing tip: open the site with `#logout` at the end of the address to sign out.
- `privacy.html` – privacy policy (needed for Meta login).

Hosted with GitHub Pages: https://elenalipovet.github.io/hebrit2/

## Saved answers

Onboarding answers are saved in Cloud Firestore under `users/{uid}` (for example `level`, `learnAlphabet`; later `streak`), one field per answer, so they can be changed later.
`firestore.rules` holds the security rules to paste into Firebase (each user can only read and write their own record).
