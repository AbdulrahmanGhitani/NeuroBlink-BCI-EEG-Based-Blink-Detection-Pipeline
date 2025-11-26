# **NeuroBlink: BCI EEG-Based Blink Detection Pipeline**

<p>NeuroBlink is a Brain–Computer Interface (BCI) pipeline that detects eye-blink events from EEG signals using machine-learning classification. The system processes multi-channel EEG data, trains a Random Forest classifier to distinguish eye-open vs. eye-closed states, and exports the predictions for integration with an Arduino-based blinking-eye demo.</p>

[![Eye Blinking Demo](thumbnail.png)](Prototype.mp4)

 ---

## 📌 **Features**

- **EEG Signal Preprocessing**
  - Loads EEG data from ARFF format  
  - Converts byte-encoded eye-state labels to integers  
  - Filters and prepares EEG channels for analysis  

- **Machine Learning Classification**
  - Trains a Random Forest classifier using scikit-learn  
  - Performs train/test splitting and accuracy evaluation  
  - Generates sequential eye-state predictions  

- **Visualization Tools**
  - Multi-channel EEG signal plotting for inspection  
  - Cleaned-signal visualization after filtering  

- **Arduino Integration Output**
  - Converts predicted classes into True/False blink indicators  
  - Exports predictions to `output.txt` for hardware use  

---

## 🧠 **Project Pipeline Overview**

1. **Load EEG Dataset**  
   - Uses the well-known *EEG Eye State Dataset* (14 EEG channels + eye-state label)

2. **Preprocess Data**  
   - Decode label bytes  
   - Remove non-numeric fields  
   - Prepare features (X) and labels (y)

3. **Train Random Forest Model**  
   - Train/test split  
   - Model training & evaluation  
   - Generate full-sequence blink predictions  

4. **Export Predictions**  
   - Convert predictions into “True/False” format  
   - Save results to `output.txt` for Arduino integration  

---

## 🛠 Technologies Used

- Python
- Pandas / NumPy
- scikit-learn
- Matplotlib
- SciPy (ARFF loading)
- Arduino (hardware demo)

---

## Contributors <a name = "contributors"></a>

<table>
  <tr>
    <td align="center">
    <a href="https://github.com/AbdulrahmanGhitani" target="_black">
    <img src="https://avatars.githubusercontent.com/u/114954706?v=4" width="150px;" alt="Abdulrahman Shawky"/>
    <br />
    <sub><b>Abdulrahman Shawky</b></sub></a>
    </td>
<td align="center">
    <a href="https://github.com/omarnasser0" target="_black">
    <img src="https://avatars.githubusercontent.com/u/100535160?v=4" width="150px;" alt="omarnasser0"/>
    <br />
    <sub><b>Omar Abdulnasser</b></sub></a>
    </td>
         <td align="center">
    <a href="https://github.com/AhmedKamalMohammedElSayed" target="_black">
    <img src="https://avatars.githubusercontent.com/u/96977876?v=4" width="150px;" alt="Ahmed Kamal"/>
    <br />
    <sub><b>Ahmed Kamal</b></sub></a>
    </td>
         <td align="center">
    <a href="https://github.com/AbdullahOmran" target="_black">
    <img src="https://avatars.githubusercontent.com/u/30219936?v=4" width="150px;" alt="Abdullah Omran"/>
    <br />
    <sub><b>Abdullah Omran</b></sub></a>
    </td>
      </tr>
 </table>

