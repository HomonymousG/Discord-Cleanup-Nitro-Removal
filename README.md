# Discord Cleanup/Nitro Removal

Discord kept adding too much crap cluttering the interface, so it was time to set things right again. I don't know what I'm doing but I found others who had achieved what I was looking for, and built upon those as things kept changing. It's now mor robust and shouldn't break with updates as easily, but also grown too big to store in a discord post so it can live here instead.

# Usage

Open up the console, paste the below, hit Enter et voila! You may need to enable the inspector first. Anything you want to still include, just delete the line first.

```css
style = `<style>

div[class*="nameplated_"] > div[class^="container_"],                          /* Remove user nameplates */
span[class^="chipletContainer"],                                               /* Remove server tags */
div[class^="footer_"],                                                         /* Remove Discover button */
button[aria-label="Open sticker picker"],                                      /* Remove sticker picker */
button[aria-label="Send a gift"],                                              /* Remove gift button */
button[aria-label="Apps"],                                                     /* Remove apps button */
div[aria-label="Edit Image with Apps"],                                        /* Remove image apps button */
div[class^="gifFavoriteButton_"],                                              /* Remove gif favourites button */
ol[aria-label="Messages in "] > div[class^="containerExpanded_"],              /* Remove sticker wave option in new DMs */
ul[aria-label="Direct Messages"] > li:has(a[href="/store"], a[href="/shop"]),  /* Remove Nitro and Shop tab under Friends */
div[aria-label="Close DM"],                                                    /* Remove the X to close DM */
div[aria-label="Leave Group"],                                                 /* Remove the X to close group DM */
div[id="profile-customization-tab"] > div[class^="container_"],                /* Remove "Give your profile a fresh look" in User Profiles */
div[class^="premiumFeatureBorder"],                                            /* Remove Nitro theme previews in Profile and Appearance */
div[class^="upsellContainer"],                                                 /* Remove various Nitro upgrade pester buttons */
div[class^="upsellOverlay"],                                                   /* Remove Per-Server theme Nitro pester */
div[id="appearance-tab"] > div > div[class^="children_"]
  > div[class^="marginTop8_"] > div > div[class^="selectionGroup_"],           /* Remove Nitro alternative app icons in Appearance */
div[aria-label="User Settings"] > div[aria-label="Family Center"],             /* Remove Family Centre in User Settings */
div[id="user-settings-cog-Family_Center"],                                     /* Remove Family Centre in cogwheel right-click */
div[aria-label="User Settings"] :nth-child(n+13):nth-child(-n+19),             /* Remove Billing section in User Settings */
div[id="user-settings-cog"] > div :nth-child(n+10):nth-child(-n+14),           /* Remove Server boost, Supscriptions, Gift Inventory, Billing from cogwheel right click */
div[aria-label="User Settings"] :nth-child(n+38):nth-child(-n+39),             /* Remove Merch and Hype Squad in User Settings */
div[id="user-settings-cog-merchandise"],                                       /* Remove Merch in cogwheel right-click */
div[id="user-settings-cog-Hypesquad_Online"],                                  /* Remove Hype Squad in cogwheel right-click */
nav[class^="sidebar_"] > div:not([aria-label="User Settings"]) :nth-child(7),  /* Remove Stickers in Server */
div[id="guild-context-guild-settings--STICKERS"],                              /* Remove Stickers in Server right-click */
div[class^="tierHeaderLocked_"],                                               /* Remove locked tiers in Server Stickers */
div[class^="tierBody_"],                                                       /*                                        */
div[class^="tierInProgress_"],                                                 /*                                        */
div[class^="progress_"],                                                       /*                                        */
nav[class^="sidebar_"] > div:not([aria-label="User Settings"]) :nth-child(9),  /* Remove Custom Invite Link in Server */
div[id="guild-context-guild-settings--VANITY_URL"],                            /* Remove Custom Invite Link in Server right-click */
nav[class^="sidebar_"]
  > div:not([aria-label="User Settings"]) :nth-child(n+21):nth-child(-n+28),   /* Remove Community (21-23), Monetization (24-26), Server Boost (27-28) */
div[id="guild-context-guild-settings--COMMUNITY"],                             /* Remove Community in Server Right-click */
div[id="guild-context-guild-settings--ROLE_SUBSCRIPTIONS"],                    /* Remove Server Subscriptions in Server Right-click */
div[id="guild-context-guild-settings--GUILD_PREMIUM"],                         /* Remove Server Boost Status in Server Right-click */
nav[class^="sidebar_"]                                                         
  > div:not([aria-label="User Settings"]) :nth-child(n+33):nth-child(-n+34),   /* Remove Delete Server */
button[class^="shinyButton"],                                                  /* Remove various "Unlock with Boosting" buttons */
none {display:none !important;}

div[class^="gifTag_"] {transform:scale(0.3);  transform-origin: top left;}     /* Reduce gif badge size */

:root {                                                                        /* Restore original font, kinda*/
  --font-primary: "Whitney Book", "gg sans", "Helvetica Neue", "Helvetica", "Arial", sans-serif !important;
  --font-display: "Whitney Book", "gg sans", "Helvetica Neue", "Helvetica", "Arial", sans-serif !important;
}

</style>`
document.head.innerHTML += style
```

Hot top for web users - paste the above into https://caiorss.github.io/bookmarklet-maker/ and hit Generate, save the output as a bookmark in your browser and you can run it from the URL bar whenever you reload Discord.




Originally based on https://github.com/Znunu/Discord-Purge-Nitro, with some added inspiration from https://github.com/bytebone/discord-ui-cleanup
