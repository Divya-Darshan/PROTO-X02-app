# Proto-x02 Blender Add-on

**Author:** Divya Darshan  
**Inspired by:** Poly Ford YouTube Channel  
**Version:** 2.8  
**Category:** Video Editing / Photogrammetry  



# 🚀 How to Download `proto-x02` Add-on

**Follow these steps to get the add-on quickly and easily:**

**1️⃣ Click the `Code` button** (usually green, top right of the file list).  
**2️⃣ Select `Download ZIP`** from the dropdown.  
**3️⃣ Save the ZIP file** to a location you can easily access.  
**4️⃣ Open Blender → Edit → Preferences → Add-ons → Install**.  
**5️⃣ Select the downloaded `proto-x02.zip` file and click `Install Add-on`**.  
**6️⃣ Enable the add-on** by checking the box next to its name in the Add-ons list.  

✅ **The add-on is now ready to use in the Video Sequencer sidebar** (press `N` to open).



---

## Overview

**Proto-x02** is a Blender add-on designed to streamline video-based photogrammetry workflows. It automates repetitive tasks like project setup, folder organization, file placeholders, template copying, tracking, and rendering. Additionally, it allows packaging the project into a zip file using a custom bot command (`I`) with 7-Zip.

The add-on integrates directly into the **Video Sequencer** interface (`Sidebar → N`) and provides intuitive operators for a smooth workflow.

This project was inspired by the **Poly Ford YouTube channel**, which showcases advanced video-to-3D pipelines and photogrammetry techniques. This add-on aims to automate many steps shown in those videos.

---

## Features

### 1. Video Import
- Supports `.mp4`, `.mov`, `.avi`, `.mkv` formats.
- Copies selected video into the `02 VIDEOS` folder.
- Automatically adds the video to the **Sequencer** for tracking and editing.
- Stores the last imported video path to manage cleanup and workflow continuity.

### 2. Project Folder Automation
- Automatically creates the following folder structure:
01 GLOMAP
02 VIDEOS
03 FFMPEG
04 SCENES
05 SCRIPT

- Generates **placeholder files** for common extensions like `.mp4`, `.mov`, `.dll`, `.exe`, `.zip`, etc., preventing empty folder errors.
- Copies **template files** (like example `.glomap` files, `track.bat`, `ffmpeg.exe`) into their respective folders.
- Recursively copies **dependencies** including DLLs, plugins, and executables, while ensuring only `track.bat` is added in `05 SCRIPT`.

### 3. Auto-Tracking & Rendering
- Runs the `track.bat` script from `05 SCRIPT` in a **visible terminal window** on Windows.
- Automatically outputs results to `04 SCENES`.
- Provides UI buttons to **start** and **cancel** tracking.
- Uses Blender properties to prevent multiple tracker instances and provides real-time feedback.
- Avoids opening Blender console or confusing terminal windows for the user.

### 4. Cleanup
- Deletes the last imported video if the corresponding Sequencer strip is removed.
- Ensures your project folder remains organized without leftover files.

### 5. Custom Bot Command (`I`)
- Pressing the `I` key triggers a zip archive of the project using **7-Zip**.
- Deletes any existing zip to avoid conflicts.
- Creates a zip in the **same project directory**, ready for sharing or backup.

---

## How It Works (Functionality Explained)

1. **Open Video**  
 - The user selects a video file via the "Open Video" button.
 - The add-on creates necessary folders, placeholder files, and copies template and dependency files automatically.
 - The video is copied into `02 VIDEOS` and added to the Blender Sequencer.

2. **Run Tracker**  
 - Pressing "Track & Render" executes the `track.bat` file inside a terminal.
 - `track.bat` handles GloMAP/FFMPEG processing, generating scene outputs in `04 SCENES`.
 - Blender UI indicates that tracking is in progress.
 - Tracking can be **cancelled** safely via the "Cancel Tracking" button.

3. **Automated Folder & File Management**  
 - Ensures the project is self-contained.
 - Handles placeholder files and dependencies to reduce errors during tracking and rendering.

4. **Project Packaging**  
 - The custom `I` command packages the project into a zip archive using 7-Zip.
 - Ideal for sharing the project, archiving, or submission purposes.

---

## Usage

1. Install the add-on in Blender (`Edit → Preferences → Add-ons → Install`).
2. Open the **Video Sequencer**.
3. Use the **Sidebar (N)** panel labeled "Photogrammetry" to:
 - Open a video
 - Run tracking
 - Cancel tracking if needed
4. Press **I** to generate a zip archive of your project.

---

## Folder Structure

Project_Root/
│   
├── 01 GLOMAP/ # GloMAP files and placeholders  
├── 02 VIDEOS/ # Imported video files   
├── 03 FFMPEG/ # FFmpeg binaries and placeholders   
├── 04 SCENES/ # Output scenes from tracking    
├── 05 SCRIPT/ # track.bat for automation  
└──  Your `.blend` blender  file


---

## Acknowledgments

- Inspired by **Poly Ford YouTube channel** for photogrammetry workflow ideas.
- Blender Python API for seamless add-on integration.
- 7-Zip for project packaging.

---

## Notes

- Tested on **Windows** only (uses `cmd /K` to show terminal).
- Blender must have a saved `.blend` file for the project root to be detected.
- Ensure **7-Zip** is installed and accessible via the system PATH for the `I` command to work.

---

## Community & Contributions

I love to see contributions from the community! If you find any bugs, have ideas for new features, or want to improve the workflow, feel free to open an issue or submit a pull request. This project is meant to help everyone streamline photogrammetry workflows in Blender, and **your input can make it even better**.  

Some ways you can contribute:

- Improve the Blender UI and log feedback system
- Add support for more video formats or OS platforms
- Enhance the `track.bat` automation with additional scripts or options
- Share example projects, templates, or presets

Let's build a helpful, collaborative Blender add-on community together! 🫂
--

