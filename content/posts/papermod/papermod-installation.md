---
title: "PaperMod Installation Guide"
summary: "Step by step guide to install and update PaperMod in your Hugo site."
date: 2021-01-20
weight: 1
series: ["PaperMod"]
aliases: ["/papermod-installation"]
tags: ["PaperMod", "Docs"]
author: ["Aditya Telange"]

social:
  fediverse_creator: "@adityatelange@mastodon.social"
---

> - **We'll be using `yml/yaml` format for all examples down below, it is recommend to use `yaml` over `toml` as it is easier to read.**
> - You can find any [YML to TOML](https://www.google.com/search?q=yml+to+toml) converters if needed.

---

## Getting Started 🚀

1. **Follow [Hugo Docs's - Quick Start](https://gohugo.io/getting-started/quick-start/) guide to install {{< inTextImg url="https://raw.githubusercontent.com/gohugoio/hugoDocs/master/static/img/hugo-logo.png" height="14" >}}.**
   <br>(Make sure you install [**Hugo v0.146.0 +**](https://github.com/gohugoio/hugo/releases) as PaperMod uses some of the latest features of Hugo. You can check your Hugo version by running `hugo version` in terminal.)

2. **Create a new {{< inTextImg url="https://raw.githubusercontent.com/gohugoio/hugoDocs/master/static/img/hugo-logo.png" height="14" >}} site**

   ```bash
   hugo new site MyFreshWebsite --format yaml
   # replace MyFreshWebsite with name of your website
   ```

   Note:
   - Older versions of Hugo may not support `--format yaml`
   - Read more here about [Hugo Docs's - hugo new site command](https://gohugo.io/commands/hugo_new_site/#synopsis)

3. **Installing/Updating PaperMod**
   - Themes reside in `MyFreshWebsite/themes` directory.
   - PaperMod will be installed in `MyFreshWebsite/themes/PaperMod`

   > {{< collapse summary="**Expand Method 1 - Git Clone**" >}}

   **INSTALL** : Inside the folder of your Hugo site `MyFreshWebsite`, run:

   ```bash
   git clone https://github.com/adityatelange/hugo-PaperMod themes/PaperMod --depth=1
   ```

   You may use ` --branch v7.0` to end of above command if you want to stick to specific release.

   **UPDATE**: Inside the folder of your Hugo site `MyFreshWebsite`, run:

   ```bash
   cd themes/PaperMod
   git pull
   ```

   {{</ collapse >}}

   > {{< collapse summary="**Expand Method 2 - Git Submodule (recomended)**" >}}

   **INSTALL** : Inside the folder of your Hugo site `MyFreshWebsite`, run:

   ```bash
   git submodule add --depth=1 https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod
   git submodule update --init --recursive # needed when you reclone your repo (submodules may not get cloned automatically)
   ```

   You may use ` --branch v7.0` to end of above command if you want to stick to specific release.
   Read more about git submodules [here](https://www.atlassian.com/git/tutorials/git-submodule).

   **UPDATE**: Inside the folder of your Hugo site `MyFreshWebsite`, run:

   ```bash
   git submodule update --remote --merge
   ```

   {{</ collapse >}}

   > {{< collapse summary="**Expand Method 3 - Download an unzip**" >}}

   Download PaperMod source as Zip from Github Releases and extract in your themes directory at `MyFreshWebsite/themes/PaperMod`

   Direct Links:
   - [Master Branch (Latest)](https://github.com/adityatelange/hugo-PaperMod/archive/master.zip)
   - [v7.0](https://github.com/adityatelange/hugo-PaperMod/archive/v7.0.zip)
   - [v6.0](https://github.com/adityatelange/hugo-PaperMod/archive/v6.0.zip)
   - [v5.0](https://github.com/adityatelange/hugo-PaperMod/archive/v5.0.zip)
   - [v4.0](https://github.com/adityatelange/hugo-PaperMod/archive/v4.0.zip)
   - [v3.0](https://github.com/adityatelange/hugo-PaperMod/archive/v3.0.zip)
   - [v2.0](https://github.com/adityatelange/hugo-PaperMod/archive/v2.0.zip)
   - [v1.0](https://github.com/adityatelange/hugo-PaperMod/archive/v1.0.zip)

   {{</ collapse >}}

   > {{< collapse summary="**Expand Method 4 - Hugo module**" >}}

   **INSTALL** :
   - Install [Go programming language](https://go.dev/doc/install) in your operating system.

   - Intialize your own hugo mod

   ```bash
   hugo mod init YOUR_OWN_GIT_REPOSITORY
   ```

   - Add PaperMod in your `hugo.yaml` file

   ```go {linenos=true}
   module:
     imports:
     - path: github.com/adityatelange/hugo-PaperMod
   ```

   **UPDATE**:

   ```bash
   hugo mod get -u
   ```

   Read more : [Hugo Docs's - HUGO MODULES](https://gohugo.io/hugo-modules/use-modules/)

   {{</ collapse >}}

4. **Finally set theme as PaperMod in your site config**

   In `hugo.yaml` add:

   ```yml {linenos=true}
   theme: ["PaperMod"]
   ```

### Next up - Customizing PaperMod to suit your preferences 🎨

- Your site will be blank after you set up for the very first time.
- You may go through this website's source code - [PaperMod's exampleSite's source](https://github.com/adityatelange/hugo-PaperMod/tree/exampleSite)
- You can also refer to the following wiki pages for detailed documentation on all features and configuration options.

| Topic                                                                                             | Description                                     |
| ------------------------------------------------------------------------------------------------- | ----------------------------------------------- |
| **[Installation guide](https://github.com/adityatelange/hugo-PaperMod/wiki/Installation)**        | Detailed installation and update instructions   |
| **[Features wiki page](https://github.com/adityatelange/hugo-PaperMod/wiki/Features)**            | In-depth explanations of all features           |
| **[FAQ wiki](https://github.com/adityatelange/hugo-PaperMod/wiki/FAQs)**                          | Common questions and configuration walkthroughs |
| **[Icons wiki](https://github.com/adityatelange/hugo-PaperMod/wiki/Icons)**                       | Documentation for social icons and share icons  |
| **[Variables wiki](https://github.com/adityatelange/hugo-PaperMod/wiki/Variables)**               | List of all available template variables        |
| **[Overiding templates](https://github.com/adityatelange/hugo-PaperMod/wiki/Template_Overrides)** | Guide to customizing templates without forking  |
| **[Releases](https://github.com/adityatelange/hugo-PaperMod/releases)**                           | Detailed history of releases                    |

---

## Support 🫶

- Star 🌟 PaperMod's [Github repository](https://github.com/adityatelange/hugo-PaperMod).
- Help spread the word about PaperMod by [sharing it on social media](https://x.com/intent/tweet/?text=Checkout%20Hugo%20PaperMod%20%E2%9C%A8%0AA%20fast,%20clean,%20responsive%20Hugo%20theme.&url=https://github.com/adityatelange/hugo-PaperMod&hashtags=Hugo,PaperMod) and recommending it to your friends. 🗣️
- You can also sponsor 🏅 on [Github Sponsors](https://github.com/sponsors/adityatelange) / [Ko-Fi](https://ko-fi.com/adityatelange).

---

## Videos featuring PaperMod

You can go through few videos which are available on YouTube for getting to know the creator's thoughts as well as the setup process.

▶️ [Curated list of videos about PaperMod](https://youtube.com/playlist?list=PLeiDFxcsdhUrzkK5Jg9IZyiTsIMvXxKZP)

---
