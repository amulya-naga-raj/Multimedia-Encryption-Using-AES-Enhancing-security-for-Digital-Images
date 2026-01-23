# MULTIMEDIA ENCRYPTION USING AES: ENHANCING SECURITY FOR DIGITAL IMAGES

# CIS 628: INTRODUCTION TO CRYPTOGRAPHY SYRACUSE UNIVERSITY - FALL 2025

# TEAM: 

Amulya Naga Raj
Abhijnya Konanduru Gurumurthy
Ananya Naga Raj

---

# PROJECT DESCRIPTION:

Encrypts images using two security layers:
1. LKPD layer(Local Key Position Difference) + Pixel Scrambling
2. Encrypts with AES-256 (cryptographic layer)

Tested on 24335 images 
Trained on 14,034 images with excellent security results.

---

IMPORTANT: CODE TRAINED UNDER 'GOOGLE COLAB'
No requirements needed if running on Google colab

# GUIDE TO RUN THE CODE:

# Step 1: Open Google Colab
- Go to: https://colab.research.google.com/
- Sign in with Google account

# Step 2: Upload Notebook
- In Colab, click File menu
- Click Upload notebook
- Select: NAGARAJ_GURUMURTHY_NAGARAJ_CRYPTOGRAPHY_PROJECT_CODE.ipynb
- Wait for it to open

# Step 3: Get the Dataset
- archive.zip file is submitted along with all the required files. 
- Taken from Kaggle: https://www.kaggle.com/datasets/puneet6060/intel-image-classification
- For easier processing. Do not unzip it.
- OR
- Go to: https://www.kaggle.com/datasets/puneet6060/intel-image-classification
- need a free Kaggle account
- Click Download button
- Save archive.zip file (about 300 MB)
- DO NOT unzip it
- Wait for download to finish

# Step 4: Upload Dataset
- In Colab, Under UPLOAD AND PREPARE DATASET click folder icon on left side
- Click upload button (arrow pointing up)
- Select archive.zip from your computer
- Wait 12-15 minutes for upload
- archive.zip is a large file taken from Kaggle. 
- Requires time to upload the file

# Step 5: Run Everything One cell after Another
- At top of Colab, click Runtime menu
- Click Run all
- If warning appears, click Run anyway
- Now wait 10-12 minutes while code runs
- But need to upload archive.zip under UPLOAD AND PREPARE DATASET
- need to upload archive.zip again if the colab or system turned off and turned on  

# Step 6: Detailed analysis of code
- Scroll each cell 
- Each cell specified for its own function
- One can observe detailed analysis 
- Everything explained in detail 

# Step 7: View Dashboard
- Scroll to bottom of notebook
- Look for: "Running on public URL: https://xxxxx.gradio.live"
- Click that blue link
- Dashboard opens in new tab
- Try analyzing different images!

---

# OBSERVATIONS:

# While Running:

Minute 1-2:
  Installing packages
  Loading libraries

Minute 2-4:
  Extracting dataset
  Loading 14,034 images
  Progress messages appear

Minute 4-6:
  Encrypting images
  Shows "Encrypted 2000 images" etc.

Minute 6-10:
  Running security analysis
  Calculating NPCR, UACI, correlation
  Creating charts

Minute 10-12:
  Setting up dashboard
  Final message: "14034 images ready"

# Final Results:

You should see these numbers:
- NPCR: 99.61 percent (excellent)
- UACI: 32.76 percent (near perfect)
- Correlation reduced: 99+ percent (very strong)
- Entropy: 7.99+ bits (almost maximum)

These numbers prove the encryption works well!

---

# DASHBOARD:

#What the Dashboard Shows:

Section 1:
- Slider to pick image number: 0 to 14033
- Seed slider: leave at 42 unless testing
- Run analysis button
- OR Random button selects random image to test

Section 2:
- Four images side by side
- Original → Scrambled → Encrypted → Recovered

Section 3:
- Five charts showing security metrics
- Text box with detailed results

Section 4: 
- Expandable Sections
At the bottom of dashboard, click on these to expand:
- NPCR differential analysis
- UACI differential analysis  
- Method comparison analysis
- Attack resistance analysis
- Key sensitivity analysis
- Performance benchmarking

# How to Use It:

1. Pick an image number with slider
2. Click "Run complete analysis"
3. Wait 2-3 seconds
4. See results appear
5. Scroll down to view all charts
6. Click expandable sections for details
7. Try "Random" button for different images

