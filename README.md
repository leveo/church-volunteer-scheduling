# Open-source church volunteer scheduling

Schedule worship, kids, hospitality, and tech teams. Volunteers confirm or decline from an email link, block out dates, and subscribe to their serving calendar.

This repository is the **Volunteer Scheduling** edition of [Church4Christ](https://github.com/leveo/church4christ), an open-source
church management system and website. It contains no separate code: the quick start below
installs Church4Christ v1.6.0 with only the Volunteer Scheduling features switched on (Volunteer Scheduling, Spiritual Gifts, People & Households).
Everything else stays off until you turn it on.

**[Try the live demo](https://demo.church4christ.org/en/sandbox)** · [Main repository](https://github.com/leveo/church4christ) · [Setup guide](https://github.com/leveo/church4christ/blob/v1.6.0/docs/setup.md)

## What you get

- **Ministries, teams, positions, and plans.** A ministry holds teams, a team defines its positions, and a plan is one dated service. A new-ministry wizard sets up a whole area in a few minutes.
- **A scheduling matrix.** Fill a month at a glance; the site warns when someone is already booked that day or has a blockout.
- **Confirm or decline from email.** Each assignment sends a single-use link, no sign-in needed. A decline emails the team's leaders right away.
- **Open slots, blockouts, and availability.** Volunteers claim open slots and mark single days, ranges, or repeating dates away; leaders see who is free across upcoming plans.
- **Plans generated ahead.** Copy a service's needs forward week by week, up to about a year.
- **Reminders and a weekly digest.** Unconfirmed volunteers get a reminder before their service, and everyone gets a weekly list of their serving.
- **Personal schedule and calendar feed.** Each volunteer has a schedule page and a private subscribe link for Apple Calendar, Google Calendar, or Outlook.
- **Apply to serve and a spiritual gifts quiz.** An opportunity board, team applications that leaders approve, and a 40-statement gifts quiz that recommends ministries.
- **12 interface languages** throughout, including English and Chinese.

## Screenshots

![The scheduling matrix: plans down one axis, positions across the other](https://raw.githubusercontent.com/leveo/church4christ/v1.6.0/docs/images/serve/matrix.png)

![A plan with every position and each volunteer's status](https://raw.githubusercontent.com/leveo/church4christ/v1.6.0/docs/images/serve/plan-detail.png)

![The volunteer's serve page with upcoming assignments and open slots](https://raw.githubusercontent.com/leveo/church4christ/v1.6.0/docs/images/serve/serve-landing.png)

![Spiritual gifts quiz results with ministry recommendations](https://raw.githubusercontent.com/leveo/church4christ/v1.6.0/docs/images/serve/gifts-results.png)

## Try the live demo

Open the [public sandbox](https://demo.church4christ.org/en/sandbox). Choose **Administrator**, then open the **Volunteer Console** in the admin menu. Choose **Member portal** to see the volunteer side: the **Serve** page and the gifts quiz. All data is fictional and resets every night.

## Quick start

You need [Git](https://git-scm.com/) and [Node.js](https://nodejs.org/) 22.22.1 or newer.
These commands work in macOS and Linux terminals and in Windows PowerShell.

```bash
git clone --depth 1 --branch v1.6.0 https://github.com/leveo/church4christ.git my-church
cd my-church
npm ci
npm run onboard -- --preset volunteer-scheduling
```

`npm run onboard` opens a local form in your browser for your church's name, colors, logo,
and first administrator, with the Volunteer Scheduling features already checked. Save the form, press
Ctrl+C in the terminal, then apply it and start the site:

```bash
node scripts/setup/index.mjs --preferences .church/preferences.json --yes --dry-run
node scripts/setup/index.mjs --preferences .church/preferences.json --yes
npm run dev
```

Prefer the terminal only? Run `npm run setup -- --mode local --preset volunteer-scheduling`
instead of the form and answer the prompts.

Open the address the installer prints (usually `http://localhost:4321`). On your own
computer, sign-in links print to the terminal instead of being emailed.

## Good to know

- Reminder, digest, and confirm/decline emails need an email provider when deployed; on your own computer, emails print to the terminal instead of being sent.
- Scheduling is per position on dated plans; there is no automatic rotation algorithm that assigns people for you.

## Grow into the full system

This is the complete Church4Christ codebase with a focused starting point. When you are
ready, an administrator can turn on more features (sermons, events, volunteers, groups,
check-in, and more) in **Settings → Modules**, without reinstalling. Upgrades follow the
main repository's [upgrade guide](https://github.com/leveo/church4christ/blob/v1.6.0/docs/upgrade.md).

## Learn more

- [Volunteer scheduling](https://github.com/leveo/church4christ/blob/v1.6.0/docs/features/volunteer-serve.md)
- [Email and automation](https://github.com/leveo/church4christ/blob/v1.6.0/docs/features/email-automation.md)
- [People & households](https://github.com/leveo/church4christ/blob/v1.6.0/docs/features/people-households.md)
- [Putting it online with Cloudflare](https://github.com/leveo/church4christ/blob/v1.6.0/docs/setup.md)

## 中文简介

### 开源教会服事排班系统

为敬拜、儿童、招待、音控等团队排班；同工从邮件链接确认或婉拒，标记不能服事的日期，并订阅自己的服事日历。

- 事工 → 团队 → 岗位 → 排班计划，新事工向导几分钟建好。
- 月度排班矩阵，自动提示重复安排和请假冲突。
- 同工从邮件一键确认或婉拒，无需登录；婉拒会立即通知组长。
- 空缺认领、请假日期、可服事情况一览。
- 自动提醒和每周服事摘要，个人日历可订阅到 Apple / Google / Outlook。
- 申请服事、机会看板，以及 40 题恩赐测验推荐适合的事工。

本仓库是 [Church4Christ](https://github.com/leveo/church4christ) 的单一功能版本，不包含另外的代码。按上面的快速开始安装后，
得到的是完整的 Church4Christ v1.6.0，只预先开启了这一组功能；以后可以在「设置 → 模块」里开启更多功能。

## Questions and issues

Please open issues and questions in the [main repository](https://github.com/leveo/church4christ/issues), where all the code
lives. Report security problems privately through its
[security advisories](https://github.com/leveo/church4christ/security/advisories/new).

## License

[GNU GPL v3](LICENSE), the same license as Church4Christ.
