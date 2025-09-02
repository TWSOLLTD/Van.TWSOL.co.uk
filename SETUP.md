# Van Inventory Management - Setup Guide

## 🚀 Perfect for Netlify Hosting

This solution uses **Netlify Functions + Airtable** which is ideal for your Netlify hosting setup.

## 📋 Setup Steps

### 1. Create Airtable Base ✅ (DONE)
You already have your base: `appdywaPsOozIdDzH/tblOocYELtWE6W50l`

### 2. Create Personal Access Token
1. Go to [Airtable.com/account](https://airtable.com/account)
2. Click "Personal access tokens"
3. Click "Create new token"
4. Give it a name like "Van Inventory"
5. Select your base: `appdywaPsOozIdDzH`
6. Set permissions to "data.records:read" and "data.records:write"
7. Copy the token (it starts with `pat_`)

### 3. Configure Netlify Environment Variables
1. In your Netlify dashboard, go to your site settings
2. Go to "Environment variables"
3. Add these variables:
   - `AIRTABLE_PERSONAL_ACCESS_TOKEN` = your personal access token (starts with `pat_`)
   - `AIRTABLE_BASE_ID` = `appdywaPsOozIdDzH`

### 4. Deploy to Netlify
1. Push your code to GitHub
2. Netlify will automatically deploy
3. The function will be available at `/.netlify/functions/inventory`

## ✅ Benefits of This Solution

- **Free**: Airtable free tier (1,200 records) + Netlify free tier
- **Real-time**: Auto-syncs every 30 seconds
- **Offline Support**: Works without internet using local storage
- **Easy Management**: View/edit data in Airtable spreadsheet
- **No Database Setup**: Airtable handles everything
- **Secure**: Tokens stored in Netlify environment variables

## 🔧 How It Works

1. **Local Storage**: Data is saved locally first (instant)
2. **Auto Sync**: Syncs with Airtable every 30 seconds
3. **Offline Mode**: Works without internet
4. **Status Indicator**: Shows sync status (Online/Offline/Syncing)

## 📊 Data Management

- **View Data**: Open your Airtable base to see all inventory
- **Edit Data**: Make changes directly in Airtable
- **Backup**: Data is automatically backed up in Airtable
- **Export**: Export to Excel, CSV, or other formats

## 🆘 Troubleshooting

### Function Not Working?
1. Check Netlify function logs in dashboard
2. Verify environment variables are set
3. Check Airtable personal access token and base ID

### Sync Issues?
1. Check internet connection
2. Verify Airtable permissions
3. Check browser console for errors

## 🎯 Alternative: Simple JSON File

If you prefer not to use Airtable, you can also:

1. **Use Netlify's built-in storage** (limited but free)
2. **Store in a JSON file** in your repo
3. **Use GitHub as a simple database**

Would you like me to implement any of these alternatives instead?
