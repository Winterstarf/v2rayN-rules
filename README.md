## Rule Profiles

Choose the configuration that best fits your traffic needs:

| Profile | Description
| :--- | :--- 
| **Blocked Only** | Proxies only known blocked domains and CIDR ranges.
| **Except Russia** | Proxies all traffic except for Russian domains and IP space.
| **Everything** | Routes all traffic through the proxy.

### Subscription Links
* **blocked.json**: `https://raw.githubusercontent.com/Winterstarf/v2rayN-rules/refs/heads/main/blocked.json`
* **except_ru.json**: `https://raw.githubusercontent.com/Winterstarf/v2rayN-rules/refs/heads/main/except_ru.json`
* **everything.json**: `https://raw.githubusercontent.com/Winterstarf/v2rayN-rules/refs/heads/main/everything.json`

---

## Installation Guide

### 1. Configure Geo-Asset Sources
1. Open **Settings** > **Option Setting** > **v2rayN settings**.
2. Locate the **Geo files source** dropdown.
3. Select the `runetfreedom/russia-v2ray-rules-dat` option.
4. Save settings to initiate the `.dat` file download.

![Step 1: Geo Asset Configuration](https://raw.githubusercontent.com/Winterstarf/v2rayN-rules/refs/heads/main/images/geofiles_setting.png)

### 2. Import Routing Rules
1. Navigate to **Settings** > **Routing Setting**.
2. Click the **Add** button.
3. Enter a custom name in the **Remark** field (e.g., "RU-Bypass").
4. Paste the raw GitHub link for your chosen profile into the **URL** field.
5. Click **Import rules from subscription url**.
6. Select **Append** when prompted, then click **Confirm**.

![Step 2: Rule Import Process](https://raw.githubusercontent.com/Winterstarf/v2rayN-rules/refs/heads/main/images/importing_rules.png)

### 3. Activate the Profile
1. On the main application window, locate the **Routing** dropdown at the bottom.
2. Select the profile you just created.
3. Enable **Tun Mode** or **System Proxy** depending on your specific requirements.

![Step 3: Activating the Route](https://raw.githubusercontent.com/Winterstarf/v2rayN-rules/refs/heads/main/images/using_profiles.png)
