# Expense Tracker (with Signup + Login)
A simple expense tracker built with React (Vite), React Router, HTML, CSS and JavaScript.

## Run it
    npm install
    npm run dev
Open the URL shown in the terminal (usually http://localhost:5173).

## How to use
1. Click "Create an account" and sign up (name, email, password).
2. You are sent to the Login page - login with the same email + password.
3. Add income / expenses, filter them, delete them.
4. Logout, then signup another user - each user has their own data.

## Features
- Signup page (new members register)
- Login page
- Protected dashboard (needs login)
- Add / delete income and expenses
- Total income, expense, balance
- Filter: All / Income / Expense
- Data saved in the browser's localStorage

## Structure
    src/
      assets/                     images
      components/
        common/Button.jsx         reusable button
        layout/Navbar.jsx         top bar + logout
      context/AuthContext.jsx     who is logged in
      features/expenses/
        Summary.jsx               income / expense / balance boxes
        ExpenseForm.jsx           add form
        ExpenseList.jsx           list + delete
      pages/
        LoginPage.jsx
        SignupPage.jsx
        DashboardPage.jsx
        UnauthorizedPage.jsx
      routes/
        AppRoutes.jsx             URL -> page
        ProtectedRoute.jsx        blocks page if not logged in
      services/
        authService.js            signup + login logic
        expenseService.js         save / load expenses per user
      App.jsx
      main.jsx
      index.css

## Note
Passwords are stored as plain text in localStorage because this is a
learning project. A real app needs a backend and password hashing.
