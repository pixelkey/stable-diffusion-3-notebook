# Simple Notebook for Stable Diffusion 3

## Setup Instructions to Run Stable Diffusion 3 Locally

This notebook demonstrates how to run Stable Diffusion 3 locally using a Python environment and a Jupyter Notebook

### Prerequisites

- Python 3.11.8 (3.11+ should be fine)
- `pyenv` for managing Python versions
- `pip` for managing Python packages
- Authozation to the Huggingface repo:
Visit https://huggingface.co/stabilityai/stable-diffusion-3-medium and submit the form for access for your HF account.
- You can obtain a token from your Hugging Face account settings. Read access is all you need. https://huggingface.co/settings/tokens
- Jupyter Notebook


### Setting Up Python PyEnv Environment

1. **Install `pyenv`**: Follow the [official guide](https://github.com/pyenv/pyenv#installation) to install `pyenv` if you haven't already.

2. **Install and Set the Python Version**:
   ```bash
   pyenv install 3.11.8
   pyenv local 3.11.8
   ```

3. **Create a Virtual Environment**:
   Create a virtual environment to isolate your dependencies:
   ```bash
   python -m venv .env
   ```

4. **Activate the Virtual Environment**:
   ```bash
   source .env/bin/activate
   ```

5. **Verify Python Version**:
   Ensure you are using the correct Python version:
   ```bash
   python --version
   ```
   To check if you are in the correct environment, you can use the `which python` command in your terminal. This will display the path to the Python executable that is currently being used. Make sure that the displayed path matches the one you expect for your Python 3.11.8 environment.

### Installing Project Dependencies

To install the prerequisites for this project, you can use `pip`. Run the following command in your terminal:

```shell
pip install -r requirements.txt
```

This will install all the necessary dependencies listed in the `requirements.txt` file.

If you encounter a warning about `IProgress`, update `jupyter` and `ipywidgets`:

```shell
pip install --upgrade jupyter ipywidgets
```

### Adding Your Hugging Face Token

The notebook requires a Hugging Face token for authentication. The token can be set in a `.env.hf` file.

1. **Create .env.hf File**:
   In the root directory of your project, create a file named `.env.hf`.

2. **Add Your Hugging Face Token**:
   Add the following line to the `.env.hf` file:
   ```plaintext
   HUGGINGFACE_TOKEN=your_hugging_face_token_here
   ```

   Replace `your_hugging_face_token_here` with your actual Hugging Face token. You can obtain a token from your Hugging Face account settings. https://huggingface.co/settings/tokens

### Running the Notebook

Once the installation is complete, you can proceed with running the notebook locally.

1. **Launch Jupyter Notebook**:
   ```bash
   jupyter notebook
   ```
   This will open a browser window or tab with the Jupyter Notebook interface.

2. **Open the Notebook**:
   Navigate to the notebook file (e.g., `sd3.ipynb`) and open it.

3. **Run the Cells**:
   Follow the instructions within the notebook to run the cells and generate images using Stable Diffusion 3.

### Saving and Displaying Images

The notebook includes code to save generated images to a local directory and display them in a grid layout.

- **Save Images**: Generated images are saved in the `output` directory with filenames based on the seed and sanitized prompt text.
- **Display Images**: Images are displayed in a grid layout using `matplotlib`.

### Additional Information

- **Model Caching**: The notebook is set up to cache the model locally after the first download, reducing redundant downloads in subsequent runs.
- **Custom Filenames**: The code ensures that generated images are saved with meaningful filenames, including the seed and a sanitized version of the prompt.

### Troubleshooting

If you encounter any issues, consider the following steps:

- Ensure you are in the correct Python environment (`which python`).
- Verify that all dependencies are installed correctly (`pip list`).
- Check for typos in the `requirements.txt` file or the commands you run.

For further assistance, feel free to open an issue in the repository.

### Contributing

Contributions are welcome! If you'd like to contribute, please fork the repository and create a pull request with your changes.

### License

This project is licensed under the MIT License.

---

By following the instructions above, you should be able to set up and run the Stable Diffusion 3 notebook locally on your machine. Happy coding!