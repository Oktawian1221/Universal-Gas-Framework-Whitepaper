# Whitepaper Generator

Automated LaTeX whitepaper generation with a single command.

## Quick Start

```bash
# Make executable
chmod +x generate.sh

# Generate whitepaper
./generate.sh

# Or with custom name
./generate.sh my-whitepaper
```

## Setup

### Prerequisites
- LaTeX distribution (TeX Live, MiKTeX, etc.)
- `pdflatex` and `bibtex` in PATH

### Installation
```bash
git clone <your-repo>
cd whitepaper-generator
chmod +x generate.sh
```

## Usage

### Basic Generation
```bash
./generate.sh                    # Creates whitepaper_TIMESTAMP.pdf
./generate.sh custom-name        # Creates custom-name_TIMESTAMP.pdf
```

### NPM Scripts (optional)
```bash
npm run generate                 # Generate with default name
npm run build                    # Same as generate
npm run clean                    # Clean output and temp files
npm run watch                    # Auto-regenerate on file changes
```

### Make Commands
```bash
make                            # Generate PDF
make clean                      # Clean auxiliary files
```

## Project Structure

```
├── src/
│   ├── main.tex               # Main LaTeX file
│   └── ...                    # Other LaTeX files
├── output/                    # Generated PDFs
├── generate.sh               # Generation script
├── Makefile                  # Make targets
└── README.md                 # This file
```

## Customization

Edit `generate.sh` to modify:
- LaTeX engine (pdflatex, xelatex, lualatex)
- Output directory
- File naming convention
- Cleanup behavior