# 🌍 Country-to-City Excel Generator (Using CountriesNow API)

This is a simple web-based tool built with **HTML + JavaScript** that:

1. Accepts an Excel file containing a list of country names (one per row)
2. Sends API requests to fetch cities for each country using the [CountriesNow API](https://countriesnow.space/)
3. Compiles all results into a new Excel file with the format:  
   `Country | City`
4. Allows download of the final file directly in the browser

---

## 📁 Input Excel Format

Your uploaded Excel file must contain a column named:


**Example:**

| CountryName         |
|---------------------|
| India               |
| United Arab Emirates|
| Afghanistan         |
| France              |

---

## 🚀 How to Use

1. Open `index.html` in your browser.
2. Click **“Upload Excel”** and choose your `.xlsx` file.
3. Click **“Start Processing”**.
4. Once completed, a download will start for `CountryCities.xlsx`.

---

## 📦 Output Format

The output Excel will contain:

| Country   | City       |
|-----------|------------|
| India     | Mumbai     |
| India     | Delhi      |
| France    | Paris      |
| ...       | ...        |

---

## 🛠 Technologies Used

- [SheetJS (xlsx)](https://sheetjs.com/) – For reading and writing Excel files
- [FileSaver.js](https://github.com/eligrey/FileSaver.js/) – For file download
- [CountriesNow API](https://countriesnow.space/) – Free country-to-city data API

---

## 🔗 API Endpoint Used

**POST** `https://countriesnow.space/api/v0.1/countries/cities`

**Request Body:**
```json
{
  "country": "India"
}
{
  "error": false,
  "msg": "...",
  "data": ["City1", "City2", ...]
}
