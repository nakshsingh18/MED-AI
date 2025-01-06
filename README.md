# MEDAI- AI-Driven Healthcare Assistance Platform

MedAi is a comprehensive AI-driven platform designed to enhance healthcare access through a **medical chatbot**, **symptom checker**, and **hospital location finder**. The platform aims to provide immediate healthcare assistance, reducing unnecessary clinic visits and helping individuals find the nearest medical facilities using simple and accessible web tools.

## Features

- **Medical Chatbot**: Provides real-time responses to general health-related queries and offers immediate first aid advice based on the injury type. It also provides mental health support and helpline details.
- **Symptom Checker**: Allows users to input their symptoms and get a list of possible diseases along with their details, symptoms, and suggested treatments.
- **Hospital Finder**: Uses geolocation to find the nearest healthcare facilities based on the user's pin code, providing the location, name, and distance to the nearest hospitals.

## Technologies Used

- **Frontend**: 
  - React.js: For dynamic user interface development.
  - Streamlit: For building interactive web applications for symptom checking and hospital finding.

- **Backend**: 
  - Node.js: For managing API calls and backend logic.
  - Python (Streamlit): For the hospital locator backend.
  
- **APIs**: 
  - **WatsonX IBM API**: For chatbot integration, enabling conversational health assistance.
  - **OpenCage API**: For geolocation and reverse geocoding of user locations.
  - **Overpass API**: For querying OpenStreetMap data to find nearby hospitals based on geolocation.

## How It Works

### Medical Chatbot
The chatbot uses **WatsonX IBM API** for handling user queries. It can respond to both physical and mental health inquiries, providing actionable first aid advice based on the injury or condition. It is designed to assist users with immediate health concerns and offer the first step toward relief.

## Symptom Checker
Users input their symptoms, and the system compares the input to a dataset of known diseases. The top five potential diseases are shown along with their descriptions, symptoms, and treatment suggestions. The data for symptom checking is sourced from trusted medical websites like NIH, WHO, and the National Library of Medicine.

- **Dataset**: Includes diseases, symptoms, descriptions, and treatment plans.
- **Technology**: Uses Streamlit for the user interface and fuzzy string matching to compare symptoms.

## Hospital Finder
The hospital finder helps users locate nearby hospitals by entering their pin code. It uses the **OpenCage API** for geocoding and the **Overpass API** to query OpenStreetMap data for hospitals within a specified radius.

### Process:
1. Input the pin code.
2. The system retrieves the latitude and longitude of the user's location.
3. It queries the Overpass API to find hospitals within a 10 km radius.
4. The hospitals are sorted by proximity and displayed with their names, addresses, and distances.

## Installation

### Prerequisites
Ensure you have the following installed:

- **Node.js** (for the backend and frontend)
- **npm** (Node package manager)
- **Python** (for the hospital finder functionality)
- **Streamlit** (for frontend interactions)

### Install Dependencies
Clone the repository and install the necessary dependencies for both frontend and backend:

    ```bash
    git clone https://github.com/your-username/MedAi.git
    cd MedAi
    npm install # Install frontend dependencies
    pip install -r requirements.txt # Install backend dependencies

## Start the Application

To start the frontend, run the following command:
    
    ```bash
    npm start
To start the backend services (hospital finder), run:

    ```bash
    streamlit run app.py

Now, open your browser and navigate to http://localhost:3000 to access the application.

# License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements
- IBM WatsonX for chatbot integration.
- OpenCage API for geolocation.
- Overpass API for OpenStreetMap data access.

## Future Improvements
- Integration with more medical datasets for better disease prediction.
- Multilingual support for global accessibility.
- Mobile application version for easier access on smartphones.
