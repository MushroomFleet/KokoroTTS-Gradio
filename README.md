# Kokoro TTS Gradio Project
![demoUI](https://raw.githubusercontent.com/MushroomFleet/KokoroTTS-Gradio/refs/heads/main/images/demo.png)

This project is designed to process voice data using Python and various supporting files. It includes capabilities for voice processing, audio analysis, and audio generation. The latest update introduces a new Blending feature that allows for the combination of two distinct voice profiles to generate unique speech outputs.

NOTE: This was initially offered using "uv" based packages, but it now uses normal "pip install" packages. As a result, if you had the first version, you would need to delete the old .venv, and re-run the install.bat file.

## Installation

1. Ensure you have Python installed (check the required Python version in the `.python-version` file).
2. Clone or download the repository to your local machine.
3. Run the `install.bat` file to set up any required dependencies and environment configurations.
4. Verify that all the necessary files are present, including:
   - Python scripts: `kokoro-Gradio.py`, `hello.py`
   - Model file: `kokoro-v1.0.onnx`
   - Voice configuration: `voices-v1.0.bin` and `voice-data.json`
   - Batch scripts: `install.bat`, `run-cli.bat`

## Running the Application

You can run the application in several ways:

- **CLI Mode:**  
  Execute `run-cli.bat` from the command line to start the application in command-line mode.

- **Gradio UI Mode:**  
  Run the `kokoro-Gradio.py` script to launch the application with a graphical user interface powered by Gradio. The Gradio interface now features two tabs:
   - **Standard:**  
     Use this tab to generate speech using a single, selected voice.
   - **Blending:**  
     This new tab allows you to blend two voices. Within the Blending tab, enter the desired text, set the speed, select two different voices, and choose a blend mode (currently "default"). The blending function combines the vocal styles of both selected voices equally (50/50) and generates a blended audio file saved in the `output/` directory with a timestamped filename (e.g., `blended_audio_YYYYMMDD_HHMMSS.wav`).

- **Testing:**  
  For initial tests, you can run `hello.py` to check that the basic functionality is working.

## User Functions

- **Voice Processing and Analysis:**  
  The application utilizes the `kokoro-v1.0.onnx` model for voice processing and leverages the configuration in `voices-v1.0.bin` along with `voice-data.json` to manage voice data.

- **Audio Handling:**  
  Processed audio outputs are saved in the `output/` directory. Check this folder for generated audio files after processing.

- **Voice Blending:**  
  With the addition of the Blending tab in the Gradio UI, you can now generate audio by blending two distinct voice profiles. The process involves selecting Voice 1 and Voice 2, entering your desired text and speed, and then utilizing the blend function to generate a unique combined audio output.

- **General Workflow:**  
  Follow the installation steps, run the appropriate script or batch file, and interact with the UI (or CLI) as per your requirements.

## Troubleshooting

- Ensure that you have a compatible Python version installed.
- Make sure that `install.bat` has been executed successfully to set up the environment.
- Check the console output for any error messages if the app does not start as expected.
- Verify file integrity and paths if issues persist.

For further support or to report issues, please refer to the project documentation or contact the development team.
