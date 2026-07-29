Bug01: Client Crash (P0 - High Severity)
1. Description

Summary: The desktop application window crashes and reloads instantly when attempting to preview an animated sticker in a server thread.

2. Steps to Reproduce

Launch Discord Desktop Client on Windows 11.

Enter any server text channel and click to open an active side-panel Thread.

Click on the Sticker/Expression Picker icon inside the chat text box.

Hover the mouse cursor over any custom animated .APNG or Lottie sticker to trigger the autoplay preview.

3. Expected Results

The sticker preview should play smoothly inside the picker menu overlay without affecting the main client window thread stability.

4. Actual Results

The entire Electron application window freezes immediately for 2 seconds, throws an unhandled rendering frame exception, and undergoes a full hard reload (black screens and displays the spinning Discord loading logo).

5. Client & Device Information

App Version: Stable 264120 (04ad2f1)

Operating System: Windows 11 Pro 23H2 (Build 22631.3155)

Hardware Profile: Intel Core i7-13700K, 32GB RAM, NVIDIA RTX 4070

Logs Attached: DxDiag.txt, discord_render_crash.log

Bug02: Functional / UI Bug (P2 - Medium Severity)
1. Description

Summary: Role color hierarchy fails to apply to a user's nickname inside the voice channel active participant list on mobile.

2. Steps to Reproduce

Open the Discord Mobile app on iOS.

Navigate to a server where your user account is assigned a custom role with a specific color (e.g., Green for "Moderator").

Tap on a Voice Channel to join the voice call room.

Look at your name inside the list of connected voice participants.

3. Expected Results

The username text should inherit and display the designated color flag of your highest hierarchical server role (Green).

4. Actual Results

The username defaults to standard system text color (White/Dark Gray depending on light/dark mode themes), ignoring the custom role color entirely. Note: The name appears correctly in the text chat list, meaning the bug is isolated to the Voice UI component layer.

5. Client & Device Information

App Version: TestFlight Mobile Build 218.0

Operating System: iOS 19.4.1

Hardware Profile: iPhone 15 Pro Max

Logs Attached: ios_client_ui_debug.jsonq
