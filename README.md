![image](https://github.com/user-attachments/assets/3921958c-776a-471a-82cf-b00295301113)# EcoLens

**EcoLens** is a sustainability analysis tool that allows users to scan a product barcode and get detailed sustainability scores based on various environmental and social parameters. It utilizes a barcode lookup API, web scraping, and Google's generative AI to gather and assess product sustainability information.

## Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Environment Variables](#environment-variables)
- [Project Structure](#project-structure)
- [Contributing](#contributing)

  


## Watch the Loom Video
[![Watch the Video](![image](https://github.com/user-attachments/assets/bacdd70e-a534-48ea-b698-07c2809200b5)
)(https://www.loom.com/share/739baac2854d4dec84f857893820a5d9?sid=a5791a9d-4a97-4445-9140-412e2b0df07d)]

## Features
- Barcode scanning and product lookup.
- Web scraping for additional product and brand information.
- Google generative AI integration to generate sustainability scores.
- Detailed breakdown of sustainability metrics including materials, energy usage, waste management, and more.

## Technologies Used
- **Frontend**: React, React Markdown
- **Backend**: Node.js, Express
- **APIs**: Barcode Lookup API, Google Generative AI
- **Web Scraping**: Puppeteer
- **Other**: Axios, CORS

## Installation

### Prerequisites
Make sure you have the following installed on your machine:
- Node.js (v14+)
- npm (v6+)

### Clone the repository
```bash
git clone https://github.com/s-sweta/EcoLens.git
cd EcoLens
```

### Setup environment variables
Create a `.env` file in the root directory and add the following variables:
```env
FRONTEND_URL=http://localhost:3000
PORT=5000
BARCODE_LOOKUP_API_KEY=<your-barcode-lookup-api-key>
API_KEY=<your-google-generative-ai-api-key>
```

### Run the app
1. **Backend:**
   ```bash
   cd backend
   npm install
   node index.js
   ```
   This will start the backend server on `http://localhost:5000`.

2. **Frontend:**
   Open a new terminal and run:
   ```bash
   cd frontend
   npm install
   npm start
   ```
   The React app will run on `http://localhost:3000`.

## Usage
1. Enter a product barcode in the input field and submit.
2. The backend will fetch product details via the Barcode Lookup API and scrape additional data using Puppeteer.
3. The Google generative AI will then assess the product’s sustainability across various parameters and provide a score.
4. The results, including the score and breakdown, will be displayed on the frontend.

### Example Workflow
- Enter barcode `8901138836122` for a product.
- The app will return sustainability metrics such as **Materials**, **Energy Usage**, **Waste Management**, **Social Responsibility**, and **Economic Impact**.

## Environment Variables
- **FRONTEND_URL**: The URL of your frontend application.
- **PORT**: The port for running the backend.
- **MONGO_URI**: MongoDB connection string (optional, if you're using MongoDB).
- **BARCODE_LOOKUP_API_KEY**: API key for Barcode Lookup.
- **GOOGLE_GEMINI_API_KEY**: API key for Google generative AI.

## Project Structure
```plaintext
EcoLens/
│
├── backend/                      # Backend code
│   ├── index.js                  # Express server entry point
│   └── ...                       # Other backend files (routes, utils)
│
├── frontend/                     # Frontend React application
│   ├── src/
│   │   ├── components/           # React components
│   │   ├── App.js                # Main app component
│   │   └── ...                   # Other frontend files
│   └── ...                       # Other frontend configs (package.json, etc.)
│
├── .env                          # Environment variables (shouldn't be shared)
├── package.json                  # Project dependencies
└── README.md                     # This file
```

## Contributing
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add new feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Open a pull request.

