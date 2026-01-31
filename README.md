# TableTime Pro - Venue Portal

Manager reporting and analytics portal for TableTime Pro.

## Files

```
venue.tabletimepro.com/
├── index.html      ← Main app (all dependencies inline)
├── manifest.json   ← PWA manifest
├── netlify.toml    ← Netlify config
└── icons/          ← Add your app icons here
    ├── favicon.ico
    ├── icon-192.png
    └── icon-512.png
```

## Deployment

1. Push these files to your GitHub repo
2. Connect to Netlify
3. Deploy!

No build step required - it's all static HTML/CSS/JS.

## Features

- **Reports Tab**: Filter sessions by date, view KPIs, export CSV
- **Audit Log Tab**: View all logged actions with timestamps
- **Analytics Tab**: Revenue by table, staff performance, summary stats
- **Manager Auth**: Supports deep linking from Staff App with authentication

## Integration with Staff App

Managers can access this portal from the Staff App by clicking the "Reports" button. The Staff App passes authentication via URL params:

```
https://venue.tabletimepro.com/?tenant=xxx&role=manager&user=ManagerName
```

The portal will show:
- Auth banner with manager name
- "Back to Staff App" button
- Full access to all tabs

## Data Storage

Uses IndexedDB (same as Staff App) to read session data. The portal shares the same database as the Staff App when accessed on the same device/browser.
