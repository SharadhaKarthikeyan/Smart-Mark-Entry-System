# Smart Mark Entry System  

## Overview  
The **Smart Mark Entry System (SMS)** is designed to automate the tedious manual mark entry process by recognizing handwritten digits from scanned answer sheets using **Convolutional Neural Networks (CNNs)**. The system ensures faster, more accurate mark entry, reduces human errors, and directly updates results into a database.  

---

## Features  
- Handwritten digit recognition using CNN trained on **MNIST dataset**.  
- Automated **mark entry into database** with student roll number mapping.  
- Supports image input through **webcam or phone camera**.  
- Preprocessing, segmentation, cropping, and feature extraction of scanned images.  
- GUI built with **Tkinter** for easy faculty and student interaction.  
- Email notifications for mark updates (faculty → student, student → faculty).  
- Separate login portals for **faculty** and **students** with role-based access.  

---

## Tech Stack  
- **Languages**: Python  
- **Libraries**: TensorFlow, Keras, NumPy, OpenCV, Tkinter, Matplotlib, Pillow, Scikit-learn  
- **Database**: SQLite  
- **Frontend**: Tkinter GUI  

---

## Modules  
1. **User Module** – Faculty & Student login/registration.  
2. **Preprocessing Module** – Cropping, resizing, background suppression.  
3. **Segmentation Module** – Identifying and extracting individual characters.  
4. **CNN Module** – Handwritten digit recognition and training on MNIST.  
5. **Database Module** – Inserting/updating student marks in SQLite.  
6. **Notification Module** – Automated email alerts for marks.  
7. **GUI Module** – Interactive interface for faculty and students.  

---

##  Workflow  
1. **Faculty/Student Login**  
2. **Upload or Scan Answer Script (Webcam/Phone)**  
3. **Image Preprocessing & Segmentation**  
4. **CNN-based Recognition of Handwritten Digits**  
5. **Automatic Database Update**  
6. **Mark Display for Faculty & Students**  
7. **Email Notification Sent**  

---
## Results
- Achieved **~90%** accuracy in handwritten digit recognition.

