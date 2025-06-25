# Voxscribe - Real-time Voice Transcription & Translation

A simple app that records your voice, transcribes it, and translates it to French in real-time.

## What You Need (Windows)

- **Python 3.8+** - Download from [python.org](https://www.python.org/downloads/)
- **Node.js** - Download from [nodejs.org](https://nodejs.org/)
- **A microphone** and modern web browser

## Quick Setup (Windows)

### Step 1: Start the Backend Server

1. Open **PowerShell** (search for it in Start menu)
2. Navigate to your project folder:
 
   ```

3. Run this single command to start the backend:
   ```powershell
   cd multilingo-server; python -m venv venv; .\venv\Scripts\Activate.ps1; pip install -r requirements.txt; uvicorn main:app --reload
   ```

4. Wait for it to show:
   ```
   INFO: Uvicorn running on http://127.0.0.1:8000
   Whisper model loaded.
   ```

### Step 2: Start the Frontend

   ```
 Run this command:
   ```powershell
   cd voxscribe-app; npm install; npm run dev
   ```

4. Wait for it to show:
   ```
   Local: http://localhost:5173/
   ```

### Step 3: Use the App

1. Open your browser and go to: `http://localhost:5173`
2. Allow microphone access when asked
3. Click "Start Session"
4. Click "Start Recording" → speak → click "Stop Recording"
5. See your speech transcribed and translated to French!

## Simple Windows Batch Files (Optional)

To make it even easier, you can create these batch files:

### Create `start-backend.bat`:
```batch
@echo off
cd multilingo-server
if not exist venv (
    python -m venv venv
)
call venv\Scripts\activate.bat
pip install -r requirements.txt
uvicorn main:app --reload
pause
```

### Create `start-frontend.bat`:
```batch
@echo off
cd voxscribe-app
npm install
npm run dev
pause
```

Then just double-click these files to start each part!

## Troubleshooting

**If Python command doesn't work:**
- Make sure you checked "Add Python to PATH" during installation
- Restart PowerShell after installing Python

**If npm command doesn't work:**
- Restart PowerShell after installing Node.js
- Make sure Node.js installation completed successfully

**If microphone doesn't work:**
- Check Windows microphone permissions in Settings
- Make sure your browser has microphone access

**If you get permission errors:**
- Run PowerShell as Administrator
- Or try: `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser`

## Change Translation Language

To translate to a different language instead of French:

1. Open `multilingo-server\main.py` in any text editor
2. Find this line: `"fr"` (appears twice)
3. Replace with:
   - `"es"` for Spanish
   - `"de"` for German  
   - `"it"` for Italian
   - `"pt"` for Portuguese
4. Save the file

## That's It!

The app should now be running. Both PowerShell windows need to stay open while using the app. 

fastapi
uvicorn
websockets
starlette
pydub
numpy
soundfile
openai-whisper
langdetect
deep-translator
sqlalchemy
tortoise-orm
passlib
fastapi-users 
