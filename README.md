# Lam_Naturals

Here's a detailed README file describing the entire project, including setup instructions, project structure, and deployment processes.

---

# Lam Naturals

## Overview

Lam Naturals is an agribusiness specializing in dried fruits and vegetables, targeting both local and international markets. This project aims to create a web application to showcase Lam Naturals' products and facilitate easy purchasing through an automated form. The web application consists of a frontend built with React and a backend built with Node.js and Express, with Airtable as the centralized database.

## Table of Contents

1. [Project Structure](#project-structure)
2. [Features](#features)
3. [Setup Instructions](#setup-instructions)
4. [Deployment](#deployment)
5. [Contributing](#contributing)
6. [License](#license)

## Project Structure

```
lam-naturals/
│
├── backend/
│   ├── src/
│   │   ├── config/
│   │   │   ├── dbConfig.js
│   │   │   ├── airtableConfig.js
│   │   │   └── index.js (aggregates all configurations)
│   │   ├── controllers/
│   │   │   ├── productController.js
│   │   │   ├── orderController.js
│   │   │   └── index.js (aggregates all controllers)
│   │   ├── models/
│   │   │   ├── productModel.js
│   │   │   ├── orderModel.js
│   │   │   └── index.js (aggregates all models)
│   │   ├── routes/
│   │   │   ├── productRoutes.js
│   │   │   ├── orderRoutes.js
│   │   │   └── index.js (aggregates all routes)
│   │   ├── services/
│   │   │   ├── productService.js
│   │   │   ├── orderService.js
│   │   │   └── index.js (aggregates all services)
│   │   ├── middlewares/
│   │   │   ├── authMiddleware.js
│   │   │   ├── errorHandler.js
│   │   │   └── index.js (aggregates all middlewares)
│   │   ├── utils/
│   │   │   ├── logger.js
│   │   │   ├── constants.js
│   │   │   └── helpers.js
│   │   ├── app.js
│   │   └── server.js
│   ├── .env
│   ├── .gitignore
│   ├── package.json
│   ├── package-lock.json
│   ├── README.md
│   └── ... (other root-level files)
│
├── frontend/
│   ├── public/
│   │   ├── index.html
│   │   └── ... (other public files)
│   ├── src/
│   │   ├── assets/
│   │   │   ├── images/
│   │   │   └── ... (other assets)
│   │   ├── components/
│   │   │   ├── Header.js
│   │   │   └── ... (other components)
│   │   ├── pages/
│   │   │   ├── HomePage.js
│   │   │   └── ... (other pages)
│   │   ├── services/
│   │   │   ├── apiService.js
│   │   │   └── ... (other service files)
│   │   ├── utils/
│   │   │   └── ... (utility files)
│   │   ├── App.js
│   │   ├── index.js
│   │   └── ... (other root-level files)
│   ├── .env
│   ├── .gitignore
│   ├── package.json
│   ├── package-lock.json
│   ├── README.md
│   └── ... (other root-level files)
│
├── .gitignore
├── README.md
└── ... (other project-level files)
```

## Features

- **Home Page**: Introduction to Lam Naturals and featured products.
- **Products Page**: Display all available dried fruits and vegetables.
- **Product Detail Page**: Detailed information about a specific product.
- **Shopping Cart**: Add, remove, and view products in the shopping cart.
- **Checkout**: Fill in details to purchase products.
- **Admin Dashboard**: Manage products, view orders, and monitor sales (future implementation).

## Setup Instructions

### Prerequisites

- Node.js (v14.x or later)
- npm (v6.x or later)
- Git
- Airtable API key

### Clone the Repository

```bash
git clone https://github.com/yourusername/lam-naturals.git
cd lam-naturals
```

### Backend Setup

1. **Navigate to the backend directory**:
    ```bash
    cd backend
    ```

2. **Install backend dependencies**:
    ```bash
    npm install
    ```

3. **Create a `.env` file**:
    ```plaintext
    PORT=5000
    AIRTABLE_API_KEY=your_airtable_api_key
    AIRTABLE_BASE_ID=your_airtable_base_id
    ```
4. **Run the backend server**:
    ```bash
    npm start
    ```

### Frontend Setup

1. **Navigate to the frontend directory**:
    ```bash
    cd ../frontend
    ```

2. **Install frontend dependencies**:
    ```bash
    npm install
    ```

3. **Create a `.env` file**:
    ```
    REACT_APP_BACKEND_URL=http://localhost:5000
    ```

4. **Run the frontend development server**:
    ```bash
    npm start
    ```

## Deployment

### Frontend Deployment (Netlify)

1. **Build the frontend**:
    ```bash
    npm run build
    ```

2. **Deploy to Netlify**:
    - Log in to Netlify and create a new site.
    - Link your GitHub repository and select the `frontend` directory.
    - Configure the build settings:
        - **Build Command**: `npm run build`
        - **Publish Directory**: `frontend/build`

### Backend Deployment (Hosting Platform)

1. **Choose a Hosting Platform**: (e.g., Heroku, AWS, DigitalOcean)
2. **Deploy to Heroku**:
    - Log in to Heroku and create a new app.
    - Link your GitHub repository or use Heroku CLI.
    - Set up environment variables on Heroku.
    - Deploy the backend by pushing to the repository.

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a new Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
