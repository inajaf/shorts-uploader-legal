# Privacy Policy — Shorts uploader

Last updated: 21 September 2026

## 1. Summary

"Shorts uploader" is a **local desktop application**. It has no backend server, no user
accounts with the author, and no analytics or telemetry. Data the application handles stays
on your computer, except for the requests it makes to the third-party services **you**
configure with **your own** credentials.

## 2. What the application stores, and where

Everything below is stored locally, on your machine:

| Data | Location | Purpose |
| --- | --- | --- |
| YouTube video URLs and metadata you enter | local SQLite database (`data/`) | processing history |
| Downloaded source video and extracted audio | `data/cache/` | transcription and rendering |
| Generated Shorts | `output/` | your finished videos |
| OAuth tokens for YouTube | `data/youtube_channels/`, `data/youtube_token.json` | uploading on your behalf |
| OAuth tokens for TikTok | `data/tiktok_accounts/` | uploading on your behalf |
| API keys (AI providers, TikTok app key/secret) | `.env` | calling those APIs |

These files are stored in plain text on your disk. Protect your computer and your backups
accordingly.

## 3. What leaves your computer, and to whom

The author receives **nothing**. There is no telemetry, no crash reporting, and no
analytics. Data is sent only to services that you enable:

- **YouTube / Google** — when you connect a channel, verify it, upload a Short, or read a
  video's public metadata. Subject to Google's Privacy Policy.
- **TikTok** — when you connect an account, query creator information, upload a draft, or
  publish a post. Subject to TikTok's Privacy Policy.
- **Your chosen AI provider** (Gemini, Groq, OpenAI or OpenRouter) — the transcript text and
  prompts needed to analyse a video and write titles, descriptions and hashtags. Subject to
  that provider's privacy policy.
- **The source video host** — the application downloads the public video you asked it to
  process.

Nothing else is transmitted. If you configure no provider and connect no account, the
application works entirely offline apart from downloading the source video.

## 4. Retention and deletion

You are in control, because the data is on your disk:

- Delete generated videos with the application's delete buttons, or by removing files in
  `output/`.
- Disconnect an account in the application (or delete the token file) to remove its stored
  token. To revoke access on the platform side, use your Google account permissions page or
  TikTok's *Manage app permissions* page.
- Delete `data/` and `.env` to remove all history, caches and credentials.

## 5. Children

The application is not directed at children under 13, and the author does not knowingly
collect information from them.

## 6. Security

Credentials are stored in local files rather than a secret manager. Keep the machine and
its user account secure, and do not share your `.env` file or the `data/` directory.

## 7. Changes

This policy may be updated in the repository where this file is published. The version
published there is the current one.

## 8. Contact

Questions: open an issue in the repository where this file is published.

---

## Кратко по-русски

Программа локальная: у автора нет сервера, аналитики и телеметрии, и он не получает ваши
данные. Всё хранится на вашем компьютере: история в `data/`, готовые ролики в `output/`,
токены YouTube и TikTok в `data/`, ключи API в `.env`. Наружу данные уходят только в те
сервисы, которые вы сами подключили: YouTube, TikTok и выбранный AI-провайдер (ему
отправляется текст расшифровки для анализа). Удалить всё можно, удалив `data/`, `output/`
и `.env`, а также отозвав доступ в настройках Google и TikTok.
