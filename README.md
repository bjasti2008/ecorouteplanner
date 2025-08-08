Eco Route Planner 
Welcome to the Eco Route Planner! This web application helps you plan your journeys by comparing different transportation modes based on their estimated CO₂ emissions, time, and cost. Make greener travel choices and contribute to a more sustainable future.

Features
Advanced Geocoding & Autocomplete: Easily find start, end, and waypoint locations with intelligent address suggestions powered by Geoapify.
Reverse Geocoding on Map Clicks: Click anywhere on the map to instantly get a human-readable address for that location.
Multi-Modal Routing: Compare routes for driving (Gasoline, Hybrid, Electric), biking, walking, and public transit.
Real-time Traffic (Simulated/API-dependent): Input your preferred departure time to get route estimates that can account for traffic patterns (requires Geoapify API plan with traffic data).
Nuanced Eco-Calculations:
Vehicle-specific CO₂ emissions and fuel costs based on selected vehicle type (Gasoline, Hybrid, Electric).
Estimated electricity grid emissions for EV mode.
Fuel prices fetched from a real-time API (CollectAPI) based on your starting location.
Interactive Route Details: Expand sections to view step-by-step directions for each route.
Route Polyline Highlighting: Hover over a route card to highlight its path on the map, making comparisons intuitive.
Saved Routes: Save your favorite or frequently used routes directly in your browser's local storage.
Route Customization: Choose to avoid tolls and highways for driving routes.
Comparative Visualizations: See a clear bar chart comparing time, cost, and CO₂ for all calculated routes.
Carbon Savings Calculator: Quantify your positive environmental impact by showing CO₂ savings and their equivalent in "trees planted."
Weather Impact: Get current weather conditions for your starting location with basic warnings for walking/biking in adverse weather.
Responsive Design: Enjoy a seamless experience on both desktop and mobile devices.

Getting Started
This project is designed as a single HTML file for simplicity, leveraging CDN links for React, Leaflet, Tailwind CSS, and external APIs.
Prerequisites
To run this application and utilize its full features, you will need API keys for the following services:
Geoapify: For geocoding (address search, reverse geocoding, autocomplete) and routing.
Get your API key here: https://www.geoapify.com/
CollectAPI (Gas Price): For fetching real-time fuel prices.
Get your API key here: https://collectapi.com/
(Note: Open-Meteo for weather data does not require an API key.)

Installation
Clone the repository:
git clone https://github.com/bjasti2006/ecorouteplanner.git
cd ecorouteplanner

Open index.html:
Open the index.html file in your preferred web browser. You can simply double-click it, or serve it using a local HTTP server (recommended for better browser security and API access, e.g., using Python: python -m http.server in the directory, then navigate to http://localhost:8000).

Insert Your API Keys:
Open index.html in a text editor. Locate the // --- API Keys --- section within the <script type="text/babel"> block. Replace the placeholder values with your actual API keys. If you've already inserted your keys, please ensure they are valid and correctly placed.

// IMPORTANT: Using Geoapify API key for geocoding and routing
const GEOAPIFY_API_KEY = 'YOUR_GEOAPIFY_API_KEY_HERE';
// Fuel Price API Key (e.g., from CollectAPI)
const FUEL_PRICE_API_KEY = 'YOUR_COLLECTAPI_KEY_HERE';

Usage
Set Locations:
Type your "Start Location" and "End Location" into the input fields. Autocomplete suggestions will appear as you type.
Alternatively, click directly on the map to set your start, end, and subsequent waypoint locations.
Add Waypoints (Optional): Click "+ Add Waypoint" to include intermediate stops on your journey.
Select Vehicle Type: Choose between Gasoline, Hybrid, or Electric for driving calculations.
Enable EV Mode: Check the "Enable EV Mode" box if you want to consider your hybrid/PHEV car running purely on electricity for a segment, or for a pure EV.
Set Departure Time: Input a preferred departure time for more accurate (traffic-aware) routing estimates.
Route Preferences: Check "Avoid Tolls" or "Avoid Highways" if desired.
Compare Routes: Click the "Compare Routes" button to see the estimated time, cost, CO₂, and eco points for each transportation mode.
View Details: Click "Show Details" on any route card to see step-by-step directions and weather impact.
Save/Load Favorites: Use the "Save Route" button to store your current route, and load previously saved routes from the "Favorite Routes" section.
Use Current Location: Click "Use My Current Location" to automatically set your starting point.

Technologies Used
React: For building the user interface.
Leaflet.js: An open-source JavaScript library for interactive maps.
Tailwind CSS: A utility-first CSS framework for rapid styling.
Geoapify API: For geocoding (search, autocomplete, reverse) and routing.
CollectAPI: For fetching real-time fuel prices.
Open-Meteo API: For current weather data.
Babel Standalone: For transpiling JSX directly in the browser.

Contributing
Contributions are welcome! If you have ideas for new features, improvements, or bug fixes, please feel free to:
Fork the repository.
Create a new branch (git checkout -b feature/your-feature-name).
Make your changes.
Commit your changes (git commit -m 'Add new feature').
Push to the branch (git push origin feature/your-feature-name).
Open a Pull Request.

License
This project is open-source and available under the MIT License.
