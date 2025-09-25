# AMD-FSR-4-INT8

Install AMD FSR 4.0.2 on RX 6000 and RX 7000 GPUs without RDNA 3 support. Step-by-step guide with required drivers, DLL replacement process, and extra tweaks for privacy and performance.

# Guide: Install AMD FSR 4.0.2 on GPUs Without RDNA 3

### ⚠️ Guide only for RX 6000 series GPUs  
(Under the video tutorial you’ll also find instructions for RX 7000 series)

---

## Steps

1. **Download the required drivers and folder** (replace `25.9.2` with the latest driver version):

- Folder: [Google Drive Link](https://drive.google.com/file/d/1Hp4v8wmaK3-yKU1is4p0foeeZiWHtjtq/view?usp=sharing)  
- Adrenalin 23.9.1: [Download](https://www.amd.com/en/resources/support-articles/release-notes/RN-RAD-WIN-23-9-1.html)  
- Adrenalin 25.9.2: [Download](https://www.amd.com/en/resources/support-articles/release-notes/RN-RAD-WIN-25-9-2.html)  

---

2. **Extract both drivers with 7-Zip**  
Right-click → `7-Zip` → `Extract to "****"`

---

3. **Copy the required DLLs from 23.9.1**  

Go to:  
```
\whql-amd-software-adrenalin-edition-23.9.1-win10-win11-sep6\Packages\Drivers\Display\WT6A_INF\B395348
```

Search for **`amdx`** inside the `B395348` folder. Copy these files:

- `amdxc64.dll` (68.6MB) – 2023/09/05 13:01  
- `amdxc32.dll` (61.7MB) – 2023/09/05 13:01  

---

4. **Replace DLLs in the latest driver**  

Go to the latest driver folder, for example:  
```
\amd-software-adrenalin-edition-25.9.2-win10-win11-sep-rdna\Packages\Drivers\Display\WT6A_INF\B419241
```

> ⚠️ The folder name (e.g. `B419241`) may change depending on the driver version.

Paste the previously copied DLLs and **replace both files**.  

Go back to:  
```
\amd-software-adrenalin-edition-25.9.2-win10-win11-sep-rdna
```

Run `Setup.exe` → Click **Install Driver Software**.

---

## ⚠️ Important

**Disable automatic driver updates.**  
Every time you reinstall drivers you must repeat this process until AMD releases pre-compiled drivers with FSR enabled.

---

## Credits & Tutorials for RX 7000

- Video tutorial: [YouTube](https://www.youtube.com/watch?v=U4B3vmWg9bg&t=)  

### How to apply in games

- **Upscaling only** → [Watch here](https://youtu.be/U4B3vmWg9bg?t=210)  
- **Upscaling + Frame Generation** → [Watch here](https://youtu.be/U4B3vmWg9bg?t=265)  

---

## Recommended Privacy & Settings Tweaks

For pre-configured driver privacy & settings, download and run the following `.bat` file:  
👉 [amd-dwords.bat](https://github.com/imribiy/amd-gpu-tweaks/blob/main/amd-dwords.bat)  
