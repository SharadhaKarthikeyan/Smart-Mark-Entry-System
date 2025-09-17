# Data Hiding in Medical Images using Deep Neural Networks  

## Overview  
Medical image security is critical for ensuring patient safety and preventing misdiagnosis caused by tampered or misidentified images.  
This project proposes a **Deep Learning–based steganography system** that hides sensitive patient information inside medical images using a **Denoising Autoencoder (DAE)**.  
The embedded data can later be extracted by authorized personnel, ensuring **confidentiality, authenticity, and integrity** of medical records.  

---

##  Features  
- **Denoising Autoencoder Model** for robust embedding and recovery of hidden data.  
- **Elliptic Curve Cryptography (ECC)** for encrypting patient information before embedding.  
- **BLAKE3 Hashing** to verify data integrity during transmission.  
- High-quality reconstruction of hidden images with **low loss**.  
- Compatible with multiple medical imaging modalities (MRI, Retinal scans).  
- Outperforms traditional techniques (LSB, DCT, GAN) in PSNR and SSIM scores.  

---

## Tech Stack  
- **Languages**: Python  
- **Libraries/Frameworks**: TensorFlow, Keras, NumPy, OpenCV, Matplotlib  
- **Cryptography**: Elliptic Curve Cryptography (ECC)  
- **Hashing**: BLAKE3  
- **Datasets**:  
  - **ADNI** – Alzheimer’s Disease Neuroimaging Initiative (MRI Scans)  
  - **DRIVE** – Retinal Vessel Segmentation Dataset  

---

## Workflow  
1. **Upload Medical Image** (`.jpg` / `.png`)  
2. **Encrypt Patient Data** using ECC → converted into image form.  
3. **Embedding Process**  
   - Cover image + Encrypted info image → fed into **DAE Encoder**  
   - Produces **Container Image** (looks identical to original cover).  
4. **Hashing**  
   - Generate BLAKE3 hash of container image → transmitted alongside.  
5. **Extraction Process (Receiver)**  
   - Verify image integrity using hash.  
   - Use **DAE Decoder** to reconstruct hidden patient information.  
   - Decrypt using ECC to recover original patient data.  

---

## Results  
- **ADNI Dataset (MRI scans)**:  
  - Container Image Loss: **2%**  
  - Reconstructed Secret Image Loss: **2%**  
  - PSNR: **41.89 dB**, SSIM: **0.9979**  

- **DRIVE Dataset (Retinal scans)**:  
  - Container Image Loss: **5%**  
  - Reconstructed Secret Image Loss: **3%**  
  - PSNR: **40.98 dB**, SSIM: **0.9935**  
 The proposed system **outperformed GAN, Single AE, and Stacked AE** in accuracy and reconstruction quality.  

---
