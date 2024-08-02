# DistillPDF

DistillPDF is an advanced PDF optimization and transformation tool designed for high-performance environments where precision and file size reduction are critical. It's suitable for both commercial and academic applications, employing adaptive concurrency management and Bayesian optimization to balance processing speed with system resource constraints and optimization quality.

## Features

- Image resizing and compression with configurable dimensions and quality
- Conversion of colored images to grayscale to reduce complexity
- Flattening of PDF annotations and form fields to static content
- Aggressive font subsetting to include only the characters used in the document
- Metadata removal for enhanced privacy and security
- Cleanup of unreferenced PDF resources to shrink file size
- Content stream optimization to strip unnecessary data
- Vector graphic simplification using Bayesian optimization for optimal results
- Text-aware and shape-aware vector optimization to preserve important content
- Multi-threaded processing for performance optimization
- Parallel batch processing of multiple PDFs from a directory
- Adaptive concurrency management to handle system file descriptor limits
- Extreme optimization mode for maximum file size reduction
- Detailed logging of processes and errors for troubleshooting and analysis

## Benefits for Vector Embeddings and RAG Systems

The optimizations performed by DistillPDF can offer benefits for creating vector embeddings and using PDFs in Retrieval-Augmented Generation (RAG) systems:

- **Processing Speed**: Smaller file sizes may lead to faster text extraction for embedding creation, especially beneficial for large PDF corpora.
- **Storage Efficiency**: Reduced file sizes allow storing more documents in vector databases, potentially improving the knowledge breadth for RAG systems.
- **Cleaner Text Extraction**: Flattening annotations and form fields may result in cleaner text extraction, potentially improving embedding quality.
- **Noise Reduction**: Cleaning unreferenced resources might remove noise that could otherwise be captured in the embedding process.

## Setup

Ensure you have Python >= 3.9 installed.

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/distillpdf.git
   cd distillpdf
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

To use DistillPDF, provide an input PDF file or directory and an output destination, along with optional flags for grayscale conversion, flattening, and specifying the number of processing threads.

Basic usage for a single file:
```
./distillpdf input.pdf --output output.pdf
```

With options:
```
./distillpdf input.pdf --output output.pdf --threads=4 --grayscale --flatten
```

For processing a directory of PDFs:
```
./distillpdf input_directory/ --output_dir=optimized_pdfs/ --threads=4 --grayscale --flatten
```

### Options

- `--output`: Output optimized PDF file (for single file input)
- `--output_dir`: Output directory for optimized PDFs (for directory input)
- `--threads`: Number of threads to use for processing (default: number of available CPU cores)
- `--grayscale`: Convert images to grayscale
- `--flatten`: Flatten form fields and annotations
- `--max_files`: Maximum number of files to process concurrently (default: 100)

## Contributing

Contributions to DistillPDF are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the GNU Affero General Public License v3.0. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

This project uses several open-source libraries including PyMuPDF (fitz), pikepdf, OpenCV, scikit-learn, scipy, and numpy. We're grateful to the maintainers and contributors of these projects.

## Author

Juan Sugg Gilbert
juanpedrosugg [at] gmail [dot] com