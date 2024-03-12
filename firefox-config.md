# Firefox Configuration
_This configuration aims to deliver the best privacy and security without breaking web sites._


## Settings
- General
    - Disable `Recommend extensions as you browse`
    - Disable `Recommend features as you browse`
- Home
    - Firefox Home Content
        - Shortcuts
            - Disable `Sponsored shortcuts`
- Search
    - Search Suggestions
        - Disable all suggestions
- Privacy & Security
    - Select `Strict` Browser Privacy
    - Web Site Privacy Preferences
        - Enable `Tell web sites not to sell or share my data`
        - Enable `Send web sites a "Do Not Track" request`
    - Cookies and Site Data
        - Enable `Delete cookies and site data when Firefox is closed`
    - Passwords
        - Disable `Ask to save passwords for web sites`
    - History
        - Select `Use custom settings for history`
        - Enable `Remember browsing and download history`
    - Permissions
        - Block all requests for all permissions
        - Enable `Block pop-up windows`
        - Enable `Warn you when web sites try to install add-ons`
    - Firefox Data Collection and Use
        - Disable all options
    - Security
        - Deceptive Content and Dangerous Software Protection
            - Enable all options
    - Certificates
        - Enable all options
    - HTTPS-Only Mode
        - Select `Enable HTTPS-Only Mode in all windows`


## about:config
- Set `extensions.pocket.enabled` to `false` to disable Pocket
- Set `dom.event.clipboardevents.enabled` to `false` to defeat copy/paste blocking


# Add-ons
- [Skip Redirect](https://addons.mozilla.org/en-US/firefox/addon/skip-redirect/)
- [FastForward](https://addons.mozilla.org/en-US/firefox/addon/fastforwardteam/)
- [Smart Referer](https://addons.mozilla.org/en-GB/firefox/addon/smart-referer/)
- [uBlock Origin](https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/)


## Smart Referer Configuration
- Disable `Use default whitelist`
- Select `Lax` Domain name matching strictness


## uBlock Origin [Configuration](/firefox-config/ublock_origin_initial_config.txt)
<details>
    <summary>Settings</summary>
    <img src="firefox-config/ublock_origin_settings.png" width="800">
</details>

<details>
    <summary>Filter Lists</summary>
    <img src="firefox-config/ublock_origin_filter_lists.png" width="800">
</details>

<details>
    <summary>My Rules</summary>
    <img src="firefox-config/ublock_origin_my_rules.png" width="800">
</details>
<br />


# References
- [Actually Legitimate URL Shortener Tool](https://filterlists.com/lists/actually-legitimate-url-shortener-tool)
- [Arkenfox](https://github.com/arkenfox/user.js/wiki/4.1-Extensions)
- [Privacy Guides](https://www.privacyguides.org/browsers/#firefox)
