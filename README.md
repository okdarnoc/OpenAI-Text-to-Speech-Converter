# OpenAI Text-to-Speech Converter

A Python script that converts text files to speech using OpenAI's text-to-speech API. This script is specifically optimized for Cantonese text-to-speech conversion with detailed formatting rules and guidelines.

## Features

- Batch conversion of text files to MP3 format
- Specialized Cantonese text-to-speech formatting rules
- Automatic handling of:
  - Numbers and dates
  - Time formats
  - Currency
  - Percentages
  - Phone numbers
  - Email addresses
- Configurable voice options
- File overwrite protection
- Robust error handling

## Prerequisites

- Python 3.7 or higher
- OpenAI API key
- Internet connection

## Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/openai-tts-converter.git
cd openai-tts-converter
```

2. Install required packages:
```bash
pip install openai
```

3. Set up your OpenAI API key (recommended to use environment variables):
```bash
export OPENAI_API_KEY='your-api-key-here'
```

## Usage

1. Place your text files in a directory
2. Run the script:
```bash
python tts_converter.py
```
3. Follow the prompts to:
   - Enter your OpenAI API key (if not set in environment)
   - Specify input directory containing text files
   - Specify output directory for MP3 files

## Text Formatting Rules

The script includes comprehensive rules for Cantonese text-to-speech conversion:

1. **Speech Style**: Uses natural Cantonese speaking style
2. **Regional Terms**: Proper handling of regional terms (Taiwan, Macau, Hong Kong)
3. **Content Focus**: Reads only specified content without additions
4. **Pronunciation**: Natural tone with appropriate emotion
5. **Numbers**: Converts numbers to Chinese format
   - "100" → "一百"
   - "1000" → "一千"
   - "10000" → "一萬"
   - "100000" → "十萬"
   - "1000000" → "百萬"
6. **Dates**: Converts dates to Chinese format
   - "2022-01-01" → "二零二二年一月一日"
7. **Time**: Converts time to Chinese format
   - "13:00" → "下午一時"
8. **Currency**: Converts currency to Chinese format
   - "$100" → "一百港元"
9. **Percentages**: Converts percentages to Chinese format
   - "50%" → "百分之五十"
10. **Phone Numbers**: Converts phone numbers to Chinese format
    - "123-4567" → "一二三四五六七"
11. **Email Addresses**: Spells out email addresses
    - "info@2cexam.com" → "i n f o @ 2 c e x a m . c o m"

## Code Structure

The script is organized into two main functions:

```python
def process_text_files(api_key, input_dir, output_dir):
    """
    Process text files and convert to MP3 using OpenAI's text-to-speech API.
    
    Args:
        api_key (str): OpenAI API key for authentication
        input_dir (str): Directory path containing input text files
        output_dir (str): Directory path where output MP3 files will be saved
    """

def main():
    """
    Main function to handle user input and orchestrate the text-to-speech conversion process.
    """
```

## Example

```bash
$ python tts_converter.py
Enter your OpenAI API key: sk-your-api-key
Enter the directory path containing your text files: /path/to/input
Enter the directory path where you want to save the audio files: /path/to/output
```

## Error Handling

The script includes comprehensive error handling for:
- Invalid directories
- File read/write errors
- API errors
- File format issues
- Existing file conflicts

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Security Note

⚠️ IMPORTANT: Never commit your API key to version control. Always use environment variables or secure configuration files to store sensitive information.

## Requirements

Create a `requirements.txt` file with:

```
openai>=1.0.0
```

## Support

For support, please open an issue in the GitHub repository.
