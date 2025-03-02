# ✨ Keras 3: Deep Learning for Humans ✨

Keras 3 is a multi-backend deep learning framework, with support for **JAX**, **TensorFlow**, **PyTorch**, and **OpenVINO** (for inference-only).
Effortlessly build and train models for **computer vision**, **natural language processing**, **audio processing**, **timeseries forecasting**, **recommender systems**, etc.

### 🌟 Why Choose Keras 3?
- **🚀 Accelerated model development**: Ship deep learning solutions faster thanks to the high-level UX of Keras and the availability of easy-to-debug runtimes like PyTorch or JAX eager execution.
- **⏱️ State-of-the-art performance**: Pick the backend that is the fastest for your model architecture (often JAX!), achieving speedups from **20% to 350%** compared to other frameworks. [✨ Benchmark here ✨](https://keras.io/getting_started/benchmarks/).
- **💻 Datacenter-scale training**: Scale confidently from your laptop to large clusters of GPUs or TPUs.

Join nearly **three million developers**, from burgeoning startups to global enterprises, in harnessing the power of **Keras 3**.

---
## ✨ Installation Guide ✨

### 🔄 Install with pip
Keras 3 is available on PyPI as `keras`. (**Keras 2 remains available as `tf-keras`**).

1. Install `keras`:

   ```sh
   pip install keras --upgrade
   ```

2. Install backend package(s):
   
   To use `keras`, install at least one backend: `tensorflow`, `jax`, or `torch`.
   **Note**: `tensorflow` is required for some features (e.g., certain preprocessing layers & `tf.data` pipelines).

---

### 🏡 Local Installation
#### ✅ Minimal Installation
Keras 3 is **compatible with Linux & MacOS**. (**Windows users should use WSL2**).

1. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
2. Run installation from root directory:
   ```sh
   python pip_build.py --install
   ```
3. Run API generation script when updating `keras_export` public APIs:
   ```sh
   ./shell/api_gen.sh
   ```

---
### 🚀 Adding GPU Support
The default `requirements.txt` installs **CPU-only** versions of TensorFlow, JAX, and PyTorch.
For GPU support, use `requirements-{backend}-cuda.txt` (requires **NVIDIA driver pre-installed**).

**Example**: Creating a JAX GPU environment with `conda`:
```sh
conda create -y -n keras-jax python=3.10
conda activate keras-jax
pip install -r requirements-jax-cuda.txt
python pip_build.py --install
```

---
## 💪 Configuring Your Backend
Set the backend via an **environment variable** or edit `~/.keras/keras.json`.

**Available backends**: `"tensorflow"`, `"jax"`, `"torch"`, `"openvino"` (inference-only).

Example:
```sh
export KERAS_BACKEND="jax"
```

**In Colab**:
```python
import os
os.environ["KERAS_BACKEND"] = "jax"
import keras
```

**⚠️ Important:** The backend **must be configured before importing** `keras` & cannot be changed afterward.

---
## ♻️ Backwards Compatibility
Keras 3 works as a **drop-in replacement** for `tf.keras` (when using TensorFlow backend).

- **For standard `tf.keras` models**: Use the `.keras` format for `model.save()`.
- **For models with custom components**: Convert them to a **backend-agnostic** implementation in minutes.
- **Dataset flexibility**: Use `tf.data.Dataset` or PyTorch `DataLoaders` with any backend.

---
## 🏆 Why Use Keras 3?

✅ **Run high-level Keras workflows on any framework** – seamlessly switching between **TensorFlow, JAX, and PyTorch**.

✅ **Write custom components** (e.g., layers, models, metrics) that integrate with **any framework**.

✅ **Avoid framework lock-in** – future-proof your ML code!

✅ **For PyTorch users**: Finally, experience the power & usability of **Keras**!

✅ **For JAX users**: Gain a **fully-featured, battle-tested, well-documented** modeling & training library.

Read more in the [📣 Keras 3 release announcement](https://keras.io/keras_3/).

