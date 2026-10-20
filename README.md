# Next Word Prediction

A next-word prediction app built with Python, TensorFlow/Keras, and Streamlit.

## Features

- Loads a trained TensorFlow/Keras language model
- Predicts the next word from user-provided text
- Simple interactive web interface powered by Streamlit

## Project Structure

```text
next_word_prediction/
├── app.py
├── requirements.txt
├── README.md
└── next_word_model.keras  # Example name; use your actual model filename
```

## Requirements

- Python version compatible with the TensorFlow version used by your model
- Dependencies listed in `requirements.txt`

## Run Locally

1. Clone or download this repository.
2. Open a terminal in the project folder.
3. (Recommended) Create and activate a virtual environment.

   **Windows**
   ```bash
   python -m venv .venv
   .venv\Scripts\activate
   ```

   **macOS/Linux**
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```

4. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

5. Start the app:

   ```bash
   streamlit run app.py
   ```

## Deploy on Streamlit Community Cloud

1. Push `app.py`, `requirements.txt`, the README, and all required model/tokenizer files to your GitHub repository.
2. In Streamlit Community Cloud, create an app and select the repository and `app.py` as the entry point.
3. Deploy the app.

If deployment fails, open the app's **Manage app → Logs** and check the full error. TensorFlow compatibility depends on the Python version and the environment used to train/save the model.

## Model and Tokenizer Files

Make sure the model file and any tokenizer, vocabulary, or configuration files your code loads are included in the repository, and that the paths in `app.py` match their exact filenames. Do not rename your model file unless you also update the code.

## Troubleshooting

- **`ModuleNotFoundError: No module named 'tensorflow'`**: Check that `tensorflow` is in `requirements.txt`, commit the file, and redeploy.
- **Model file not found**: Verify the filename and relative path used by `load_model(...)`.
- **TensorFlow/Keras compatibility error**: Pin compatible package versions based on the Python version and TensorFlow/Keras version used to save the model.

## License

Add a license if you intend to distribute this project publicly.
