<p align="center">
  <img src="assets/app-icon-256.png" alt="YomVezman app logo" width="160" height="160">
</p>

# YomVezman

Hebrew dates, festivals and daily prayer times in a native Mac calendar.

**Public preview — 0.8.2-preview.1.** A feature-freeze prerelease for testing, not a finished release or an App Store-approved build. [Website](https://webservices-org.github.io/yomvezman-releases/) · [Download and release notes](https://github.com/WEBServices-ORG/yomvezman-releases/releases/tag/v0.8.2-preview.1).

The DMG contains app version **0.8.2 (12)**. The preview label identifies this distribution; it does not change the signed app version.

## App preview

[![YomVezman full-screen calendar with Hebrew dates and Jerusalem prayer times](assets/yomvezman-0.6.1-calendar-1920.jpg)](https://webservices-org.github.io/yomvezman-releases/assets/yomvezman-0.6.1-calendar.jpg)

YomVezman 0.6.1 · Jerusalem sample calendar. Open the image to view it at full size.

## Requirements

- A Mac with Apple silicon (M-series).
- macOS 14 or later.
- Internet access to load fresh calendar events and default prayer times. Previously loaded matching information can be used offline and is labeled as saved data.

## Install

1. Download the [Apple-silicon DMG](https://github.com/WEBServices-ORG/yomvezman-releases/releases/download/v0.8.2-preview.1/YomVezman-0.8.2-12-arm64.dmg).
2. Open the DMG and drag YomVezman to Applications.
3. Eject the disk image and open YomVezman from Applications.
4. Choose a city and timezone. Check the Israel/diaspora schedule, candle-lighting offset and Havdalah method for your practice.

This preview is Developer ID signed and notarized by Apple. Notarization is a security check; it is not App Store review or certification of calendar calculations. If macOS reports a damaged app, an unidentified developer or a failed security check, stop and contact support. Do not disable Gatekeeper or remove quarantine attributes to force the app open.

## Use

New in 0.8.2: the Psalms reader now reaches the final verse of the daily portion, including at maximum text size. Native Hebrew Home/End checks passed for the original failing case and the longest daily portion.

New in 0.8.1: oversized calendar downloads are bounded during transfer, preserving other requests and exact-request saved fallback. This is a reliability patch within the feature freeze.

New in 0.8.0: **View > Daily Psalms** opens the selected day’s Hebrew monthly reading offline. All 150 chapters / 2,527 verses come from Sefaria’s explicitly selected **Tanach with Nikkud** edition (Public Domain; source tanach.us), with exact references and attribution. No generated text or English translation is included. Adjust text size, or Tab into the text and use Up/Down by verse and Home/End. Reading uses the selected city’s daytime date; no reading history is stored.

Browse Hebrew or Gregorian months with both dates displayed. Switch between English and Hebrew and use the window's full-screen control. Select a day for its events and prayer times. The year panel includes festival dates, Hebrew-year information and a traditional molad table.

Open Settings with Command-comma. Location edits are drafts until saved. Map and current-location lookup are optional; manual location entry is available. Display and menu-bar choices apply immediately. The optional menu-bar date follows sunset at the selected location; an asterisk indicates that sunset is unavailable and the daytime date is displayed.

To remove local calendar data, open Settings > Saved data > Remove saved calendar data. Read the confirmation before continuing. This removes saved location/preferences and downloaded source responses; you will need to choose a city again. It does not erase records held by Apple or Hebcal or change macOS location permission.

Calendar events and default times come from [Hebcal](https://www.hebcal.com/). Optional custom daily calculations run locally. Check the selected location, timezone and method against your community's practice. Unavailable solar events are shown explicitly.

## Updates

Choose YomVezman > Check for Updates to see available versions and release notes. Optional automatic checks at launch are off by default. In 0.4.0 and later, choose Update, then Install Update and Install and Relaunch. Versions through 0.3.0 require one manual DMG installation to gain this capability. Installation always requires confirmation.

## Support development

If you find YomVezman useful, you can [support its development via PayPal](https://www.paypal.com/ncp/payment/VRVYW4BB3CH3L). Contributions are optional.

## Support and privacy

For app support or privacy questions, email [beacons_mobile_9k@icloud.com](mailto:beacons_mobile_9k@icloud.com). Read the [privacy notice](https://webservices-org.github.io/yomvezman-releases/privacy.html). Do not post private locations, credentials or other sensitive information in public issue reports. Useful reports include the app version, macOS version, the steps taken and what happened.

## Repository scope

This repository distributes the Mac app and its website. The application's source repository is private. No affiliation with another calendar application or religious certification is claimed.

## Testing status and limitations

96 automated tests pass, including live calendar integration, festival lengths, calculation comparisons, polar-boundary cases and saved-data reset/recovery. Both converters passed isolated English/Hebrew full-screen checks. See release notes for remaining acceptance limits.

Introduced in 0.7.0: View > Date converter compares exact dates across years; View > Festival converter compares full daytime festival ranges across up to ten Hebrew years using the selected city and Israel/diaspora setting. Editing a festival year range requires Load again. Missing dates and source-unavailable states are explicit.

Introduced in 0.6.1: About YomVezman is available from the application and date-status menus. It shows the running version/build, app icon, credits, bundled Sparkle license, privacy and support links. English/Hebrew layouts and keyboard dismissal passed native checks; status-item-only invocation and broader recovery checks remain open.

Acceptance checks still open: full Dock-free window lifecycle and recovery; first-use location permission grant/denial and arbitrary map-point input; spoken VoiceOver date editing; native same-process network failure/recovery; native reset error presentation. These are unverified paths, not claims of confirmed defects. Keep Dock mode enabled if you need the most thoroughly exercised launch path. These remain required before 0.9.0 RC; publishing a preview does not close them. App Store validation is planned for 1.0.0. The reader fix passed isolated development-app checks; final 0.8.2 signed-package UI, mixed-input scrolling and spoken reader output remain unverified. Earlier hosted desktop/narrow rendering passed; full website zoom/keyboard checks remain open.

SHA-256 (`YomVezman-0.8.2-12-arm64.dmg`):

```text
6fe95dbf2eb022d33716823582aafea4b904b314e0e286d2422e620a07fc5f96
```
