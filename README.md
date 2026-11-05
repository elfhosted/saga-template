# Saga template

A Saga is your own written account of running apps on ElfHosted. You draft it with Sam, ElfHosted's assistant, publish it on your own GitHub Pages site, and earn hosting credit for it whatever it says. This template turns the files from your ElfBot Saga export into a clean, readable site.

## Set it up

ElfBot's Saga page walks you through this, with links filled in for your account.

1. In ElfBot, check your Saga and choose **Download my Saga**. You get `saga.zip`.
2. Click **Use this template** at the top of this page, then **Create a new repository**. Make it public.
3. Unzip `saga.zip`. In your new repository, choose **Add file**, then **Upload files**, select everything inside the unzipped folder and drag it onto the page. Choose **Commit changes**. Your files replace the samples, and the sample chapter drops out of the list once your Saga is in.

   The zip also holds a `share/` folder of copies you can paste into other blogs. This template never publishes it.
4. Go to **Settings**, then **Pages**. Under **Build and deploy**, choose **Deploy from a branch**, pick the `main` branch and the `/ (root)` folder, then save. Your site appears at `https://USERNAME.github.io/REPO` within a minute or two.
5. Back in ElfBot, paste that address into **Send us your link**. ElfBot checks the page for your Saga ID and the note, then sends it to ElfHosted to confirm your reward.

## Choose a look

Open `_data/saga.yml` and set two lines:

```
style: long-read
palette: forest
```

- `style` is `long-read` (an essay), `uptime-log` (a log of short entries with the chart up front) or `at-a-glance` (cards in a grid).
- `palette` is `forest`, `dusk`, `ember`, `tide` or `graphite`. Each one has a light and a dark version that follow the reader's device.

If a value is missing or misspelled, the site uses `long-read` and `forest`. Your `description` in the same file is what search engines and link previews show.

## Add a chapter

Create a file in `chapters/` named for the year and month, such as `chapters/2027-01.md`:

```
---
layout: chapter
title: "January 2027"
date: 2027-01-20
---

What happened this month.
```

It shows up in the chapter list on your Saga page, newest first. To use a chart, put an `.svg` file in `assets/` and add `![A short description](assets/name.svg)` to the chapter.

## Keep it pseudonymous

- Set `author` in `_data/saga.yml` to a pseudonym, or remove the line to show no name.
- Commits carry the git author name and email you used. Check them with `git config user.name` and `git config user.email`, and use a pseudonym and your GitHub noreply address if you want to stay private.
- Your GitHub profile and username are visible too. Check them before you share the link. Your username is part of the default site address.

## It's yours

The repository and the site belong to you. Edit the text freely, and delete the repository or turn off Pages at any time to take it down.

## The disclosure stays

Every page shows a short note that you received hosting credit and that your opinions are your own. It lives in `_layouts/default.html`, not in your content, so editing `index.md` or `saga.yml` doesn't change it. It has to stay in place for the reward, and so does the Saga ID at the foot of the page, which shows the site is yours.

## Licence

MIT. See `LICENSE`.
