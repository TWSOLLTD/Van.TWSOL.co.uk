# Van Inventory Management System

A modern, responsive web application for managing van stock inventory with real-time synchronization and offline capabilities.

## 🚀 Features

- **Modern UI**: Card-based layout with responsive design
- **Real-time Search**: Filter items by name or stock status
- **Admin Panel**: Secure password-protected management interface
- **Offline Support**: Works without internet using local storage
- **Auto Sync**: Background synchronization with cloud storage
- **Statistics Dashboard**: Real-time inventory statistics
- **Email Reports**: Send restock requests via email
- **Status Indicators**: Visual stock level indicators

## 📁 Project Structure

```
Van.TWSOL.co.uk/
├── index.html              # Main application
├── inventory.json          # Default inventory data
├── netlify.toml           # Netlify configuration
├── netlify/               # Netlify functions
│   └── functions/
│       ├── inventory.js   # Main inventory API
│       └── package.json   # Function dependencies
├── README.md              # This file
└── SETUP.md              # Setup instructions
```

## 🛠️ Setup Instructions

### Quick Start (Local Only)
1. Open `index.html` in your browser
2. Start managing inventory!

### Full Setup (With Cloud Sync)
See [SETUP.md](SETUP.md) for detailed instructions.

## 🔧 Configuration

### Admin Access
- **Password**: `T7S` (stored as base64 hash)
- **Access**: Click "Admin Access" button

### Data Storage Options
1. **Local Storage Only** (default) - Works immediately
2. **Airtable + Netlify Functions** - Cloud sync with spreadsheet
3. **JSON File** - Version controlled data storage

## 📊 Inventory Management

### Adding Items
1. Click "Admin Access" and enter password
2. Fill in item details (name, min stock, current stock)
3. Click "Add Item"

### Taking Items
- Click "Take 1" for single items
- Click "Take X" for multiple items
- Items below minimum stock show "Replace" buttons

### Replacing Items
- Click "Replace 1" to add one item
- Click "Replace All" to restore to minimum stock
- Use "Send Replace List" to email restock requests

## 🎨 UI Features

### Search & Filter
- **Search**: Type to filter by item name
- **Filters**: All Items / Low Stock / Out of Stock
- **Real-time**: Results update as you type

### Status Indicators
- **Green**: In stock (above minimum)
- **Yellow**: Low stock (below minimum)
- **Red**: Out of stock (zero items)

### Statistics Dashboard
- Total items in inventory
- Low stock items count
- Out of stock items count
- Total stock count

## 🔒 Security

- Admin password is base64 encoded (not plain text)
- Environment variables for API keys
- CORS protection on API endpoints
- Input validation and sanitization

## 🌐 Deployment

### Netlify (Recommended)
1. Connect GitHub repository to Netlify
2. Set build settings:
   - **Publish directory**: `.` (root)
   - **Functions directory**: `netlify/functions`
3. Add environment variables (if using cloud sync)
4. Deploy!

### Other Hosting
- Upload all files to any web server
- Works with any static hosting service

## 🔧 Development

### Local Development
1. Open `index.html` in browser
2. Make changes and refresh

### Testing Functions
1. Install Netlify CLI: `npm install -g netlify-cli`
2. Run: `netlify dev`
3. Test functions locally

## 📝 Data Format

Inventory items are stored as JSON:
```json
{
  "name": "Item Name",
  "minStock": 5,
  "currentStock": 3
}
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📄 License

This project is open source and available under the MIT License.

## 🆘 Support

For issues or questions:
1. Check the [SETUP.md](SETUP.md) guide
2. Review browser console for errors
3. Check Netlify function logs (if using cloud sync)
4. Create an issue in the repository

---

**Built with ❤️ for efficient van inventory management**
