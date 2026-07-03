# Soil Symphony 🌱

A Streamlit web app that suggests the most suitable crop to grow based on soil moisture, temperature, and pH level.

## Features

- Simple input form for **moisture (%)**, **temperature (°C)**, and **soil pH**
- Rule-based matching against a database of 60+ crops (grains, vegetables, fruits, spices, and cash crops)
- Displays the recommended crop name along with a reference image
- Sidebar navigation with a **Home Page** (project overview) and **Result Page**

## How It Works

1. Enter your soil's moisture, temperature, and pH values.
2. Click **Show Result**.
3. The app checks your values against predefined ranges for each crop and returns the best match, or an error message if no crop fits the given conditions.

## Tech Stack

- Python
- [Streamlit](https://streamlit.io/)

## Installation

```bash
pip install streamlit
```

## Usage

```bash
streamlit run app.py
```

Replace `app.py` with your script's filename.

## Notes / Known Limitations

- Crop images are referenced using local Windows file paths (`C:\Users\user\Downloads\...`). These paths must exist on the machine running the app, or the image won't display. For portability, consider moving images into a project folder (e.g. `images/rice.jpeg`) and using relative paths instead.
- Crop matching is based on fixed `if-elif` range checks, so overlapping ranges will always return the first matching crop in the list order.
