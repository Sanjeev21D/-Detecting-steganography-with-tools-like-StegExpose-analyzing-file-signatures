# Detecting-steganography-with-tools-like-StegExpose-analyzing-file-signatures
## AIM:
To detect hidden data using steganography detection tools like StegExpose and analyze file signatures for authenticity and manipulation.
## Requirements:
- **Operating System:** Linux / Windows
- **Tools:**
    - StegExpose (Java-based tool)
    - Hex Editor (e.g., xxd, HxD)
    - File command (Linux) or TrID (Windows)
- **Sample files:**
    - Suspected stego files (.jpg, .png, .wav)
    - Clean reference files
## ARCHITECTURE DIAGRAM:
```mermaid
flowchart TD
    A[Input File: JPG/PNG/WAV] --> B[File Signature Analysis]
    B --> C{Signature Match?}
    C -- Yes --> D[Pass to StegExpose]
    C -- No --> E[File Tampered / Mismatch]
    D --> F[StegExpose Detection: Suspicious or Clean]
    F --> G[Report Findings]
```

## DESIGN STEPS:
### Step 1:
Install StegExpose or use the JAR version to detect steganography in image files.

### Step 2:
Run StegExpose on a directory of suspected image files using the command:

### Step 3:
Analyze file signatures using tools like file, binwalk, or xxd to check for inconsistencies or embedded content.

## PROGRAM:
**Check file type**
```bash
file suspect.jpg
```
or view magic bytes:
```
xxd suspect.jpg | head
```
**Run StegExpose**
```bash
java -jar StegExpose.jar suspect.jpg
```
## OUTPUT:
List of Images with Steganography Detection Scores and File Signature Details

## Install Steghide
<img width="760" height="396" alt="image" src="https://github.com/user-attachments/assets/d9d607ec-cb87-491c-bbff-40cdf05d4c35" />

## Verify Installation
<img width="280" height="72" alt="image" src="https://github.com/user-attachments/assets/1715704c-614d-4e4a-bf4c-594b7816c466" />

## Embed the Secret Message into the Image
<img width="432" height="171" alt="image" src="https://github.com/user-attachments/assets/a9341a42-8b67-4bae-af63-1207c733fc9a" />

## Delete original file
<img width="272" height="54" alt="image" src="https://github.com/user-attachments/assets/a61cd8db-1a0f-4c14-ae08-16799f8a5286" />

## Extract secret text from image
<img width="316" height="84" alt="image" src="https://github.com/user-attachments/assets/9713b0f5-1f1b-492e-b27a-ea6e766c0ad6" />

## Retrieve Information About the Embedded Data
<img width="305" height="72" alt="image" src="https://github.com/user-attachments/assets/b3cff237-b08f-4325-a00b-8587e46820f2" />

## Analyze File Signature
<img width="479" height="200" alt="image" src="https://github.com/user-attachments/assets/589a92ea-18c7-46d0-845f-b97726a4952e" />

## RESULT:
Hidden data was successfully detected and file signatures were analyzed for irregularities.
