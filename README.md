# upstream — Pristine bcmdhd driver for Huawei P9

![image](png/p9.png)

Unmodified Broadcom BCM43455 `bcmdhd` Wi-Fi driver as shipped in the
Huawei P9 kernel source tree. **No patches, no modifications.**

## Source

Extracted verbatim from:

- Repo:   https://gitlab.com/vvvbbbcz/android_kernel_huawei_hi3650
- Branch: `upstream`
- Path:   `drivers/huawei_platform/connectivity/bcm/wifi/driver/bcmdhd/`

## Purpose

This branch exists **only as a diff baseline**.

To see what was changed for native monitor + injection support, compare
this branch against `main`:

    git diff upstream main -- bcmdhd/wl_cfg80211.c
    git diff upstream main -- bcmdhd/dhd_linux.c
    git diff upstream main -- bcmdhd/wl_cfg80211.h

Or fetch the ready-made patches from the `main` branch under `patches/`.

## Device reference

| Field | Value |
|-------|-------|
| Device | Huawei P9 (EVA-L09 / EVA-L19 / EVA-AL00) |
| SoC | Kirin 955 |
| Wi-Fi | Broadcom BCM43455 (SDIO) |
| Kernel | Linux 4.4.53 (EMUI 8 / Android 8) |

## License

GPL-2.0 — same as the upstream kernel source.
