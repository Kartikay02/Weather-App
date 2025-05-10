# Weather App 0.1
# DEMO (https://kartikay02.github.io/Weather-App/)
A dynamic weather application that provides users with up-to-date weather information. It allows users to get weather data for their current location (via browser geolocation) or search for weather conditions in any city worldwide. The app utilizes the OpenWeatherMap API to fetch real-time data such as temperature, humidity, wind speed, cloudiness, and more.
## 🚀 Features

*   **Tabbed Interface:** Easily switch between "Your Weather" (geolocation-based) and "Search Weather" (city-based).
*   **Geolocation Weather:**
    *   Prompts for location access on the "Your Weather" tab.
    *   Displays weather for the user's current geographical location.
    *   Caches location coordinates in session storage for quicker access during the same session.
*   **City Search Weather:**
    *   Allows users to search for weather by city name on the "Search Weather" tab.
*   **Detailed Weather Information Displayed:**
    *   City Name
    *   Country Flag (using Flagpedia API)
    *   Current Weather Description (e.g., "clear sky", "light rain")
    *   Weather Icon representing current conditions
    *   Temperature (in Celsius)
    *   Wind Speed (in m/s)
    *   Humidity (percentage)
    *   Cloudiness (percentage)
*   **Loading State:** Visual "loading" indicator while fetching data from the API.
*   **User-Friendly Interface:** Clean and intuitive design with clear visual cues.

## 🛠️ Technologies Used

*   **Frontend:**
    *   HTML5
    *   CSS3 (including custom properties, Flexbox)
    *   JavaScript (ES6+ with `async/await` for API calls)
*   **APIs:**
    *   **OpenWeatherMap API:** For fetching weather data.
    *   **Flagpedia API (`flagcdn.com`):** For displaying country flags.
    *   **Browser Geolocation API:** For retrieving user's current location.
*   **Storage:**
    *   Browser `sessionStorage`: To store user's coordinates for the "Your Weather" tab.

## ⚙️ Setup and Installation

1.  **Clone the repository (or download the files):**
    ```bash
    git clone <your-repository-url>
    cd weather-app-0.1
    ```
    (If you don't have a Git repository yet, simply ensure `index.html`, `styles.css`, and `index.js` are in the same folder.)

2.  **Get an API Key from OpenWeatherMap:**
    *   Go to [OpenWeatherMap](https://openweathermap.org/appid) and sign up for a free account.
    *   Navigate to the API keys section on your account page and generate/copy your API key.

3.  **Update API Key in `index.js`:**
    *   Open the `index.js` file.
    *   Find the line:
        ```javascript
        const API_KEY = "d1845658f92b31c64bd94f06f7188c9c";
        ```
    *   Replace `"d1845658f92b31c64bd94f06f7188c9c"` with **your actual OpenWeatherMap API key**.

4.  **Open in Browser:**
    *   Open the `index.html` file in your preferred web browser.
    *   **Note on Geolocation:** For the "Your Weather" (geolocation) feature to work correctly, you might need to serve the files through a local web server (e.g., using VS Code's "Live Server" extension, Python's `http.server`, or `npx serve`). Some browsers restrict geolocation features on pages loaded directly from the local file system (`file:///...`).

## 📖 How to Use

1.  **Your Weather Tab:**
    *   Upon loading, the application defaults to the "Your Weather" tab.
    *   If you haven't granted location access before (or if coordinates aren't in session storage), you'll see a "Grant Location Access" screen.
    *   Click the "Grant Access" button. Your browser will prompt you for permission to access your location. Allow it.
    *   The app will then fetch and display the weather for your current location.
    *   Your location coordinates are saved in session storage. If you switch tabs and come back, or refresh the page (within the same browser session), it will try to use these stored coordinates.

2.  **Search Weather Tab:**
    *   Click on the "Search Weather" tab.
    *   An input field will appear. Type the name of the city for which you want to find the weather (e.g., "London", "Tokyo").
    *   Press the `Enter` key or click the search icon button.
    *   The app will fetch and display the weather information for the searched city.

## 📁 Project Structure


weather-app-0.1/
├── index.html # Main HTML structure of the application
├── styles.css # CSS styles for the application
├── index.js # JavaScript logic, API calls, and DOM manipulation
└── README.md # This file

## 📝 To-Do / Potential Improvements

*   **Error Handling:**
    *   Display user-friendly messages for API errors (e.g., city not found, invalid API key, network issues). The current `catch` blocks are placeholders (`//HW`).
    *   Handle cases where geolocation is denied by the user or not supported by the browser (the `else` block in `getLocation()` is a placeholder `//HW - show an alert for no gelolocation support available`).
*   **UI/UX Enhancements:**
    *   Add animations for tab transitions or weather card appearance.
    *   Implement more detailed forecast data (e.g., hourly or 5-day forecast).
    *   Option to switch temperature units (e.g., Celsius to Fahrenheit).
*   **Accessibility (a11y):**
    *   Ensure proper ARIA attributes for interactive elements.
    *   Verify keyboard navigability.
*   **Code Refinements:**
    *   Further modularize JavaScript functions if the codebase grows.
    *   Add comments to more complex parts of the code.
*   **Testing:** Implement basic unit or integration tests.

## 📄 License

(Specify a license if you have one, e.g., MIT License. If not, you can omit this section or state "This project is unlicensed.")

---


content_copy
download
Use code with caution.
IGNORE_WHEN_COPYING_END
