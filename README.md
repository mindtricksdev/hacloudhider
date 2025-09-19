# Home Assistant Cloud Hider

[![hacs_badge](https://img.shields.io/badge/HACS-Custom-orange.svg)](https://github.com/custom-components/hacs)

A simple HACS frontend integration that hides the "Home Assistant Cloud" menu item from your Home Assistant sidebar.

## Why?

If you prefer not to see the Home Assistant Cloud option in your sidebar menu, this integration will cleanly hide it from view while keeping all other functionality intact.

## Features

- ✅ Automatically hides the "Home Assistant Cloud" menu item
- ✅ Works across all Home Assistant pages and navigation
- ✅ Handles dynamic sidebar updates and route changes
- ✅ Lightweight and efficient
- ✅ No configuration needed

## Installation

### HACS (Recommended)

1. Open HACS in your Home Assistant instance
2. Go to "Frontend" section
3. Click the three dots menu (⋮) in the top right corner
4. Select "Custom repositories"
5. Add this repository URL: `https://github.com/mindtricksdev/hacloudhider`
6. Select "Frontend" as the category
7. Click "Add"
8. Find "Home Assistant Cloud Hider" in the list and click "Download"
9. Restart Home Assistant

### Manual Installation

1. Download the `cloud_hider.js` file from the latest release
2. Copy it to your `config/www/` directory
3. Add the following to your `configuration.yaml`:

```yaml
frontend:
  extra_module_url:
    - /local/cloud_hider.js
```

4. Restart Home Assistant

## How it Works

The integration uses a lightweight JavaScript module that:

1. Monitors the DOM for the Home Assistant Cloud menu item
2. Hides it using CSS `display: none`
3. Continues to monitor for navigation changes and sidebar updates
4. Re-hides the element if it reappears during dynamic updates

The script is designed to be efficient and only runs the hiding logic when necessary.

## Compatibility

- ✅ Home Assistant 2023.1+
- ✅ All modern browsers
- ✅ Works with custom themes
- ✅ Compatible with other frontend integrations

## Troubleshooting

### The Cloud menu item still appears

- Ensure you've restarted Home Assistant after installation
- Check browser console for any JavaScript errors
- Try clearing your browser cache
- Verify the integration is properly loaded in HACS

### Need to access Home Assistant Cloud settings?

You can still access Home Assistant Cloud settings directly via URL: `/config/cloud`

## Contributing

Issues and pull requests are welcome! Please feel free to contribute improvements or report bugs.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

If you find this integration useful, consider:

- ⭐ Starring this repository
- 🐛 Reporting issues
- 💡 Suggesting improvements

---

**Note**: This integration only hides the visual menu item. It does not disable or affect Home Assistant Cloud functionality in any way.
