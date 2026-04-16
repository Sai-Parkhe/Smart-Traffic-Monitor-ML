Smart-Traffic-Monitor-ML 🚦
A high-performance, real-time vehicle detection and traffic analytics system optimized for NVIDIA GPU acceleration. This project leverages YOLOv8 to identify various vehicle types and automatically generates organized Excel reports with statistical tallies.

🌟 Key Features
Hardware Accelerated: Optimized for NVIDIA RTX 3050 using CUDA 12.1.

Real-Time Detection: Processes webcam feeds to identify Bikes, Cars, Buses, Boats, Planes, and more.

Custom Object Mapping: Translates standard AI labels into project-specific categories.

Automated Analytics: Generates a numbered Excel report (Detection_Report_N.xlsx) after every session.

Data Summarization: Automatically appends a "Vehicle Summary Tally" at the bottom of the Excel logs.

🛠️ Tech Stack
Model: YOLOv8 (Ultralytics)

Libraries: OpenCV, PyTorch, Pandas, Openpyxl

Hardware: NVIDIA RTX 3050 (Laptop)

Environment: Python 3.11 / Conda

🚀 Installation & Setup
1. Clone the Repository
Bash
git clone https://github.com/YOUR_USERNAME/Smart-Traffic-Monitor-ML.git
cd Smart-Traffic-Monitor-ML
2. Install Dependencies
Ensure you have Python installed, then run:

Bash
pip install ultralytics opencv-python pandas openpyxl torch torchvision torchaudio
Note: For GPU support, ensure your PyTorch installation matches your CUDA version.

3. Data Configuration
The system uses a vehicle_data.yaml file to map dataset paths. Ensure your dataset is structured as follows:

Plaintext
/dataset
  /train
    /images
    /labels
  /val
    /images
    /labels
📈 Training the Model
The model was trained using Transfer Learning on a custom vehicle dataset.

Epochs: 50

Image Size: 640

Device: GPU (device=0)

To retrain, run the training cell within the Jupyter Notebook.

🖥️ Usage
Place your trained best.pt file in the root directory.

Launch the Jupyter Notebook: ann mini project.ipynb.

Run the Real-Time Analytics System cell.

Press 'q' to stop the feed and automatically save the Excel report.

📊 Sample Output
The system generates an Excel file containing:

Detection Log: Timestamped entries of every vehicle seen.

Summary Tally: A table showing the total count for each vehicle category (e.g., Car: 45, Bike: 12).
