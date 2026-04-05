---
title: Create a bot
---
> [!info] User automation
> Fluxer allows for **non-malicious** user account automation (selfbots), but as of now that usecase is not being tested on `fluxer-swift`.
## Creating the bot
To make a Fluxer bot, go to your Fluxer account settings, then in the **Applications** tab in the sidebar (it is at the very bottom).
![[ishare-1775390382-brave browser.png]]

Then, create an application. You should see something like this:
![[ishare-1775390454-obsidian.png]]

In this screen you can set your bot's profile picture, banner, about me, and more. If this is a bot meant for only your communities to use, you may want to disable **Public Bot** so others cannot invite it to their own communities.
## Getting its token
Below **Bot token**, click on Regenerate. You should then see your bot token, save it somewhere safe.
> [!danger]
> Never share this with anyone for any reason. **Anyone** with this token can take full control of your bot.
> Also, **do not** push that token to your repository. Use a proper [[Configuration|configuration]] file and `.gitignore` it.
## Adding your bot to a community
You can add bots to any community that you own, or have the `Administrator` or `Manage Community` permission in. For that, scroll down to the **OAuth2 URL Builder** section, and choose the `bot` scope. Then, select the permissions that your bot will need.
> [!warning] Administrator permission
> You should avoid granting the **Administrator** permission to your bot, as it gives full access to communities with no restrictions. This means that if your bot is taken over, some quite serious damage can be done.
> Fluxer will also show a warning to users trying to add your bot if it requests this permission.

You can then copy the **Authorize URL** and open it in your browser.


