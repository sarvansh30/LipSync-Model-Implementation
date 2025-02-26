# Lip Sync Model Implementation Assignment

This project implements a lip sync model for generating realistic lip-synced videos as part of an internship assignment. The implementation is based on the open-source Wav2Lip repository, which was used to create the final results.

## Resulting Videos 
**Check the output folder**

## Repository Structure

```
├── wav2lip/                # Cloned Wav2Lip repository (with necessary modifications)
├── input/                  # Contains input files
│   ├── anika_speech.mp4    # Input video created from a static image (40 seconds long)
│   └── input_audio.mp3     # Text-to-speech audio file generated using [PlayHT](https://play.ht)
├── output/                 # Contains generated lip-synced videos
│   ├── result1.mp4         # Final output video (lip-synced)
│   └── result2.mp4         # Additional output video (lip-synced)
├── requirements.txt        # Project dependencies
└── README.md               # This documentation file
```

## Setup and Installation

### Clone the Repository:
```bash
git clone <repository-url>
cd <repository-directory>
```

### Install Dependencies:
```bash
pip install -r requirements.txt
```

### Download the Pre-trained Model:

1. Visit the [Wav2Lip repository](https://github.com/Rudrabha/Wav2Lip) and follow the instructions to download the pre-trained model checkpoint.
2. Place the checkpoint file in an appropriate directory (or specify its path when running the inference).

## Usage

To generate a lip-synced video, run the following command from the project root:
```bash
python inference.py --checkpoint_path <path-to-checkpoint> --face input/anika_speech.mp4 --audio input/input_audio.mp3
```
Replace `<path-to-checkpoint>` with the actual path to your downloaded model checkpoint. The output video(s) will be saved in the `output/` folder.

## Additional Information

### Text-to-Speech:
The audio for this project was generated using the [PlayHT](https://play.ht) website with an Indian accent.

### Wav2Lip:
This project builds upon the open-source [Wav2Lip](https://github.com/Rudrabha/Wav2Lip) repository. For detailed instructions on the model and additional features, please refer to their documentation.

## Acknowledgments

- Many thanks to the creators of Wav2Lip for their excellent open-source contribution.
- Thanks to PlayHT for providing a robust text-to-speech service.
