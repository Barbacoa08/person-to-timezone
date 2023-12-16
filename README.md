# Person to Place

Are you sick to death of trying to remember who lives where and what time it is there? Me too.

## features and functionality examples

The app is entirely local. On initial load, you will see the following message: "No preferences found, using default preferences," which means everything is turned on.
![initial loading screen of application](./readme-images/initial-loading-screen.jpg)

The app has full CRUD functionality.
![GIF of an entry being shown, removed, and then added again](./readme-images/CRUD-functionality.gif)

The app allows searching for a person, place, or timezone independent of if those options are shown.
![GIF of an entry being searched for by timezone and then place](./readme-images/search-place-or-timezone.gif)

Finally, the app has a range of preferences, such as what columns to show, date and time format, and more.
![GIF of different options being enable and disabled by the preferences modal](./readme-images/app-preferences.gif)

## dev notes

- all icons created from my Calvin face image via: `pnpm tauri icon ./src-tauri/icons/app-icon.png`
  - [docs here](https://tauri.app/v1/guides/features/icons/#command-usage)
- run app dev: `pnpm tauri dev`
- run web dev: `pnpm dev`
- generate a new set of app icons: `pnpm tauri icon ./src-tauri/icons/app-icon.png`
  - works with (almost) any type of image format
- generate the app
  - note that this is taken care of via [Tauri's GitHub Actions](https://github.com/tauri-apps/tauri-action).
  - [generate mac app](https://tauri.app/v1/guides/building/macos/)
    - apple silicon: `pnpm tauri build --target aarch64-apple-darwin`
    - intel: `pnpm tauri build --target x86_64-apple-darwin`
    - universal: `tauri build --target universal-apple-darwin`
  - [generate pc app](https://tauri.app/v1/guides/building/windows): `pnpm tauri build --target x86_64-pc-windows-msvc`

## other notes

_After_ starting work on this project, I found [Clocker](https://github.com/n0shake/clocker) for Mac. Clocker solves a similar problem, and is free, but is Mac only and doesn't have a "notes" feature or as much customization. If what you need is a simple name-to-time on a Mac, Clocker may be a better product for you. If you need slightly more extensive notes, a larger display, and want more customization options, Person to Place may be a better product for you.

The app images were generated by "[Stable Doodle](https://clipdrop.co/stable-doodle)"

Data for the app is stored at:

- Mac: `/Users/[username]/Library/Application Support/com.tauri.dev/.settings.dat`
- PC: unknown
