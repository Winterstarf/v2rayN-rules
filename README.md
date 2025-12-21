# Important
These rules are meant to be used with whatever XRay core-supported client you want. For desktop, I can recommend v2rayN, which is available on Linux, Win and macOS.
As for mobile, v2RayTun is there on Android and iOS, as well as v2rayNG (Android only), though there are other options like V2Box and Happ (which I do not recommend, however, as they're pieces of ad-infested trash).

If you want to use cores like Sing-Box or mihomo (Clash/Meta), there are converters to **.srs** and **.mrs** files available, though because of lack of support of some of the transport options on these cores I restrain from using them at this time.

I should also mention that the rules below are using geo files from the **[runetfreedom](https://github.com/runetfreedom/russia-v2ray-rules-dat)** repo, containing "geo tags" (i.e. geoip:google, geosite:meta), which are useful if my rules are not sufficient for your use scenario.

## Routing rules

There currently exists 3 routing "profiles":

| Profile | Description
| :--- | :--- 
| **blocked_only** | Proxies only known blocked domains and CIDR ranges
| **except_ru** | Proxies all traffic except for Russian domains and IP space
| **all** | Routes all traffic through the proxy

### Raw links for v2rayN/v2rayNG with .json files
* **blocked_only.json**: `https://raw.githubusercontent.com/Winterstarf/v2ray-rules/refs/heads/main/rules/blocked_only.json`
* **except_ru.json**: `https://raw.githubusercontent.com/Winterstarf/v2ray-rules/refs/heads/main/rules/except_ru.json`
* **all.json**: `https://raw.githubusercontent.com/Winterstarf/v2ray-rules/refs/heads/main/rules/all.json`

### Base64 encoded rules for v2RayTun
* **blocked_only**: 
```
eyJkb21haW5TdHJhdGVneSI6IklQSWZOb25NYXRjaCIsImlkIjoiMTc1QUE2NzMtMkVENC00QjNELUE2RUQtQTVGMEUyMTMyRUY2IiwiYmFsYW5jZXJzIjpbXSwiZG9tYWluTWF0Y2hlciI6Imh5YnJpZCIsIm5hbWUiOiJSdWxlc2V0IiwicnVsZXMiOlt7Il9fbmFtZV9fIjoiQmxvY2sgQWRzIiwiaWQiOiI5MDJDQjdGOS1BQzlBLTQzNEYtQTkyNS1FNEE2MTlEQkQ1OTAiLCJ0eXBlIjoiZmllbGQiLCJkb21haW4iOlsiZ2Vvc2l0ZTpjYXRlZ29yeS1hZHMtYWxsIl0sIm91dGJvdW5kVGFnIjoiYmxvY2sifSx7Il9fbmFtZV9fIjoiUHJveHkgRE5TIiwiaWQiOiIyRjg0RjNCQi1CQUM1LTRBM0UtOEIyRC1DOTM2M0VBQkI1NjQiLCJ0eXBlIjoiZmllbGQiLCJpcCI6WyIxLjAuMC4xIiwiMS4xLjEuMSIsIjguOC44LjgiLCI4LjguNC40Il0sIm91dGJvdW5kVGFnIjoicHJveHkifSx7Il9fbmFtZV9fIjoiUHJveHkgYmxvY2tlZCBDSURSIiwiaWQiOiI3NzY1NzJEQS1DRTQ0LTQ1QTQtODg2OC1DRDc1MzQ3NTQxRUEiLCJ0eXBlIjoiZmllbGQiLCJpcCI6WyJnZW9pcDpydS1ibG9ja2VkIiwiZ2VvaXA6Z29vZ2xlIl0sIm91dGJvdW5kVGFnIjoicHJveHkifSx7Il9fbmFtZV9fIjoiUHJveHkgYmxvY2tlZCBkb21haW5zIiwiaWQiOiJEMDlGOTVEMS1COEQzLTRCN0ItQUEzRS1DNUE2RDAwMDc5RTEiLCJ0eXBlIjoiZmllbGQiLCJkb21haW4iOlsiZ2Vvc2l0ZTpydS1ibG9ja2VkIl0sIm91dGJvdW5kVGFnIjoicHJveHkifSx7Il9fbmFtZV9fIjoiUHJveHkgY3VzdG9tIGRvbWFpbnMiLCJpZCI6IkM0RkVCMEU1LUZCNjYtNDg1MS1BQzEzLUU1NTlDQ0VGN0JENyIsInR5cGUiOiJmaWVsZCIsImRvbWFpbiI6WyJhbGxhcmtub3cub25saW5lIiwiYW1lbXYuY29tIiwiYW5pbWVnby5vcmciLCJhbmltZW5pbWUucnUiLCJhdG9taWNzLndzIiwiYmFja2xvZ2dkLmNvbSIsImJ5dGVkYXBtLmNvbSIsImJ5dGVnZWNrby1pMThuLmNvbSIsImJ5dGVvdmVyc2VhLmNvbSIsImNvb21lci5wYXJ0eSIsImNvb21lci5zdSIsImRvdXlpbi1wb3J0YWwuY29tIiwiZG91eWluLmNvbSIsImRvdXlpbnNlYy5jb20iLCJkb3V5aW5zdGF0aWMuY29tIiwiZG91eWludm9kLmNvbSIsImV6Z2lmLmNvbSIsImZvdHBybzEzNWFsdG8uY29tIiwiaWJ5dGVkdG9zLmNvbSIsImlieXRlaW1nLmNvbSIsImllc2RvdXlpbi5jb20iLCJpZXNkb3V5aW5hcGkuY29tIiwiaXBzdGF0cC5jb20iLCJpc25zc2RrLmNvbSIsImp1dC5zdSIsImtlbW9uby5wYXJ0eSIsImtlbW9uby5zdSIsImtlbW9uby5jciIsImx1bWV4LnNwYWNlIiwibXVsdC1mYW4udHYiLCJtdXNjZG4uY29tIiwibXVzaWNhbC5seSIsIm9icnV0LnNob3ciLCJwMTYtdGlrdG9rY2RuLWNvbS5ha2FtYWl6ZWQubmV0IiwicmV2ZXJiLmNvbSIsInJleW9ob2hvLnNwYWNlIiwic2dwc3RhdHAuY29tIiwic25kLnNjIiwic25kY2RuLmNvbSIsInNuc3Nkay5jb20iLCJzb3VuZGNsb3VkLmNsb3VkIiwic291bmRjbG91ZC5jb20iLCJzb3ZldHJvbWFudGljYS5jb20iLCJzb25pY2JpZHMuY29tIiwidGlrLXRva2FwaS5jb20iLCJ0aWt0b2suY29tIiwidGlrdG9rY2RuLWV1LmNvbSIsInRpa3Rva2Nkbi11cy5jb20iLCJ0aWt0b2tjZG4uY29tIiwidGlrdG9rZC5uZXQiLCJ0aWt0b2tkLm9yZyIsInRpa3Rva3YuY29tIiwidGlrdG9rdi5ldSIsInRpa3Rva3YudXMiLCJ0aWt0b2t3LmV1IiwidGlrdG9rdy51cyIsInR0bGl2ZWNkbi5jb20iLCJ0dHdzdGF0aWMuY29tIiwidmlkZW9mcmFtZTIuY29tIiwieW5vcHJvamVjdC5uZXQiLCJ5dW1lLndpa2kiLCJtb2RyaW50aC5jb20iLCJvcGVudnBuLm5ldCIsIm1vZHVsYXJncmlkLm5ldCIsInNwb25zb3IuYWpheS5hcHAiLCJsZWFndWVvZmxlZ2VuZHMuY29tIiwicmlvdGdhbWVzLmNvbSIsInBsYXl2YWxvcmFudC5jb20iLCJzdGVhbWhpc3RvcnkubmV0IiwiYjQybWFwLmNvbSIsImFuaWxpc3QuY28iLCJuZXh1c21vZHMuY29tIl0sIm91dGJvdW5kVGFnIjoicHJveHkifSx7Il9fbmFtZV9fIjoiUHJveHkgRGlzY29yZCBDSURSICIsImlkIjoiNjBEQTZDNzUtNjVGOC00QUYxLUE0MjctNjc3NUUwQjhGMDRCIiwidHlwZSI6ImZpZWxkIiwiaXAiOlsiMzQuMC4wLjAvMTYiLCIzNC4xLjIyNC4wLzE5IiwiMzUuMjA3LjAuMC8xNiIsIjM1LjIxMi4wLjAvMTQiLCIzNS4yMTcuMC4wLzE4IiwiMzUuMjE5LjIyNC4wLzE5IiwiNjYuMjIuMTkyLjAvMTgiXSwib3V0Ym91bmRUYWciOiJwcm94eSJ9LHsiX19uYW1lX18iOiJQcm94eSBUZWxlZ3JhbSBDSURSICIsImlkIjoiNkJDQ0UwRTYtNDc1Ni00OTU4LTgzRjEtMzAyNTI4NjU5NzMyIiwidHlwZSI6ImZpZWxkIiwiaXAiOlsiMTQ5LjE1NC4xNjAuMC8yMCIsIjE4NS43Ni4xNTEuMC8yNCIsIjkxLjEwNS4xOTIuMC8yMyIsIjkxLjEwOC4xNi4wLzIxIiwiOTEuMTA4LjQuMC8yMiIsIjkxLjEwOC41Ni4wLzIyIiwiOTEuMTA4LjguMC8yMSJdLCJvdXRib3VuZFRhZyI6InByb3h5In0seyJfX25hbWVfXyI6IlByb3h5IFdoYXRzQXBwIENJRFIiLCJpZCI6IkRFMkYwRkY0LUI2REQtNDQwMS1CRjY0LThCMkU4NzhGOUMwQyIsInR5cGUiOiJmaWVsZCIsImlwIjpbIjEyOS4xMzQuMC4wLzE3IiwiMTU3LjI0MC4wLjAvMTYiLCIxNjMuNjQuMC4wLzEyIiwiMTczLjI1Mi42NC4wLzE4IiwiMTg1LjYwLjIxNi4wLzIyIiwiMjA0LjE1LjIwLjAvMjIiLCIzMS4xMy4yNC4wLzIxIiwiMzEuMTMuNjQuMC8xOCIsIjU3LjE0MS4wLjAvMjAiLCI1Ny4xNDQuMC4wLzE0IiwiNjYuMjIwLjE0NC4wLzIwIiwiNjkuMTcxLjE5Mi4wLzE4IiwiNjkuNjMuMTYwLjAvMTkiLCI3NC4xMTkuNzYuMC8yMiJdLCJvdXRib3VuZFRhZyI6InByb3h5In0seyJfX25hbWVfXyI6IlByb3h5IFJvYmxveCBDSURSIiwiaWQiOiJGNzQ1MTM4NS1FNDM0LTQ0NTktQjNENS1BRUM5QjEyRUM3Q0UiLCJ0eXBlIjoiZmllbGQiLCJpcCI6WyIxMjguMTE2LjAuMC8xNyJdLCJvdXRib3VuZFRhZyI6InByb3h5In0seyJfX25hbWVfXyI6IkRpcmVjdCBiaXR0b3JyZW50IiwiaWQiOiI3OUI4OUYzNi1BNDU3LTRFMjEtOTBENy0yNDE4OTQ4NEI5MzUiLCJ0eXBlIjoiZmllbGQiLCJwcm90b2NvbCI6WyJiaXR0b3JyZW50Il0sIm91dGJvdW5kVGFnIjoiZGlyZWN0In0seyJfX25hbWVfXyI6IkRpcmVjdCBwcml2YXRlIENJRFIiLCJpZCI6IjI2MUQ2MjNGLUU1NkMtNEY3Qy04RTAwLTYxQjBGMzMxOEEwOSIsInR5cGUiOiJmaWVsZCIsImlwIjpbImdlb2lwOnByaXZhdGUiXSwib3V0Ym91bmRUYWciOiJkaXJlY3QifSx7Il9fbmFtZV9fIjoiRGlyZWN0IHByaXZhdGUgZG9tYWlucyIsImlkIjoiOEQ0NERBQzEtMDU3QS00NTNGLTg3QUYtODczMDM0OEZFMzcyIiwidHlwZSI6ImZpZWxkIiwiZG9tYWluIjpbImdlb3NpdGU6cHJpdmF0ZSJdLCJvdXRib3VuZFRhZyI6ImRpcmVjdCJ9LHsiX19uYW1lX18iOiJEaXJlY3QgZWxzZSIsImlkIjoiMTBGRDJEMEYtQTQ4Ny00OTE1LTlEM0EtNTlCMjI2MkU2QTJGIiwidHlwZSI6ImZpZWxkIiwicG9ydCI6IjAtNjU1MzUiLCJvdXRib3VuZFRhZyI6ImRpcmVjdCJ9XX0=
```
* **except_ru**: 
```
eyJkb21haW5TdHJhdGVneSI6IklQSWZOb25NYXRjaCIsImlkIjoiOTgwMTc5NDQtQjdDMC00NEE4LTkyRDYtRUJBQUQyOTlFRTY2IiwiYmFsYW5jZXJzIjpbXSwiZG9tYWluTWF0Y2hlciI6Imh5YnJpZCIsIm5hbWUiOiJSdWxlc2V0IiwicnVsZXMiOlt7Il9fbmFtZV9fIjoiQmxvY2sgQWRzIiwiaWQiOiIxMTgyN0E3MS1BMDZDLTRDMDUtOTI0RC1COTQ5QTYwMjMxN0UiLCJ0eXBlIjoiZmllbGQiLCJkb21haW4iOlsiZ2Vvc2l0ZTpjYXRlZ29yeS1hZHMtYWxsIl0sIm91dGJvdW5kVGFnIjoiYmxvY2sifSx7Il9fbmFtZV9fIjoiRGlyZWN0IFJ1c3NpYW4gQ0lEUiIsImlkIjoiMjIxQkJCNzktMTA2Qi00MDc2LUI4NTktMEUyN0ZFMkE5OTcyIiwidHlwZSI6ImZpZWxkIiwiaXAiOlsiZ2VvaXA6cnUiXSwib3V0Ym91bmRUYWciOiJkaXJlY3QifSx7Il9fbmFtZV9fIjoiRGlyZWN0IGJpdHRvcnJlbnQiLCJpZCI6IkQwNTlEREZELTg0RjktNDQ1NC1CRTE5LTI5RUI3MDA3NkMwOCIsInR5cGUiOiJmaWVsZCIsInByb3RvY29sIjpbImJpdHRvcnJlbnQiXSwib3V0Ym91bmRUYWciOiJkaXJlY3QifSx7Il9fbmFtZV9fIjoiRGlyZWN0IHByaXZhdGUgQ0lEUiIsImlkIjoiRTJENkVDOUYtMTU1MC00MDU0LTg1OUYtMTEzQTI4OUJBNEEzIiwidHlwZSI6ImZpZWxkIiwiaXAiOlsiZ2VvaXA6cHJpdmF0ZSJdLCJvdXRib3VuZFRhZyI6ImRpcmVjdCJ9LHsiX19uYW1lX18iOiJEaXJlY3QgcHJpdmF0ZSBkb21haW5zIiwiaWQiOiI0ODBDMDY5OS0yOEQ4LTQ2QzEtQUExRi00N0U3NkNBQUYxN0YiLCJ0eXBlIjoiZmllbGQiLCJkb21haW4iOlsiZ2Vvc2l0ZTpwcml2YXRlIl0sIm91dGJvdW5kVGFnIjoiZGlyZWN0In0seyJfX25hbWVfXyI6IlByb3h5IGVsc2UiLCJpZCI6IkRERDQyRjc4LTBBMDEtNEQxOC1CRDk5LTczMkYzOTQ5QUZCMCIsInR5cGUiOiJmaWVsZCIsInBvcnQiOiIwLTY1NTM1Iiwib3V0Ym91bmRUYWciOiJwcm94eSJ9XX0=
```
* **all**:
```
eyJkb21haW5TdHJhdGVneSI6IklQSWZOb25NYXRjaCIsImlkIjoiMUJDRUI2MDgtODhERS00NTE4LTlDRkEtMjgyNjVEQ0M1QkVEIiwiYmFsYW5jZXJzIjpbXSwiZG9tYWluTWF0Y2hlciI6Imh5YnJpZCIsIm5hbWUiOiJSdWxlc2V0IiwicnVsZXMiOlt7Il9fbmFtZV9fIjoiQmxvY2sgQWRzIiwiaWQiOiJGNERGNDQ1NS0zMzk1LTQwODYtQjgzNS02MTZCNTAzQkMwRkUiLCJ0eXBlIjoiZmllbGQiLCJkb21haW4iOlsiZ2Vvc2l0ZTpjYXRlZ29yeS1hZHMtYWxsIl0sIm91dGJvdW5kVGFnIjoiYmxvY2sifSx7Il9fbmFtZV9fIjoiRGlyZWN0IHByaXZhdGUgQ0lEUiIsImlkIjoiOTBFQUQ5Q0YtOTcyMS00M0Y4LUIyNUItMzI4ODFGODg5MDdDIiwidHlwZSI6ImZpZWxkIiwiaXAiOlsiZ2VvaXA6cHJpdmF0ZSJdLCJvdXRib3VuZFRhZyI6ImRpcmVjdCJ9LHsiX19uYW1lX18iOiJEaXJlY3QgcHJpdmF0ZSBkb21haW5zIiwiaWQiOiIxQjQwQUZEQS00MjFFLTQ2QUMtOTA0Qy1ERUQzQzNEQzgxMDIiLCJ0eXBlIjoiZmllbGQiLCJkb21haW4iOlsiZ2Vvc2l0ZTpwcml2YXRlIl0sIm91dGJvdW5kVGFnIjoiZGlyZWN0In0seyJfX25hbWVfXyI6IlByb3h5IGVsc2UiLCJpZCI6Ijg3NDBGM0I2LUFEQUEtNDg5RC1BQTExLTVGNTk1N0E4QzQ5NyIsInR5cGUiOiJmaWVsZCIsInBvcnQiOiIwLTY1NTM1Iiwib3V0Ym91bmRUYWciOiJwcm94eSJ9XX0=
```

---

## v2rayN Guide: Custom Routing Setup

Follow these steps to initialize the Russian geo-assets and apply my custom routing configurations.

---

### 1. Download geofiles and default presets
First, you must download the specific .dat files for the region.
1. Open **Settings** > **Regional presets setting**.
2. Select **Russia** from the list. This downloads the necessary `.dat` files.
3. **Note:** This will create default profiles. You can use them, or proceed to the next steps to **overwrite/delete** them with my (or your) custom settings.

### 2. Configure geofiles source (optional, but check if it's set correctly anyways)
1. Open **Settings** > **Option Setting** > **v2rayN settings**.
2. Locate the **Geo files source** dropdown.
3. Select the `runetfreedom/russia-v2ray-rules-dat` option.

![Step 1: Geo Asset Configuration](https://raw.githubusercontent.com/Winterstarf/v2ray-rules/refs/heads/main/images/geofiles_setting.png)

### 3. Import My Custom Rules
To use my specific profiles (overwriting the defaults if desired):
1. Navigate to **Settings** > **Routing Setting**.
2. Click **Add** to create a new profile (or double-click an existing one to overwrite it).
3. **Remark:** Enter a name for the profile.
4. **Domain Strategy:** Choose **IPOnDemand**.
5. **URL:** Paste the raw link of one of the profiles above.
6. Click **Import rules from subscription url**.
7. Select **Append** if you've created a new profile, or **Replace** if you're editing a default preset.

> ### Updating
> When you need to update the rules to the latest version:
> 1. Open your existing routing profile in **Routing Setting**.
> 2. Click **Import rules from subscription url** again.
> 3. When prompted, you **must select Replace** to overwrite the old rules with the updated ones.

![Step 2: Rule Import Process](https://raw.githubusercontent.com/Winterstarf/v2ray-rules/refs/heads/main/images/importing_rules.png)

### 4. Activate the Routing Profile
1. On the main application window, look for the **Routing** dropdown menu at the bottom.
2. Select the custom profile you just created/updated.
3. Enable **Tun Mode** or **System Proxy** depending on your needs.

![Step 3: Activating the Route](https://raw.githubusercontent.com/Winterstarf/v2ray-rules/refs/heads/main/images/using_profiles.png)

---

## v2RayTun guide

### 1. Configure Geo-Asset source
1. Open the app and go to the **Routing** menu.
2. Tap the **Square with an arrow** icon.
3. Locate **Geo files source** and select `runetfreedom/russia-v2ray-rules-dat` from the dropdown list.
4. Tap the **Cloud icon** to start the download. Wait until the `.dat` files are fully updated.

<img src="https://raw.githubusercontent.com/Winterstarf/v2ray-rules/refs/heads/main/images/v2raytun_geo.png" width="350">

### 2. Set domain strategy
1. In the **Routing** menu, find the **Domain Strategy** setting and choose **IPOnDemand**.
2. Copy the chosen Base64 code to your clipboard.
3. In v2RayTun, tap the **three dots menu** (top right).
4. Select **Import ruleset from clipboard**.

<img src="https://raw.githubusercontent.com/Winterstarf/v2ray-rules/refs/heads/main/images/v2raytun_routing.png" width="350">

---

## Trivia & Advanced Usage for v2RayTun, v2rayNG and possibly other apps

* **Custom service outing:** You can manually route specific domains or services by using the **Services** menu on the main screen. This is useful for forcing specific sites through the proxy regardless of global rules.
* **Custom app routing:** In the **Routing** menu, you can choose exactly which apps on your device use the proxy. 
    * **Routing of selectyed applications:** If you choose this, remember to select your browser (Chrome, Firefox, etc.) and any other apps that need to bypass blocks.
    * **Bypass Mode:** Useful if you want everything proxied except for local Russian apps (like banking or government services).
