
# System Tweaks

## IMPROVING SYSTEM PERFORMANCE

Disables Z-RAM, Window Blur Effects, and animations:

```sh
adb shell settings put global zram_enabled 0
adb shell settings put global accessibility_reduce_transparency 1
adb shell settings put global disable_window_blurs 1
adb shell settings put global window_animation_scale 0.0
adb shell settings put global transition_animation_scale 0.0
adb shell settings put global animator_duration_scale 0.0
adb shell settings put system screen_auto_brightness_adj 1.0
```

---

## DISABLING ANDROID SCREEN SAVER TO GET BETTER BATTERY LIFE

```sh
adb shell settings put secure screensaver_enabled 0
adb shell settings put secure screensaver_activate_on_sleep 0
adb shell settings put secure screensaver_activate_on_dock 0
```

---

## Speed up Long Press Delay

```sh
adb shell settings put secure long_press_timeout 250
adb shell settings put secure multi_press_timeout 250
```

---

## Google Optimization (change from 0 to 1 if you wanna enable something)

Disable android auto:

```sh
adb shell settings put system gearhead:driving_mode_settings_enabled 0
```

GSM Tweak:

```sh
adb shell settings put secure assistant 0
adb shell settings put secure smartspace 0
adb shell settings put global google_core_control 0
adb shell settings put secure adaptive_connectivity_enabled 0
```

---

## Disabling Online Manual URL and Remote Support

```sh
adb shell settings put global online_manual_url 0
adb shell settings put system remote_control 0
```

---

## Improve app launch times

```sh
adb shell settings put global activity_starts_logging_enabled 0
adb shell settings put secure send_action_app_error 0
adb shell settings put global bixby_pregranted_permissions 0
adb shell settings put system send_security_reports 0
adb shell settings put system rakuten_denwa 0
```

---

## Killing Game Optimizing Service

```sh
adb shell settings put secure game_auto_temperature_control 0
adb shell pm clear --user 0 com.samsung.android.game.gos
adb shell settings put secure gamesdk_version 0
adb shell settings put secure game_home_enable 0
adb shell settings put secure game_bixby_block 1
```

---

## OLED Screen Tweak

```sh
adb shell settings put global burn_in_protection 1
```

---

## Improve Touchscreen Responsiveness and Latency

```sh
adb shell settings put secure tap_duration_threshold 0.0
adb shell settings put secure touch_blocking_period 0.0
```

---

## Disable Background Scanning for Devices

```sh
adb shell settings put system nearby_scanning_permission_allowed 0
adb shell settings put system nearby_scanning_enabled 0
adb shell settings put global ble_scan_always_enabled 0
```

---

## Disable hotword detection

```sh
adb shell settings put global hotword_detection_enabled 0
```

---

## Disable Android's Motion Engine Sensor (optional)

```sh
adb shell settings put system master_motion 0
adb shell settings put system motion_engine 0
adb shell settings put system air_motion_engine 0
adb shell settings put system air_motion_wake_up 0
adb shell settings put system intelligent_sleep_mode 0
adb shell settings put secure adaptive_sleep 0
```

---
