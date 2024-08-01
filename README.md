# DistilPDF

DistilPDF is an advanced PDF optimization tool that provides comprehensive functionalities to transform and optimize PDF files. It's designed for high-performance environments where precision and file size reduction are critical, suitable for both commercial and academic applications.

## Features

- Image compression and resizing
- Grayscale conversion
- Form field and annotation flattening
- Font subsetting
- Metadata removal
- Unused resource cleanup
- Content stream optimization
- Vector graphic simplification using Bayesian optimization
- Multi-threaded processing for performance optimization

## Setup

Ensure you have Python version 3.8.x installed.

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/distil-pdf.git
   cd distil-pdf
   ```

2. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```

3. Make the script executable:
   ```
   chmod +x distillpdf
   ```

4. (Recommended) Move the `distillpdf` script to a directory in your PATH, and modify the script's shebang to point to your compatible Python binary location.

## Usage

To use DistilPDF, provide an input PDF file and an output destination, along with optional flags for grayscale conversion, flattening, and specifying the number of processing threads.

Basic usage:
```
./distillpdf input.pdf output.pdf
```

With options:
```
./distillpdf input.pdf output.pdf --threads=4 --grayscale --flatten
```

### Options

- `--threads`: Number of threads to use for processing (default: number of available CPU cores)
- `--grayscale`: Convert images to grayscale
- `--flatten`: Flatten form fields and annotations

## Contributing

Contributions to DistilPDF are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the GNU Affero General Public License v3.0. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

This project uses several open-source libraries including PyMuPDF, pikepdf, and others. We're grateful to the maintainers and contributors of these projects.
