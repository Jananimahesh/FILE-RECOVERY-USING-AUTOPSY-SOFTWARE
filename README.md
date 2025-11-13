# FILE-RECOVERY-USING-AUTOPSY-SOFTWARE

## AIM
To use **Autopsy Digital Forensics Tool** to retrieve deleted files from a disk image.

---

## REQUIREMENTS
- **Operating System**: Windows 10/11, macOS, or Linux
- **Tool**: [Autopsy Digital Forensics](https://www.autopsy.com/)  
- **Test Data**: Disk image file (`disk.dd`, `disk.img`, `.E01`)

---

## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Install Autopsy]
    B --> C[Create New Case in Autopsy]
    C --> D[Add Data Source: Disk Image]
    D --> E["Run File System & Data Recovery Modules"]
    E --> F[Locate Deleted Files in Results]
    F --> G[Recover and Export Deleted Files]
```
## DESIGN STEPS:
### Step 1:
Open Autopsy and create a new case with appropriate case details.

### Step 2:
Add a disk image as a data source and let Autopsy analyze the content.

### Step 3:
Navigate to the "Deleted Files" section in Autopsy and examine or recover the deleted files.

## PROGRAM:
### Install Autopsy
```bash
# Download Autopsy from:
# https://www.autopsy.com/
# Install following the setup wizard.

```
<img width="458" height="243" alt="image" src="https://github.com/user-attachments/assets/5fefdab7-99fd-40d7-96da-507139c63a1d" />

### Create a New Case
```
# File → New Case
# Enter Case Name: Deleted_File_Recovery
# Choose Base Directory: C:\Cases\Deleted_File_Recovery
# Click Finish
```
<img width="478" height="296" alt="image" src="https://github.com/user-attachments/assets/5567c550-9fdf-4511-9f8d-4f7ab8119818" />

### Add Disk Image
```
# Add Data Source → Disk Image or VM File
# Browse to: C:\forensics\disk.dd
# Click Next
```
<img width="335" height="299" alt="image" src="https://github.com/user-attachments/assets/46c99788-4662-4c86-ae94-63aabb636430" />

### Run Ingest Modules
```# Select:
# - File System Analysis
# - Keyword Search (optional)
# - Data Recovery / Carving
# Click Finish
```
<img width="291" height="185" alt="image" src="https://github.com/user-attachments/assets/9627eed0-ba66-43ed-aaf2-29fea75d7ece" />

### Locate Deleted Files
```
# Navigate to 'Deleted Files' section in the tree view
# Review metadata (size, hash, timestamps)
```



### Export Deleted Files
```
# Right-click → Extract File(s)
# Save to: C:\forensics\Recovered_Files\
```

## OUTPUT:
Recovered Deleted File List and Details

Folder before deleting the files

<img width="689" height="452" alt="image" src="https://github.com/user-attachments/assets/5e481ecc-d423-4b07-b674-d8a2af80b48c" />

Folder after deleting the files

<img width="697" height="469" alt="image" src="https://github.com/user-attachments/assets/e77a7a16-91dc-43fc-9b82-49e010cfb565" />

Folder after extracting the deleted images using autopsy

<img width="689" height="452" alt="image" src="https://github.com/user-attachments/assets/5e481ecc-d423-4b07-b674-d8a2af80b48c" />





## RESULT:
Deleted files were successfully retrieved and analyzed using Autopsy.