---

# TROUBLESHOOTING IF ANY ISSUE:

#Problem: "Dataset not found"
Fix: - Make sure archive.zip is uploaded
     - Check file browser shows archive.zip in the list in left pannel

#Problem: "Out of memory"  
Fix: - Click Runtime → Restart runtime
     - Then run everything again

#Problem: "Cells showing errors"
Fix: - Run cells from top to bottom in order
     - Don't skip any cells
     - Wait for each cell to finish before next one

#Problem: "Dashboard link doesn't work"
Fix: - Re-run the last cell (dashboard cell)
     - New link will be generated
     - Old links expire after 1 Week

#Problem: "Taking too long"
Fix: - This is normal! Processing 14,000 images takes time
     - First run: 10-15 minutes is expected
     - Just let it run and don't close the tab

---

# File Organization

After code runs, Colab creates these folders automatically:
- dataset/ - contains all images extracted from zip
- encrypted_dataset/ - encrypted versions
- encrypted_dataset_scrambled/ - hybrid encrypted versions
- aes_key.bin - encryption key file

Don't need to create these - code makes them automatically.

---

# Dataset Information

Name: Intel Image Classification Dataset
Source: Kaggle
Link: https://www.kaggle.com/datasets/puneet6060/intel-image-classification
Size: 300 MB zipped
Images: 14,034 in training set
Categories: buildings, forest, glacier, mountain, sea, street

Important: Downloaded this yourself from Kaggle.

---

# RESULTS:

# NPCR (Number of Pixel Change Rate):
- Measures how many pixels change when you encrypt
- We got: 99.61 percent
- This means: 99.61% of pixels are different after encryption
- Excellent! Above 99% is considered secure

# UACI (Unified Average Changing Intensity):
- Measures how much pixel values change
- We got: 32.76 percent
- Ideal is: 33.33 percent
- Excellent! Very close to ideal

# Correlation:
- Measures if adjacent pixels are predictable
- Original: ~0.95 (high - pixels are predictable)
- Encrypted: ~0.002 (near zero - completely random)
- Excellent! Patterns are destroyed

# Entropy:
- Measures randomness
- We got: 7.996 bits
- Maximum: 8.000 bits
- Excellent! Almost Perfectly random

# Processing Speed:
- We got: 1-3 milliseconds per image
- Can process: 300-500 images per second
- Very fast! Suitable for real-time use

---

# GOOGLE COLAB:

Advantages:
- Nothing to install on computer
- Works the same for everyone
- Has powerful computers in the cloud
- Free to use
- No configuration needed
- All packages already available

Compared to running on your laptop:
- No need to install Python
- No need to install packages
- No worrying about versions
- No path issues
- Just upload and run

---

# Important Notes

1. Run cells in order - don't skip around
2. Wait for each cell to finish before running next
3. Archive.zip must be uploaded before running
4. Time takes 10-15 minutes - this is normal since dataset is too large
5. Dashboard link works for 72 hours then expires
6. Can re-run anytime to get new dashboard link
7. Don't close Colab tab while cells are running

---


# REQUIREMENTS:

To run this code locally (not on Colab), these packages needed:

numpy==1.24.3
pillow==10.0.0
pycryptodome==3.18.0
matplotlib==3.7.2
pandas==2.0.3
gradio==4.0.0

But for Colab, these are already installed!

---

# SUMMARY:


1. Open colab.research.google.com
2. Upload notebook
3. Download archive.zip from Kaggle or check submission 
4. Upload archive.zip to Colab
5. Click Runtime → Run all
6. Wait for 10 - 15 minutes
7. Click gradio.live link
8. Check random samples
9. Results


# SUPPORT:

If any issues running this:

1. Check this README first
2. Make sure archive.zip is uploaded
3. Make sure cells run in order
4. Try restarting runtime and running again

Contact: Amulya Naga Raj - amnagara@syr.edu

---

# PROJECT DETAILS:

Built:
- Two-layer encryption system
- First layer scrambles pixels
- Second layer does AES encryption
- Tested on 14,034 real images
- Created interactive dashboard
- All security tests passed

RESULTS OF TESTS DONE FOR THE METHOD:
- 99% correlation reduction (destroys patterns)
- 39% better than regular AES alone
- Very fast (300+ images per second)
- Lossless (perfect reconstruction)
- Defense in depth (two layers)

