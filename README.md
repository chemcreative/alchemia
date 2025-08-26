# Alchemia

Interactive TouchDesigner + Replicate AI project for the **Bahamas Quiz** and related experiments.

## Folder Structure
- **Assets/** – Backdrop graphics for the Bahamas quiz and prompt.csv
- **Backup/** – Backup TouchDesigner files  
- **Capture/** – Input and output images from the Bahamas quiz and Replicate AI, named using RFID  
- **MangoRoom/** – TEST files for the heat map  
- **bahamas.toe** – Main quiz UI  
- **replicate.toe** – Replicate AI file  

## Usage

For the Bahamas Quiz, both `replicate.toe` and `bahamas.toe` need to be open at the same time.

### bahamas.toe
In `/project1/p5/text2` line 18 change:

```python
FILE_PATH  = f"C:/Users/BryanSnigur/Desktop/ChemistryCreative/Alchemia/Capture/Input/{RFID_VALUE}.jpg"
to:
FILE_PATH  = f"C:/Users/YOUR PC PATH/Alchemia/Capture/Input/{RFID_VALUE}.jpg"
```
In /project1/p5/moviefileout1 parameter file, update:
```python
"C:/Users/BryanSnigur/Desktop/ChemistryCreative/Alchemia/Capture/Input/" + str(op('/project1/p4/rfid')[0,0]) + ".jpg"
to:
"C:/Users/YOUR PC PATH/Alchemia/Capture/Input/" + str(op('/project1/p4/rfid')[0,0]) + ".jpg"
```
Also on that same container change the Video Device In parameter to your camera.

If it ever gets stuck, go to the main project layer (/project1/) and the constant dictating the pages, manually adjust

### replicate.toe
In /project1/replicate/text2 line 48, change:
```python
output_file = rf"C:\Users\BryanSnigur\Desktop\ChemistryCreative\Alchemia\Capture\Output\{rfid_str}.jpg"
to:
output_file = rf"C:\Users\YOUR PC PATH\Alchemia\Capture\Output\{rfid_str}.jpg"
```

### Notes
Always make sure your paths match your local system’s username and folder structure in the mentioned text DAT's and moviefileout TOP's
