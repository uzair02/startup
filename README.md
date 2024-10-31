# Sentimantle

EMPOWER YOUR DECISIONS WITH EMOTIONAL INSIGHTS. ADVANCED SENTIMENT ANALYSIS FOR BUSINESS INTELLIGENCE. YOUR PARTNER IN EMOTIONAL DATA ANALYTICS.

---

## Table of Contents

1. [Introduction](#introduction)
2. [Technology Stack](#technology-stack)
3. [Prerequisites](#prerequisites)
4. [Folder Structure](#folder-structure)
5. [Environment Variables](#environment-variables)
6. [Installation](#installation)
   - [Local Development Setup](#local-development-setup)
   - [Dockerized Setup](#dockerized-setup)
7. [Usage](#usage)
8. [Development URLs](#development-urls)
9. [Contributing](#contributing)

---

## Introduction

At Sentimantle, we understand the profound impact emotions have on decision-making. As your dedicated partner in sentiment analysis, we help you navigate the intricate landscape of customer opinions and market trends. Our innovative approach employs proprietary algorithms to monitor and interpret emotional cues from vast data sources, ensuring you're always informed.

Our unique service distills complex data from Google Maps, Tripadvisor, Booking.com reviews, and other option to add the data through manual channels to generate easy-to-understand report, delivered weekly to your preferred emails. Our solutions are customized to provide actionable insights at a cost-effective price.

Stay tuned as we unveil the future of emotional intelligence in business, where staying attuned to sentiment is effortless, and data-driven decisions are guaranteed.

---

## Technology Stack

- **Backend**: Flask
- **Frontend**: ReactJS
- **Database**: MySQL
- **Sentry**: Error Monitoring
- **Deployment Dev**: Fly.io
- **Deployment Staging**: Azure
- **Emails**: Postmark
- **Project Management**: [Clickup](https://app.clickup.com/9009176125/v/l/8cfu7hx-2560)

---

## Prerequisites

To run the project, you will need the following:

- Node.js 18.17.0 or above
- npm
- Docker
- Postman (for testing API endpoints)

---

## Folder Structure

This is the project’s folder structure, which will help developers quickly locate essential files and directories:

**Root Directory: `FE_SENTIMANTLE/`**

- **Source Directory (`src/`)**  
  Contains the main application source code, React components, and logic.

  - **Core Application Files**
    - `App.js` - Main application component
    - `App.css` - Main application styles
    - `index.js` - Application entry point
    - `index.css` - Global styles
    - `AProtectedRoute.js`, `UProtectedRoute.js` - Protected route components
    - `DateRangePicker.js` - Date selection component
    - `Regex.js` - Regular expressions utilities
    - `reportWebVitals.js` - Performance monitoring
    - `setupTests.js` - Test setup
    - `TextObjects.jsx` - Text components
    - `TotalServices.jsx` - Services overview component
    - `axios.jsx` - API setup (using Axios)

  - **Major Directories**
    - `assets/` - Static assets (images, fonts)
    - `components/`
      - `AdminDashboard/` - Admin interface components
      - `ApiServices/` - API services
      - `Input/` - Reusable input components
      - `Loader/` - Loading indicators
      - `ModalContent/` - Modal components
      - `NoDataFound/` - Empty state indicators
      - `Pagination/` and `ReactPagination/` - Pagination components
      - `Search/` - Search component
      - `TableComponent/` - Reusable table components
      - `UserDashboard/` - User components
      - `Utils/` - Utility functions
      - `Wrapper/` - Layout wrappers

    - `config/`
      - `config.js` - App configuration

    - `pages/`
      - `AdminDashboard/` - Admin pages
      - `ErrorPages/` - Error pages
      - `UserDashboard/` - User pages

- **Configuration Files**
  - `.dockerignore`, `.env`, `.gitignore`
  - `Dockerfile`, `fly.dev.toml`, `fly.staging.toml`
  - `nginx.conf` - Nginx server config
  - `package-lock.json`, `package.json`
  - `postman-collection.json` - API testing collection
  - `README.md` - Documentation

---

## Environment Variables

Environment variables required for the project:

- **Development URL**: `REACT_APP_API_URL=https://dev-be-sentimantle.fly.dev`
- **Staging URL**: `REACT_APP_API_URL=https://staging-sentimnatle-api.ambitiousmoss-885b98c6.centralus.azurecontainerapps.io`

---

### Installation

Follow this step-by-step guide to install and set up the project. You can use either the **Local Development Setup** or the **Dockerized Setup**.

---

### Local Development Setup

1. **Clone the repository**:

   ```sh
   git clone https://github.com/Codeaza-A-Creative-Agency/FE_sentimantle.git
   cd FE_sentimantle
   ```

2. **Install dependencies**:

   ```sh
   npm install
   ```

   - If the above command doesn’t work, try:
     ```sh
     npm install --force
     ```

3. **Start the development server**:

   ```sh
   npm start
   ```

---

### Dockerized Setup

1. **Clone the repository** (if not already done):

   ```sh
   git clone https://github.com/Codeaza-A-Creative-Agency/FE_sentimantle.git
   cd FE_sentimantle
   ```

2. **Create a `.env` file** in the project root:
   - Add the necessary environment variables as specified in the project requirements.

3. **Build the Docker image**:
   - **For Windows PowerShell**:
     ```powershell
     docker build --build-arg (Get-Content test.env | ForEach-Object { $_ -replace '^([^=]+)=(.*)$', '$1=$2' }) -t dev-fe-sentimantle .
     ```
   - **For Ubuntu/Linux**:
     ```sh
     docker build --build-arg $(cat test.env | xargs) -t dev-fe-sentimantle .
     ```

4. **Run the Docker container**:

   ```sh
   docker run -p 3000:80 dev-fe-sentimantle
   ```

---

## Usage

*[Provide examples and instructions on using the application here]*

---

## Development URLs

- **Dev Environment Admin**: [Link](https://dev-fe-sentimantle.fly.dev/admin-dashboard)
- **Dev Environment User**: [Link](https://dev-fe-sentimantle.fly.dev/user-dashboard)
- **Staging Environment Admin**: [Link](https://staging-sentimantle-frontend.ambitiousmoss-885b98c6.centralus.azurecontainerapps.io/admin-dashboard)
- **Staging Environment User**: [Link](https://staging-sentimantle-frontend.ambitiousmoss-885b98c6.centralus.azurecontainerapps.io/user-dashboard)

---

## Development

Details about the development, staging, and production environments.

### Development URL

- [Dev Environment Admin](https://dev-fe-sentimantle.fly.dev/admin-dashboard)
- [Dev Environment User](https://dev-fe-sentimantle.fly.dev/user-dashboard)

### Staging URL

- [Staging Environment Admin](https://staging-sentimantle-frontend.ambitiousmoss-885b98c6.centralus.azurecontainerapps.io/admin-dashboard)
- [Staging Environment User](https://staging-sentimantle-frontend.ambitiousmoss-885b98c6.centralus.azurecontainerapps.io/user-dashboard)

### Production URL

Coming soon

---

## Contributing

To contribute:

- Fork the repository
- Create a new branch (`git checkout -b feature/AmazingFeature`)
- Commit your changes (`git commit -m 'Add some AmazingFeature'`)
- Push to the branch (`git push origin feature/AmazingFeature`)
- Open a pull request


---
