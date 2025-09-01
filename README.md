# 🎬 Proto-x02 Blender Add-on  

**Author:** Divya Darshan  
**Inspired by:** Poly Ford YouTube Channel  
**Version:** 2.8  
**Category:** Video Editing / Photogrammetry  

---

## 🚀 How to Download & Install  

1. Go to [https://gitlab.com/divya-darshan/proto-x02](https://gitlab.com/divya-darshan/proto-x02).
2. Click the **`Code`** button (Blue top right on GitLab1).  
3. Select **Download**.  
4. Save the ZIP file (e.g., `proto-x02.zip`).  
5. Open **Blender** → `Edit` → `Preferences` → `Add-ons` → `Install`.  
5. Select the downloaded file.  
7. Enable the add-on from the **Add-ons list**.  

✅ The add-on is now available in the **Video Sequencer Sidebar** (`N` key).  

---

## ✨ Overview  

**Proto-x02** is a Blender add-on built to **streamline video-based photogrammetry workflows**.  
It automates repetitive tasks like:  

- Project setup & folder creation  
- Placeholder & template file generation  
- Video import & Sequencer integration  
- Auto-tracking & rendering  
- Project packaging with **7-Zip**  

This project is inspired by the **Poly Ford YouTube channel**, known for advanced photogrammetry tutorials.  

---

## 🔑 Features  

### 🎥 Video Import  
- Supports `.mp4`, `.mov`, `.avi`, `.mkv`  
- Copies video into the `02 VIDEOS` folder  
- Automatically adds video to the **Sequencer**  
- Tracks last imported video for cleanup  

### 📂 Project Folder Automation  
- Creates structured folders:
01 GLOMAP/
02 VIDEOS/
03 FFMPEG/
04 SCENES/
05 SCRIPT/

- Adds placeholder files (`.mp4`, `.mov`, `.dll`, `.exe`, `.zip`, etc.)  
- Copies templates (e.g., `track.bat`, `ffmpeg.exe`, example `.glomap`)  
- Handles dependencies (DLLs, plugins, executables)  

### 🛠 Auto-Tracking & Rendering  
- Runs `track.bat` inside `05 SCRIPT` in a visible terminal  
- Outputs results to `04 SCENES`  
- Start/Cancel buttons in the UI  
- Prevents duplicate tracker instances  

### 🧹 Cleanup  
- Deletes last imported video if Sequencer strip is removed  
- Keeps project folder clean and organized  

### 📦 Project Packaging (Key `I`)  
- Press **`I`** to archive project with **7-Zip**  
- Automatically removes old zips  
- Saves archive in project root  

---

## ⚡ Usage  

1. Install add-on in Blender.  
2. Open the **Video Sequencer**.  
3. Use **Sidebar → Photogrammetry** panel to:  
 - Import a video  
 - Run tracking  
 - Cancel tracking  
4. Press **`I`** to zip the entire project.  

---

## 🙏 Acknowledgments  

- Inspired by **Poly Ford YouTube channel**  
- Built with the **Blender Python API**  
- Uses **7-Zip** for packaging  

---

## 📝 Notes  

- Tested on **Windows only** (uses `cmd /K`)  
- Blender file must be **saved** for project root detection  
- Requires **7-Zip installed & added to PATH**  

---

## 🤝 Contributions  

Contributions are welcome! You can:  

- Improve the UI & logging  
- Add more video/OS support  
- Enhance `track.bat` automation  
- Share templates & presets  

Let’s build a collaborative Blender add-on community together! 🫂  


