# Dynamic Island Visualizer
A sleek, minimalist audio-reactive visualizer for Spicetify, inspired by the iPhone's Dynamic Island call interface.

🌟 Features
iPhone Style Aesthetics: Minimalist pill-shaped bars that expand vertically from the center rather than the bottom.

Pro Physics Engine: Implements Asymmetric Physics with a snappy "Fast Attack" (upward movement) and a floaty "Gravity Decay" (downward movement).

Beat-Sync Technology: Directly taps into Spotify's AudioAnalysis API to pulse in perfect synchronization with the track's beats and tatums.

Dribbblish-Style Color Extraction: Uses a custom canvas-based extractor to "read" the album art pixels manually. This ensures color reactivity even when Spotify's internal APIs are broken or restricted.

Zero-Dependency Design: Optimized to work on vanilla Spotify without requiring specific themes or external CSS frameworks.

🚀 Installation
1. Download the script
Download dynamicViz.js and place it in your Spicetify Extensions folder:

Windows: %AppData%\Spicetify\Extensions\

macOS/Linux: ~/.spicetify/Extensions/

2. Enable the extension
Open your terminal or PowerShell and run:

PowerShell

spicetify config extensions dynamicViz.js
spicetify apply
🛠 Customization
The script is heavily commented to allow for easy personal tweaks. You can edit the following values directly in the dynamicViz.js file:

Physics Snappiness: Change the 0.6 (Attack) and 0.08 (Decay) multipliers in the Physics Loop section.

Visual Size: Adjust the height (default 20px) and width (default 3px) in the CSS injection block.

Color Sensitivity: Modify the getDribbblishColor function to change how aggressively the visualizer brightens dark album art.

❓ Troubleshooting
The bars are green and don't change color: This usually means the script cannot find the album art image. Ensure you aren't using another extension that completely removes the cover art from the bottom-left corner.

The visualizer isn't moving: Ensure you are playing a song from Spotify's library. Local files (MP3s uploaded from your computer) do not have AudioAnalysis data on Spotify's servers and will only show a subtle "breathing" animation.

The visualizer disappeared after a Spotify update: Spotify occasionally changes the class names of UI elements. If the visualizer is gone, check the BAR_SELECTOR variable in the script and update it to the current class name of the playback bar.

📜 Credits
Inspired by the Apple Dynamic Island.

Color extraction logic adapted from the Dribbblish Dynamic Theme.

Built with ❤️ for the Spicetify Community.
