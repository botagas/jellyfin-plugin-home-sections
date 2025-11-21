# Using This Plugin Repository

## Option 1: Manual Installation (Recommended for Testing)

1. Download the latest `.zip` file from the [Releases page](https://github.com/botagas/jellyfin-plugin-home-sections/releases)
2. Extract the contents to your Jellyfin plugins folder:
   - **Windows**: `%AppData%\Jellyfin\Server\plugins\HomeScreenSections\`
   - **Linux**: `/var/lib/jellyfin/plugins/HomeScreenSections/`
   - **Docker**: `/config/plugins/HomeScreenSections/`
3. Restart Jellyfin
4. The plugin will appear in Dashboard → Plugins

## Option 2: Add Custom Repository to Jellyfin

Add this repository URL to Jellyfin to install and update the plugin directly from the catalog:

### Repository URL
```
https://raw.githubusercontent.com/botagas/jellyfin-plugin-home-sections/main/manifest.json
```

### Steps to Add:
1. Go to Jellyfin Dashboard
2. Navigate to **Plugins** → **Repositories**
3. Click the **+** button
4. Enter:
   - **Repository Name**: `Home Screen Sections`
   - **Repository URL**: `https://raw.githubusercontent.com/botagas/jellyfin-plugin-home-sections/main/manifest.json`
5. Click **Save**
6. Go to **Catalog** tab
7. Find **Home Screen Sections** and click **Install**

## Option 3: Submit to Official Jellyfin Repository

To make your plugin available in the default Jellyfin catalog, submit a PR to:
https://github.com/jellyfin/jellyfin-plugin-repository

You'll need to add your plugin's manifest information to their repository manifest file.

## Configuring External URL for Jellyseerr

After installation:

1. Go to Dashboard → Plugins → Home Screen Sections
2. Expand the **Jellyseerr** section under Advanced Settings
3. Configure:
   - **Jellyseerr URL (Internal)**: Your internal Jellyseerr address (e.g., `http://jellyseerr:5055`)
   - **Jellyseerr URL (External)**: Your public-facing URL (e.g., `https://requests.yourdomain.com`)
   - **Jellyseerr API Key**: Your API key from Jellyseerr

The plugin will use the internal URL for backend API requests and the external URL for frontend links.
