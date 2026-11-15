# 1. Install Python 3.12 and virtual environment support
sudo apt update
sudo apt install -y python3.12 python3.12-venv

# 2. Create the project directory
mkdir -p ~/DeepLearning
cd ~/DeepLearning

# 3. Create and activate a virtual environment
python3.12 -m venv .venv
source .venv/bin/activate

# 4. Upgrade Python packaging tools
python -m pip install --upgrade pip setuptools wheel

# 5. Install TensorFlow (CPU), Keras and common DL libraries
python -m pip install \
    tensorflow-cpu==2.20.0 \
    keras \
    numpy \
    pandas \
    matplotlib \
    seaborn \
    scikit-learn \
    scipy \
    pillow \
    wfdb

# 6. Install CPU-only PyTorch and Torchvision
python -m pip install torch torchvision \
    --index-url https://download.pytorch.org/whl/cpu

# 7. Install Jupyter Notebook, JupyterLab and kernel support
python -m pip install jupyterlab notebook ipykernel

# 8. Register the virtual environment as a Jupyter kernel
python -m ipykernel install --user \
    --name deeplearning \
    --display-name "Python (Deep Learning)"

# 9. Verify installations
python - <<'PY'
import tensorflow as tf
import keras
import torch
import torchvision
import numpy as np
import pandas as pd
import matplotlib
import sklearn
import wfdb

print("TensorFlow:", tf.__version__)
print("Keras:", keras.__version__)
print("PyTorch:", torch.__version__)
print("Torchvision:", torchvision.__version__)
print("NumPy:", np.__version__)
print("Pandas:", pd.__version__)
print("Scikit-learn:", sklearn.__version__)
print("TensorFlow GPU:", tf.config.list_physical_devices("GPU"))
print("PyTorch GPU:", torch.cuda.is_available())
print("\nAll imports successful.")
PY

# 10. Check package dependencies
python -m pip check

# 11. Launch JupyterLab
jupyter lab
