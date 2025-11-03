# OJS Admin Panel - Matrix Edition

A modern, security-focused admin panel for Open Journal Systems (OJS) with a stunning Matrix-themed interface featuring glitch effects and real-time monitoring.

![Matrix Theme](https://img.shields.io/badge/Theme-Matrix-00ff00?style=for-the-badge)
![PHP](https://img.shields.io/badge/PHP-7.4+-777BB4?style=for-the-badge&logo=php)
![License](https://img.shields.io/github/license/pigeonposse/onlyfit?style=for-the-badge&color=green&logoColor=white)

## Features

### UI/UX
- **Matrix Rain Background** - Animated falling characters creating an immersive cyberpunk atmosphere
- **Glitch Effects** - Interactive glitch animations on buttons, inputs, and cards
- **Security Terminal Aesthetic** - Grid overlays, scanning lines, and pulsing indicators
- **Responsive Design** - Fully optimized for desktop and mobile devices
- **Modern Dashboard** - Clean, intuitive interface with real-time statistics

### User Management
- **Create Users** - Add new Admin or Manager accounts with custom credentials
- **Edit Roles** - Change user roles between Admin and Manager with one click
- **Reset Passwords** - Generate secure random passwords for any user
- **Delete Users** - Remove users with confirmation and audit logging
- **User Statistics** - Real-time overview of total users and role distribution

### Security Features
- **Session Management** - Secure PHP sessions with timeout protection
- **Password Hashing** - MD5 hashing compatible with OJS standards
- **Access Control** - Role-based permissions (Admin/Manager)
- **CSRF Protection** - Form validation and security checks

### Monitoring & Logging
- **Activity Tracking** - Complete audit trail of user changes
- **Statistics Dashboard** - Visual overview of user metrics
- **Action Logging** - Detailed logs with timestamps and user info

### Database Support
- **OJS2 Compatible** - Full support for legacy OJS2 schema
- **OJS3 Compatible** - Modern OJS3 database structure support
- **Auto-Detection** - Automatically detects and adapts to your OJS version
- **Multi-Database** - Handles both user and role tables seamlessly

## Requirements

- PHP 7.4 or higher
- MySQL/MariaDB database
- OJS2 or OJS3 installation
- Web server (Apache/Nginx)

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/Sw4CyEx/OJS-ADMIN-CREATOR.git
cd OJS-ADMIN-CREATOR
```

### 2. Configure Database Connection

Edit the database configuration in `user.inc.php`:

```php
$host = 'localhost';
$dbname = 'your_ojs_database';
$username = 'your_db_username';
$password = 'your_db_password';
```

### 3. Upload to Server

Upload `user.inc.php` to your OJS installation directory or any web-accessible folder.

### 4. Set Permissions

```bash
chmod 644 user.inc.php
```

### 5. Access the Panel

Navigate to: `https://yourdomain.com/path/to/user.inc.php`

Default credentials will be your existing OJS admin account.

## Usage

### Login
1. Navigate to the admin panel URL
2. Enter your OJS admin credentials
3. Experience the Matrix-themed login with glitch effects

### Dashboard Overview
- View total users and role distribution
- Monitor recent activity
- Access quick actions

### Creating Users
1. Fill in the "Create New User" form
2. Enter username, password, email, and full name
3. Select role (Admin or Manager)
4. Click "CREATE USER" button

### Managing Users
- **Edit Role**: Click "EDIT ROLE" button, select new role, confirm
- **Reset Password**: Click "RESET PWD", new password generated automatically
- **Delete User**: Click "DELETE", confirm action in modal

## 🔧 Configuration

### Customizing Colors

The Matrix theme uses CSS variables. Edit the `:root` section in the `<style>` tag:

```css
:root {
  --matrix-green: #00ff41;
  --matrix-dark: #0d0208;
  --matrix-glow: rgba(0, 255, 65, 0.5);
}
```

### Adjusting Glitch Effects

Modify the glitch animation intensity in the CSS:

```css
@keyframes glitch {
  /* Adjust clip-path values for different effects */
}
```

### Session Timeout

Change session timeout duration (default: 30 minutes):

```php
if (time() - $_SESSION['last_activity'] > 1800) { // 1800 = 30 minutes
```

## Security Considerations

1. **Change Default Credentials** - Ensure you're using strong, unique passwords
2. **HTTPS Only** - Always use SSL/TLS encryption in production
3. **Restrict Access** - Use `.htaccess` or server config to limit IP access
4. **Regular Updates** - Keep PHP and database software updated
5. **Backup Database** - Regular backups before making bulk changes
6. **File Permissions** - Ensure proper file permissions (644 for PHP files)

## Screenshots

<!-- Add your screenshots here -->
![Login Page](https://raw.githubusercontent.com/Sw4CyEx/OJS-ADMIN-CREATOR/refs/heads/main/ojs-login.png)
![Dashboard](https://raw.githubusercontent.com/Sw4CyEx/OJS-ADMIN-CREATOR/refs/heads/main/ojs-dashboard.png)
![User Management](https://raw.githubusercontent.com/Sw4CyEx/OJS-ADMIN-CREATOR/refs/heads/main/ojs-dashboard-users.png)

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 Changelog

### Version 2.0.0 (Current)
- Matrix-themed UI with glitch effects
- Edit role functionality
- Enhanced dashboard with statistics
- Improved mobile responsiveness
- Security enhancements

### Version 1.0.0
- Initial release
- Basic user management
- Simple dashboard

## Known Issues

- Matrix rain effect may impact performance on older devices
- Some glitch effects may not work on Safari < 14

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author

Created with 💚 by Ayana

## Acknowledgments

- Inspired by The Matrix movie franchise
- Built for the Open Journal Systems community
- Special thanks to all contributors

## Support

For issues, questions, or suggestions:
- Open an issue on GitHub
- Contact: [Telegram](https://t.me/latief777)
- Discord: ayana__

## Links

- [OJS Official Website](https://pkp.sfu.ca/ojs/)
- [Documentation](https://docs.pkp.sfu.ca/)

---

**⚠️ Disclaimer**: This is an unofficial admin panel for OJS. Use at your own risk. Always backup your database before making changes.

**Made with 💚 and lots of Matrix references**
