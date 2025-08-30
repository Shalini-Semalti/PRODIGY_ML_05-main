Food Recognition and Calorie Estimation Model
This project develops a deep learning model that can recognize food items from images and estimate their calorie content, helping users track their dietary intake and make informed food choices.

Dataset used: Food-101 Dataset

📌 Features
🔍 Recognizes 101 different food categories from images
🔢 Estimates average calorie content for each food item
📊 Provides insights into dietary intake tracking
🧠 Uses Convolutional Neural Networks (CNNs) for classification
🔄 Includes data augmentation for better accuracy
📂 Project Structure
📁 Food-Recognition-Calorie-Estimator
│── 📄 food_recognition_calorie_estimation.ipynb   # Main Jupyter Notebook
│── 📄 README.md                                   # Project documentation
│── 📄 calorie_mapping.json                        # Food-to-calorie mapping file
│── 📁 food-101/                                   # Dataset (after extraction)
│   └── 📁 images/                                 # Food category images
⚙️ Installation & Setup
Clone this repository (or download as zip):

git clone https://github.com/yourusername/food-recognition-calorie-estimation.git
cd food-recognition-calorie-estimation
Install dependencies:

pip install -r requirements.txt
Configure Kaggle API (to download dataset):

Go to Kaggle Account Settings

Create a new API Token → kaggle.json will be downloaded

Place it inside:

Windows: C:\Users\<YourUsername>\.kaggle\kaggle.json
Linux/Mac: ~/.kaggle/kaggle.json
Download and unzip dataset:

kaggle datasets download -d dansbecker/food-101
unzip food-101.zip -d ./food-101
🚀 Usage
Open the Jupyter Notebook:

jupyter notebook food_recognition_calorie_estimation.ipynb
Run all cells step by step.

To test prediction on a custom image:

test_img = "./food-101/food-101/images/pizza/1005649.jpg"
predict_food(test_img)
Output Example:

Predicted Food: pizza  
Estimated Calories: 285 kcal
🧠 Model Architecture
Input Layer → 128x128x3 images
3× Convolution + MaxPooling layers with Batch Normalization
Fully Connected Dense Layers
Softmax Output Layer (101 food classes)
📊 Results
Achieved ~80% accuracy on test dataset (can be improved with transfer learning).
Calorie estimation added using predefined calorie mapping dictionary.
🔮 Future Improvements
Use Transfer Learning (ResNet, EfficientNet, Inception) for higher accuracy
Build a mobile/web app interface
Incorporate portion size estimation for more accurate calorie calculation
Connect with nutrition databases for better food info
