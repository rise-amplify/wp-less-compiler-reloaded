
# WP Less Compiler (Patched Fork)

Compiles LESS into CSS for WordPress themes. Allows administrators to output LESS for themselves and CSS for all other users.

> ⚠️ This is a patched fork of the original `wp-less-compiler` plugin (v1.3.0) by Tyler Bruffy.  
> It includes essential security updates and is safe for production use.

---

## ✨ Features

- Compile LESS files to CSS within WordPress
- Support for admin-only LESS rendering
- File hash checking to detect changes
- Lightweight and easy to configure

---

## 🔒 Security Updates in 1.3.1

This release includes crucial security patches to address an [XSS vulnerability reported by Patchstack](https://patchstack.com/database/wordpress/plugin/wp-less-compiler/vulnerability/wordpress-wp-less-compiler-plugin-1-3-0-cross-site-scripting-xss-vulnerability?_a_id=350):

- Escaped all HTML output using `esc_attr()` and `esc_html()`
- Sanitized all user input using `sanitize_text_field()` before processing
- Audited `SettingsHtml.php`, `Processor.php`, and `SettingsStyle.php` for best practices

---

## 📦 Installation

1. Download the plugin ZIP
2. Upload to your WordPress site under **Plugins > Add New > Upload**
3. Activate the plugin
4. Configure LESS/CSS files via **Settings > Less Compiler**

---

## 📜 Changelog

### 1.3.1
- Security patch release
- Escaped all HTML output in admin panel
- Sanitized all `$_POST` input values
- Updated `SettingsHtml.php`, `Processor.php`, `SettingsStyle.php`

---

## 🧩 Credits

Originally authored by Tyler Bruffy  
Patched and maintained by [Tom Dent](mailto:tom.dent@riseandamplify.co.uk)
