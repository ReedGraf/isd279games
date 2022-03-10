# Emulator Embed

## How do use this?

You need to host an `embed.html` file somewhere and have a compatible ROM. To figure out the right embed file for you here's a list:

- [`ds-embed.html`](/emulator/ds/ds-embed.html) - works with Nintendo DS ROMs
- [`gba-embed.html`](/emulator/gba/gba-embed.html) - works with Nintendo Game Boy Advanced ROMs

Once you've gotten your embed file then you need a compatible ROM and you'll need to host them somewhere (I use GitHub pages). Next we will talk about how to get it to work by adding a ROM for it to run.

---

## How do I specify the ROM?

To do this you have to take advantage of a query string in the URL. This may sound complicated but it's not. Here's an example:

```
https://www.google.com/?gws_rd=ssl
                       ^ this part^
```

What a query string is roughly is the thing after a question mark in a URL. I've formatted it so after the link to the emulator embed you add this string at the end:

```
?rom=https://mywebsite.com/my-rom.zip
     ^--Replace with your ROM link--^
```

As a result you should have something that looks like this when put together:

```
https://mywebsite.com/ds-embed.html?rom=https://rom-website.com/some-rom.zip
```

This link should be the one you can embed in an iFrame or use in a Google Site.

> TL;DR Add `?rom=` to the end of the URL of the embed.html file and then paste the link to your ROM after that. Lastly, go crazy.

> ##### If you are wondering why I'm using a zip instead of a regular rom. Idk, it just has worked having the ROM in a zip file. `¯\_(ツ)_/¯`
 