# Samsung A127F Recovery Builder

This repository is configured to build Android recovery images for the Samsung Galaxy A12 / SM-A127F via GitHub Actions.

## Device target
- Model: Samsung Galaxy A12 / SM-A127F
- Codename: a12s
- Board platform: Exynos 850
- Recommended device tree: https://github.com/loongruige/twrp_device_samsung_a12s

## Supported recoveries
- TWRP
- SHRP
- PBRP
- OrangeFox
- Multi-recovery all-in-one runner

## Quick start
1. Open the repository in GitHub.
2. Go to Actions.
3. Run the workflow you want.
4. Enter the default device values or replace them with yours.
5. Wait for the build to complete.
6. Download the generated image from the workflow artifacts or release page.

## Default values for SM-A127F
- Device tree: https://github.com/loongruige/twrp_device_samsung_a12s
- Device tree branch: master
- Device path: device/samsung/a12s
- Device name: a12s
- Makefile: omni_a12s
- Build target: recovery

## Notes
- This repository is intended to automate recovery compilation in GitHub-hosted runners.
- Use the device tree that matches your exact firmware and device variant.
- LDCHECK can help diagnose missing libraries and encryption-related dependencies.
- TWRP is the most reliable starting point for this device.

## Recommended flow
1. Build TWRP first
2. Validate boot and functionality
3. Then build SHRP, PBRP, or OrangeFox if needed
4. Keep the best-performing recovery as your primary custom recovery
