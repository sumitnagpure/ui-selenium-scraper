# Web Scraping Application with Selenium

## Description
This application is a simple Flask-based web scraper that uses Selenium to extract data from websites based on user-specified identifiers. It provides two functionalities:

1. **Display results on a webpage:** Extracts elements from a website and displays them on a result page.
2. **Save results to a text file:** Extracts elements and saves them into a text file for download.

## Features
- User inputs the target website URL and the desired identifiers (e.g., XPath, ID, class name).
- Uses Selenium WebDriver for web scraping.
- Supports multiple identifiers for extraction.
- Allows saving scraped data into a `.txt` file.
- Renders results dynamically on a webpage or provides them as a downloadable file.

## Prerequisites
- Python 3.x
- Flask
- Selenium
- A web driver (e.g., Chrome WebDriver)

## Installation

1. Clone this repository or download the files.
2. Install the required Python packages:
   ```bash
   pip install flask selenium
   ```
3. Download and install the appropriate web driver for your browser (e.g., Chrome WebDriver) and ensure it is added to your system's PATH.

## Usage

### Running the Application
1. Open a terminal and navigate to the project directory.
2. Start the Flask application:
   ```bash
   python app.ipynb
   ```f
3. Open a web browser and navigate to `http://127.0.0.1:5000/`.

### Application Pages

#### Index Page (`/`)
The landing page allows the user to:
- Enter the website URL.
- Specify the type of identifier (e.g., XPath, ID, class name, etc.).
- Provide the identifier value.

#### Scraping Results (`/scrape`)
- If single identifiers are used, scraped results are displayed dynamically on a result page (`result.html`).
- If multiple identifiers are used, scraped results are saved in a text file (`scraped_data.txt`) for download.

## File Structure

```
.
|-- app.ipynb                 # Flask application
|-- templates/
|   |-- index.html         # HTML form for user input
|   |-- result.html        # Displays results dynamically
|-- scraped_data.txt       # Generated file with scraped data (created at runtime)
|-- README.md              # Documentation file (this file)
```

## Example Input
### Single Identifier
- Website: `https://example.com`
- Identifier: `id`
- Identifier Value: `example-id`

### Multiple Identifiers
- Website: `https://example.com`
- Identifiers:
  - XPath: `//div[@class='example']`
  - Class Name: `example-class`

## Example Output
### Result Page
- Displays the extracted data as a list.

### Text File
```
Example Item 1
Example Item 2
Example Item 3
```

## Notes
- Ensure the website being scraped allows web scraping and complies with its terms of service.
- Selenium may require browser updates to match the web driver version.
- Set `debug=True` in `app.py` for debugging during development.

## Troubleshooting
- **Issue:** WebDriver not found.
  - **Solution:** Verify the web driver is installed and added to your system's PATH.
- **Issue:** Elements not found.
  - **Solution:** Check the identifiers and ensure they match the website's structure.

## License
This project is open-source and available for personal and educational use. Ensure compliance with third-party website policies when using this tool.

