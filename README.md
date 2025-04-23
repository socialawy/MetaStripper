# MetaStripper
Ever shared a document, image, or video without realizing embedded metadata could expose sensitive details? MetaStripper helps remove hidden data before sharing.
MetaStripper is a tool to remove metadata from various file types, ensuring privacy and security by cleaning sensitive information. It provides a graphical user interface (GUI) and supports multiple file formats. This project includes a Python script and portable executables for Windows, (and you can do that for macOS, and Linux).

## Contents
- `metastripper.py`: Python source script (requires Python 3.11 and dependencies).
- `MetaStripper.exe`: (optional, you can compile it yourself)Portable executable for Windows.
- `MetaStripper` (macOS): Portable executable for macOS (optional, build required).
- `MetaStripper` (Linux): Portable executable for Linux (optional, build required).
- `LICENSE`: MIT License.
- `ffmpeg.exe` (optional): For video metadata removal on Windows.
- `ffmpeg.md` (optional) To download the last compatible version for your OS, through the offical link. 
- `requirements.txt` (For compiling).
- `MetaStripper_UI_Screenshot.png`
## Download MetaStripper
The latest version of MetaStripper is available for download via GitHub Releases:  
👉 [Download MetaStripper.exe](https://github.com/socialawy/MetaStripper/releases/latest)

## Supported File Formats
- **Images**: JPG, JPEG, PNG, TIFF, BMP, WEBP, GIF, SVG, HEIC, CR2, NEF
- **Documents**: DOCX, XLSX, PDF, TXT, CSV, ODT, RTF
- **Presentations**: PPTX, ODP
- **Media**: MP3, WAV, FLAC, MP4, AVI, MKV, MOV
- **Archives**: ZIP, RAR, 7Z (copied without metadata removal)
- **Others**: HTML, generic files (via hachoir)

## Features
- Remove all metadata or keep specific info (copyright, creation date).
- Process files individually or recursively in folders.
- Set maximum file size limit (in MB).
- Create backups before cleaning.
- Detailed logging (`metastripper.log` in the temp directory).

## Usage

### Running on Windows
1. Copy `MetaStripper.exe` to any directory.
2. (Optional) Place `ffmpeg.exe` in the same directory for video metadata removal (MP4, AVI, MKV, MOV).
3. Double-click `MetaStripper.exe` to run.
4. Select files or a folder, choose options (e.g., recursive, backup), and click "Clean Files".
5. Output files are saved with `_cleaned` suffix.
6. Check `%TEMP%\metastripper.log` for details.

### Running on macOS
1. Copy `MetaStripper` to any directory.
2. (Optional) Place `ffmpeg` binary in the same directory for video metadata removal.
3. Run via terminal (`./MetaStripper`) or double-click (may require `chmod +x MetaStripper`).
4. Allow the app in System Preferences > Security & Privacy if prompted.
5. Follow the same steps as Windows.
6. Check `/tmp/metastripper.log` for details.

### Running on Linux
1. Copy `MetaStripper` to any directory.
2. (Optional) Place `ffmpeg` binary in the same directory for video metadata removal.
3. Run via terminal (`./MetaStripper`) or double-click (may require `chmod +x MetaStripper`).
4. Ensure Tkinter is installed (`sudo apt install python3-tk` on Ubuntu).
5. Follow the same steps as Windows.
6. Check `/tmp/metastripper.log` for details.

### Running the Python Script
1. Install Python 3.11 and dependencies:
   ```bash
   pip install pillow pyPDF2 python-pptx python-docx imageio pillow-heif openpyxl odfpy mutagen rarfile py7zr hachoir ffmpeg-python
- Or
   ```bash
   pip install -r requirements.txt
   
#### Note: You might want to use a virtual environment to avoid conflicts:
'bash'
python -m venv env
source env/bin/activate  # macOS/Linux
env\Scripts\activate  # Windows
pip install -r requirements.txt

## Limitations
- Encrypted PDFs are copied without cleaning.

- Archives (ZIP, RAR, 7Z) are copied without metadata removal.

- Corrupted Excel files (XLSX) are copied with a warning.

- Video metadata removal requires ffmpeg or ffmpeg.exe.

## Troubleshooting
1- Check metastripper.log in the temp directory (%TEMP% on Windows, /tmp on macOS/Linux).

2- Ensure file permissions allow reading/writing.

3- For Python script, verify all dependencies are installed.

4- On Windows, install Microsoft Visual C++ Redistributable if DLL errors occur.

## License
This project is distributed under the MIT License. Users are free to modify, distribute, and use MetaStripper for personal or commercial purposes under the MIT License. See LICENSE for details.

## Contact
For questions or support, contact socialawy at Twitter" @ahmed_f
