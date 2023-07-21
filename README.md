# Linksys Smart Device Tracker for Home Assistant - Hassio Integration

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

This repository provides an enhanced version of the Linksys smart device tracker for Home Assistant, specifically designed to handle authorization issues in the original integration.

For additional information about the original Linksys Smart integration, please refer to [Home Assistant's official documentation](https://www.home-assistant.io/integrations/linksys_smart).

## Problem Statement

The standard Linksys smart device tracker was previously experiencing problems due to a lack of required authorization handling. This repository provides a robust solution to this issue by implementing the necessary authorization process.

## New Configuration Format

The new configuration format includes the `username` and `password` fields to allow for the required authorization. See the example below:

```yaml
device_tracker:
  - platform: linksys_smart
    host: 192.168.1.1
    username: admin
    password: password
```
**Note:** Please replace `192.168.1.1`, `admin`, and `password` with your actual Linksys device's IP, username, and password respectively.

## Pending Official Change

We have submitted a change request for the official integration. Until it's accepted and deployed, you can use this customized version to benefit from the enhanced functionality.

## Custom Installation

In the meantime, this custom integration can be installed via the Home Assistant Community Store (HACS) using a custom repository. Here's how to do it:

1. Open HACS in your Home Assistant frontend.
2. Click on the three dots in the top right corner, then select 'Custom Repositories'.
3. In the 'Add Custom Repository' field, enter the following URL: `https://github.com/sideshot/hassio-linksys-smart-device-tracker.git`
4. Choose 'Integration' from the 'Category' dropdown menu and then click 'Add'.
5. Navigate back to the 'Integrations' page.
6. Click on the '+ Explore & Add Repositories' button at the bottom right.
7. Search for 'hassio-linksys-smart-device-tracker' and click on it.
8. Click on 'Install this repository in HACS'.
9. Wait for the installation to complete and then restart Home Assistant.

Now, the Linksys smart device tracker should work without any authorization issues. Enjoy!

## Contributing

We encourage you to contribute to this project! Please check out the [Contributing to Hassio-Linksys-Smart-Device-Tracker](CONTRIBUTING.md) guide for guidelines about how to proceed.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
