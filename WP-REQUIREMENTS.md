# WordPress Project Requirements

This project tracks runtime dependencies (themes/plugins) outside of Git to keep the repository lean and environment-agnostic. Use WP‑CLI to install exact versions.

## Core
- WordPress core (as included in repo)
- Database: SQLite via MU plugin (`wp-content/db.php`) and `wp-content/mu-plugins/sqlite-database-integration/`

## Theme
- Astra (activate)

Install:
```
wp theme install astra --activate
```

## Plugins
- Elementor (core)
- Advanced Custom Fields (ACF)
- Custom Post Type UI (CPT UI)
- Contact Form 7
- WP Super Cache
- Complianz – GDPR/CCPA

Install & activate:
```
wp plugin install elementor advanced-custom-fields custom-post-type-ui contact-form-7 wp-super-cache complianz-gdpr --activate
```

## Basic Settings (recommended)
```
wp language core install el
wp site switch-language el
wp option update timezone_string "Europe/Athens"
wp rewrite structure "/%postname%/" --hard
wp rewrite flush --hard
```

## Optional
- If you add a custom child theme, unignore its folder in `.gitignore`.
- Media uploads are ignored; add seed content via import or include only small sample assets.
