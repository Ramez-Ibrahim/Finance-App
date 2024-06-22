# Stock Data Fetcher

This project is a simple Flask web application that fetches stock data using the `yfinance` library and displays it on a web interface.

## Features

- Fetches current and open stock prices for a given ticker symbol.
- Simple web interface to input the ticker symbol.
- Displays stock prices on the web interface.
- Automatically updates stock prices every 15 seconds.
- Stores ticker symbols in local storage to persist data across sessions.
- Allows removal of ticker symbols from the list.

## Requirements

- Python 3.x
- Flask
- yfinance
- jQuery

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/ramez08/Finance-App.git
    cd Finance-App
    ```

2. Install the required Python packages:

    ```bash
    pip install Flask yfinance
    ```

## Usage

1. Run the Flask application:

    ```bash
    python app.py
    ```

2. Open your web browser and go to `http://127.0.0.1:5000/`.

3. Enter the stock ticker symbol in the input field and submit.

4. The application will display the current and open prices of the stock and automatically update every 15 seconds.

## Project Structure

- `app.py`: The main Flask application file.
- `templates/index.html`: The HTML template for the web interface.
- `static/style.css`: The CSS file for styling the web interface.
- `static/script.js`: The JavaScript file for client-side functionality.
- `requirements.txt`: A list of Python packages required to run the application.

## JavaScript Functionality

- The JavaScript code is responsible for managing ticker symbols, updating stock prices, and handling the UI interactions.
- Ticker symbols are stored in `localStorage` to persist data across sessions.
- Stock prices are updated every 15 seconds.
- The stock price change is color-coded based on the percentage change:
    - Dark Red: -2% or more
    - Red: Negative but less than -2%
    - Gray: No change
    - Green: Positive but less than 2%
    - Dark Green: 2% or more
- Price changes are highlighted with a flash effect:
    - Red flash for price decrease
    - Green flash for price increase

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request.

## Acknowledgements

- [Flask](https://flask.palletsprojects.com/)
- [yfinance](https://github.com/ranaroussi/yfinance)
- [jQuery](https://jquery.com/)
- This project was based on a tutorial from [YouTube](https://youtu.be/GSHFzqqPq5U?si=MpgIx21QN2h9j8nF).
