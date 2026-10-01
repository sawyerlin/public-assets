# TikTok for Developers — app registration (non-secret)

- App name: Market Brief Studio
- Category: Education (fallback: News)
- Platform: Desktop (local CLI, localhost OAuth redirect)
- Web/Desktop URL: https://sawyerlin.github.io/public-assets/tiktok/
- Description: Publishes our own short educational videos explaining economic data and market moves to our TikTok account.
- Terms of Service URL: https://sawyerlin.github.io/public-assets/tiktok/terms.html
- Privacy Policy URL: https://sawyerlin.github.io/public-assets/tiktok/privacy.html
- Products: Login Kit, Content Posting API (Direct Post, FILE_UPLOAD)
- Scopes: user.info.basic, video.upload, video.publish

## Product/scope explanation (review form)

Market Brief Studio is a desktop Python tool the developer runs on their own computer to publish short educational videos (economic data explainers, daily market briefs) that the developer produces, to the developer's own TikTok account.

Login Kit: on first run the tool opens the TikTok authorization page in the browser; the account owner logs in and grants access, and the redirect to localhost returns the auth code, which is exchanged for an access/refresh token stored locally on the developer's machine.

user.info.basic: used to display the connected account's name and avatar so the user can confirm which account will receive the post.

video.upload / video.publish (Content Posting API, Direct Post): after a video is rendered, the tool shows the title/caption, privacy level options returned by creator_info, and requires the user to confirm before posting. It then uploads the local MP4 via FILE_UPLOAD and polls the publish status, displaying the result.

No data from other users is collected; tokens are never shared.

## Status
- [x] Form saved (draft)
- [x] Sandbox + target user added (remember: Apply changes; unaudited posts need a PRIVATE account)
- [x] End-to-end sandbox post OK 2026-10-01 (PUBLISH_COMPLETE)
- [ ] Demo video recorded
- [ ] Submitted for audit
