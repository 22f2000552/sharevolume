# SEC Entity Common Stock Shares Outstanding Viewer

This project provides a single-page responsive HTML application (SPA) built with Tailwind CSS to visualize the maximum and minimum reported common stock shares outstanding for a given company, fetching data directly from the U.S. Securities and Exchange Commission (SEC) EDGAR API.

## Features

- **Dynamic Data Fetching:** Retrieves `EntityCommonStockSharesOutstanding` data for a specified CIK (Central Index Key) from the SEC API.
- **Min/Max Value Extraction:** Filters data for fiscal years (`fy`) greater than 2020 and identifies the highest and lowest reported share outstanding values along with their respective fiscal years.
- **Interactive CIK Input:** Allows users to view data for different companies by providing a CIK in the URL query parameter (e.g., `index.html?CIK=0001018724`).
- **Responsive Design:** Utilizes Tailwind CSS for a clean, modern, and mobile-friendly user interface.
- **No Page Reloads:** Updates the displayed data dynamically without a full page refresh when changing the CIK.

## Getting Started

To run this application, simply open the `index.html` file in your web browser.

### Initial Load

By default, the application will load data for **Allegion Public Limited Company**, with CIK `0001579241`.

### Viewing Data for Other Companies

You can specify a different company's CIK by appending a `CIK` query parameter to the URL.

**Example:**

To view data for Apple Inc. (CIK `0000320193`):
`file:///path/to/your/index.html?CIK=0000320193`

**Note on SEC API and CORS:**
Direct client-side `fetch()` requests to `data.sec.gov` might encounter Cross-Origin Resource Sharing (CORS) restrictions in some browser environments. For production use or strict browser policies, it is recommended to proxy these requests through a backend server (e.g., using Node.js, Python Flask, etc.) to avoid CORS issues and manage rate limits more effectively. This application directly fetches from the SEC API for demonstration purposes, assuming the environment allows it or CORS is lenient.

## Project Structure

- `index.html`: The main single-page application, including HTML structure, Tailwind CSS, and JavaScript logic.
- `README.md`: This file, providing an overview and instructions.
- `LICENSE`: The MIT License text.

## Technologies Used

- **HTML5:** Standard markup for web pages.
- **Tailwind CSS:** A utility-first CSS framework for rapid UI development.
- **JavaScript (ES6+):** For dynamic data fetching and DOM manipulation.

## License

This project is licensed under the MIT License - see the `LICENSE` file for details.
