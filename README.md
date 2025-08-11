# WatermarkApp

An Android app to select or capture images, add custom text watermarks, and save the watermarked images to a specific folder in the device gallery.

---

## Features

- **Select Image from Gallery**  
Pick any image from your device gallery.

- **Capture Photo via Camera**  
Take a new photo using your device camera.

- **Add Custom Text Watermark**  
Input your desired watermark text and apply it on the image dynamically.

- **Save to Gallery with Custom Folder**  
Save the watermarked image to a specific folder inside your device’s Pictures directory.

---

## How It Works

1. Pick an image from the gallery or capture a new photo.  
2. Enter the watermark text in the input field.  
3. Tap "Apply Watermark" to overlay the text on the image.  
4. Choose a folder name or use the default.  
5. Save the watermarked image to the gallery.

---

## Permissions

- Camera (for capturing photos)  
- Read External Storage (to pick images)  
- Write External Storage (only on Android 9 and below for saving images)

The app requests these permissions at runtime.

---

## Technical Details

- Uses Android’s modern Activity Result APIs for handling gallery and camera actions.  
- Supports Android 5.0 (API 21) and above.  
- Uses `FileProvider` to securely share image files with the camera app.  
- Handles scoped storage changes on Android 10+ using MediaStore.  
- Watermark is drawn on a copy of the original image to avoid overlapping on multiple edits.

---

