# EC Shipping Widget

A lightweight Drupal Commerce module that enhances shipping method selection with descriptions and improved theming capabilities.

## Overview

By default, Drupal Commerce displays shipping methods as simple radio buttons with labels only. This module extends the shipping method widget to include rate descriptions below each option, making the checkout process more user-friendly and informative.

## Features

- **Enhanced Display**: Shows shipping method descriptions (Rate Description field) alongside radio button labels
- **Clickable Area**: The entire label and description area acts as a clickable region for better UX
- **Easy Theming**: Provides a dedicated template for customization without additional hooks
- **Native Compatibility**: Maintains standard widget behavior, including Ajax support
- **Clean Styling**: Includes basic CSS with hidden radio inputs for a modern look
- **Zero Dependencies**: Only requires `commerce_shipping` module

## Requirements

- Drupal ^10 || ^11
- Commerce Shipping module

## Installation

1. Download and place the module in `/modules/custom/ec_shipping_widget`
2. Enable the module: `drush en ec_shipping_widget`

## Configuration

No additional configuration needed. The module automatically:
- Detects available shipping methods
- Retrieves "Rate Description" from shipping method configuration (e.g., `admin/commerce/shipping-methods/manage/1`)
- Displays descriptions below each shipping method option during checkout

## Theming

Override the template in your theme for custom styling:

```
your_theme/templates/form-element--radio--shipping-method.html.twig
```

Default CSS classes:
- `.shipping-method-item` - Container
- `.shipping-method-label` - Label text
- `.shipping-method-description` - Description text

## How It Works

1. Alters `commerce_checkout_flow` forms
2. Provides a theme suggestion for shipping method radio buttons
3. Applies minimal styling for consistent presentation
4. Displays rate descriptions from shipping method configuration

## License

This project is licensed under the GPL-2.0+.

## Author

Pavel Kasianov.

Linkedin: https://www.linkedin.com/in/pkasianov/</br>
Drupal org: https://www.drupal.org/u/pkasianov

## Support

For issues or feature requests, please contact the module maintainer.
