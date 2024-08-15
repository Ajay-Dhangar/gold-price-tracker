# Gold and Silver Prices Web App

![License](https://img.shields.io/github/license/Ajay-Dhangar/gold-price-tracker)
![Last Commit](https://img.shields.io/github/last-commit/Ajay-Dhangar/gold-price-tracker)
![Repo Stars](https://img.shields.io/github/stars/Ajay-Dhangar/gold-price-tracker?style=social)

## Overview

The **Gold and Silver Prices Web App** is a simple, responsive web application that displays the latest prices of Gold and Silver in USD. The prices are fetched from the [GoldAPI](https://www.goldapi.io/) and displayed dynamically on the page.

## Features

- **Live Gold Prices**: Fetches and displays the latest Gold prices.
- **Live Silver Prices**: Fetches and displays the latest Silver prices.
- **Responsive Design**: Optimized for both desktop and mobile devices.

## Demo

Check out the live demo: [Gold and Silver Prices Web App](https://ajay-dhangar.github.io/gold-price-tracker/)

## Technologies Used

- **HTML**: For structuring the web page.
- **CSS**: For styling the UI components and layout.
- **JavaScript**: For fetching the data from the API and updating the UI.

## Installation

First, ensure you have the forked repository on your local machine. Then, follow these steps:

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/gold-price-tracker.git
   ```

2. Navigate to the project directory:

   ```bash
   cd gold-price-tracker
   ```

3. Open the `index.html` file in your preferred web browser.

## Usage

- Simply open the app in a web browser to view the latest prices of Gold and Silver.
- The app automatically updates the prices each time it is loaded.

## Code Structure

- **index.html**: The main HTML file containing the structure of the web page.
- **styles.css**: The CSS file containing the styles and layout of the web app.
- **script.js**: The JavaScript file responsible for fetching data from the API and updating the DOM.

## API Integration

This project integrates with the [GoldAPI](https://www.goldapi.io/) to fetch live prices of Gold and Silver.

```javascript
var myHeaders = new Headers();
myHeaders.append("x-access-token", "your-access-token");
myHeaders.append("Content-Type", "application/json");

var requestOptions = {
    method: 'GET',
    headers: myHeaders,
    redirect: 'follow'
};

// Fetching Gold Price
fetch("https://www.goldapi.io/api/XAU/USD", requestOptions)
    .then(response => response.json())
    .then(result => {
        document.getElementById("goldPrice").innerHTML = "<strong>Gold Price:</strong> $" + result.price.toFixed(2);
    })
    .catch(error => console.log('error', error));

// Fetching Silver Price
fetch("https://www.goldapi.io/api/XAG/USD", requestOptions)
    .then(response => response.json())
    .then(result => {
        document.getElementById("silverPrice").innerHTML = "<strong>Silver Price:</strong> $" + result.price.toFixed(2);
    })
    .catch(error => console.log('error', error));
```

## Contributing

Contributions are welcome! Please follow these steps to contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit them (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

If you have any questions, feel free to reach out:

- **Name**: Ajay Dhangar
- **Email**: ajaydhangar49@gmail.com
- **GitHub**: [Ajay-Dhangar](https://github.com/Ajay-Dhangar)
- **LinkedIn**: [Ajay Dhangar](https://www.linkedin.com/in/ajay-dhangar/)
