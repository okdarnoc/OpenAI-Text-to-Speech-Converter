# Cantonese Text-to-Speech Converter

A Python script that converts text files to natural-sounding Cantonese speech using OpenAI's text-to-speech API. This tool is specifically designed for processing text files with proper Cantonese pronunciation and formatting rules.

## Features

- 🎯 Batch processing of text files to MP3
- 🗣️ Natural Cantonese text-to-speech with the "ballad" voice
- 🔄 Automatic file overwrite protection
- 📁 Automatic output directory creation
- ⚠️ Comprehensive error handling

### Text Processing Rules

The script automatically handles various text elements according to Cantonese speaking conventions:

1. **Text Style**
   - Converts written text to natural Cantonese speaking style
   - Preserves foreign language content as-is

2. **Number Formats**
   ```
   100 → 一百
   1000 → 一千
   10000 → 一萬
   100000 → 十萬
   1000000 → 百萬
   ```

3. **Date and Time**
   ```
   2022-01-01 → 二零二二年一月一日
   13:00 → 下午一時
   ```

4. **Special Formats**
   ```
   $100 → 一百港元
   50% → 百分之五十
   123-4567 → 一二三四五六七
   info@2cexam.com → i n f o @ 2 c e x a m . c o m
   ```

## Prerequisites

- Python 3.7 or higher
- OpenAI API key
- Internet connection

## Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/cantonese-tts-converter.git
cd cantonese-tts-converter
```

2. Install the required package:
```bash
pip install openai
```

## Usage

1. Run the script:
```bash
python tts_converter.py
```

2. When prompted:
   ```
   Enter your OpenAI API key: [Enter your API key]
   Enter the directory path containing your text files: [Path to your txt files]
   Enter the directory path where you want to save the audio files: [Output path]
   ```

3. The script will:
   - Scan for all .txt files in the input directory
   - Process each file one by one
   - Generate MP3 files in the output directory
   - Ask for confirmation before overwriting existing files

## Script Structure

```python
tts_converter.py
├── process_text_files(api_key, input_dir, output_dir)
│   └── Converts text files to MP3
└── main()
    └── Handles user input and process flow
```

## Example Usage

1. Prepare your text file (example.txt):
```
今日日期係2023年12月25日，而家時間係下午2:30。
股票價格升咗50%，由$100升到$150。
如果有問題，請電123-4567或者電郵至info@example.com。
```

2. Run the script and provide the necessary inputs.

3. The script will create an MP3 file with natural Cantonese speech.

## Error Handling

The script includes error handling for:
- Invalid directory paths
- File access issues
- API communication errors
- Invalid file formats
- Existing file conflicts

## Technical Notes

- Uses OpenAI's GPT-4o audio preview model
- Outputs MP3 format audio files
- Uses UTF-8 encoding for text files
- Preserves original filename structure (changes extension to .mp3)

## Limitations

- Currently supports only Cantonese language
- Processes .txt files only
- Requires active internet connection
- Subject to OpenAI API rate limits
- Uses fixed voice setting ("ballad")

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

If you encounter any issues or have questions:
1. Check the error message displayed by the script
2. Ensure your text files are in UTF-8 encoding
3. Verify your OpenAI API key is valid
4. Create an issue in the GitHub repository

---

## Quick Start Example

```bash
# Clone repository
git clone https://github.com/yourusername/cantonese-tts-converter.git

# Install requirement
pip install openai

# Run script
python tts_converter.py

# Follow prompts
Enter your OpenAI API key: sk-...
Enter the directory path containing your text files: ./input
Enter the directory path where you want to save the audio files: ./output
```
