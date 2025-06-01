# 🗣️ Speech Recognition using LSTM and MFCC

This project implements a simple speech recognition model using audio `.wav` files and their corresponding `.txt` transcripts. It extracts **MFCC features** from audio and trains a **Bidirectional LSTM** neural network to predict character-level transcripts.

---

## 📁 Dataset Structure

Place your dataset inside a `dataset/` folder. Each `.wav` file should have a corresponding `.txt` file with the **same name**, like:

```
dataset/
├── file1.wav
├── file1.txt
├── file2.wav
├── file2.txt
...
```

---

## 📦 Dependencies

Install the required libraries:

```bash
pip install numpy librosa scikit-learn tensorflow
```

---

## 🚀 How It Works

1. **Feature Extraction**:
   Extracts 40-dimensional MFCC features from audio files with a fixed length.

2. **Text Tokenization**:
   Tokenizes transcripts at the character level and pads them to match audio feature length.

3. **Model Architecture**:

   * Bidirectional LSTM
   * TimeDistributed Dense layers
   * Softmax output per time step

4. **Training**:
   Model is trained using categorical crossentropy and validated on a test split.

5. **Evaluation**:
   Reports final test accuracy and saves the model in `.h5` format.

---

## ✅ Output Example

```
Test accuracy: 95.00%
Predicted Transcript: hello
```

---

## 💾 Saving the Model

Model is saved as:

```python
model.save('speech_recognition_model.h5')
```

Or using Keras format:

```python
model.save('speech_recognition_model.keras')
```


---

## 📌 Notes

* Ensure `.wav` and `.txt` filenames match.
* Works best for short audio with limited vocabulary.
* Tune `max_len` if needed for different audio lengths.

---

## 👨‍💻 Developer

* **Name**: Gaurakh
* **Email**: [Gmail](mailto:gaurakh.dev@gmail.com)
* **Portfolio**: [Gaurakh-codes](https://gaurakh-codes.netlify.app/)

