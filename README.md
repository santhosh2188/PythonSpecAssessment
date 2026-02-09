# 💰 Expense Tracker

A simple, elegant expense tracking application built with Flask. Track your spending, categorize expenses, and stay on budget.

## Features

- ✅ Add, view, and delete expenses
- 📊 Filter expenses by category
- 💵 Real-time total calculation
- 📱 Responsive design
- 🔌 REST API endpoints
- ✨ Clean, modern UI
- 🧪 Comprehensive test suite

## Project Structure

```
expense-tracker/
├── app.py                  # Main Flask application
├── test_app.py             # Pytest test suite
├── requirements.txt        # Python dependencies
├── templates/
│   └── index.html         # Main HTML template
├── static/
│   └── css/
│       └── style.css      # CSS styles
└── README.md              # This file
```

## Requirements

- Python 3.8 or higher
- pip (Python package manager)

## Installation

1. **Clone or download this repository**

2. **Navigate to the project directory**
   ```bash
   cd expense-tracker
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

## Running the Application

1. **Start the Flask development server**
   ```bash
   python app.py
   ```

2. **Open your browser and visit**
   ```
   http://localhost:5000
   ```

3. **Start tracking your expenses!**

## Running the Tests

The application includes a comprehensive test suite using pytest.

### Run all tests:
```bash
pytest test_app.py -v
```

### Run specific test classes:
```bash
# Test only the Expense class
pytest test_app.py::TestExpenseClass -v

# Test only the routes
pytest test_app.py::TestRoutes -v

# Test only the API
pytest test_app.py::TestAPI -v
```

### Run with coverage:
```bash
pip install pytest-cov
pytest test_app.py --cov=app --cov-report=html
```

### Expected test output:
```
test_app.py::TestExpenseClass::test_expense_creation PASSED
test_app.py::TestExpenseClass::test_expense_with_date PASSED
test_app.py::TestRoutes::test_index_route PASSED
test_app.py::TestRoutes::test_add_expense_success PASSED
...
======================== XX passed in X.XXs ========================
```

## Using the Application

### Adding an Expense

1. Fill in the amount, category, description, and date
2. Click "Add Expense"
3. Your expense will appear in the list below

### Filtering Expenses

- Use the dropdown menu to filter by category
- Select "All Categories" to view all expenses

### Deleting an Expense

- Click the "Delete" button next to any expense
- Confirm the deletion

### Clearing All Expenses

- Click "Clear All Expenses" at the bottom
- Confirm to remove all data

## API Endpoints

The application provides REST API endpoints for programmatic access:

### Get All Expenses
```bash
GET /api/expenses
```

**Response:**
```json
[
  {
    "id": 1,
    "amount": 50.00,
    "category": "Food & Dining",
    "description": "Lunch",
    "date": "2024-02-09"
  }
]
```

### Get Summary
```bash
GET /api/summary
```

**Response:**
```json
{
  "by_category": {
    "Food & Dining": 75.50,
    "Transportation": 30.00
  },
  "total": 105.50,
  "count": 3
}
```

## Categories

The application supports the following expense categories:

- 🍔 Food & Dining
- 🚗 Transportation
- 🛍️ Shopping
- 🎬 Entertainment
- 💡 Bills & Utilities
- 🏥 Healthcare
- 📦 Other

## Data Storage

Currently, the application uses **in-memory storage**. This means:

- ✅ Fast and simple
- ❌ Data is lost when the server restarts
- 💡 Future enhancement: Add SQLite or PostgreSQL for persistence

## Testing Strategy

The test suite covers:

1. **Unit Tests** - Testing the Expense class
2. **Route Tests** - Testing Flask endpoints
3. **API Tests** - Testing JSON API responses
4. **Integration Tests** - Testing complete workflows
5. **Validation Tests** - Testing input validation and error handling

### Test Coverage Includes:

- ✅ Expense creation and validation
- ✅ Adding expenses (valid and invalid inputs)
- ✅ Deleting expenses
- ✅ Filtering by category
- ✅ Total calculation
- ✅ API responses
- ✅ Error handling
- ✅ Complete user workflows

## Development Notes

### Built With

- **Flask** - Python web framework
- **pytest** - Testing framework
- **HTML/CSS** - Frontend (no JavaScript frameworks needed!)

### Code Generation Tool Used

This project was built using **Claude** (Anthropic's AI assistant) to demonstrate effective use of AI code generation tools for rapid application development.

### Key Engineering Practices

- ✅ Clean, readable code with comments
- ✅ Comprehensive test coverage
- ✅ Input validation and error handling
- ✅ RESTful API design
- ✅ Responsive UI design
- ✅ Clear documentation

## Future Enhancements

Potential improvements for the application:

- [ ] Persistent storage (SQLite/PostgreSQL)
- [ ] User authentication
- [ ] Budget setting and alerts
- [ ] Monthly/weekly summaries
- [ ] Data export (CSV, PDF)
- [ ] Charts and visualizations
- [ ] Receipt image uploads
- [ ] Recurring expense tracking

## Troubleshooting

### Port Already in Use
If port 5000 is already in use, modify `app.py`:
```python
app.run(debug=True, host='0.0.0.0', port=5001)  # Change port
```

### Module Not Found Errors
Make sure you've installed all dependencies:
```bash
pip install -r requirements.txt
```

### Tests Failing
Ensure you're in the correct directory and have pytest installed:
```bash
pip install pytest
pytest test_app.py -v
```

## License

This project is provided as-is for educational and demonstration purposes.

## Contributing

This is a demonstration project, but feel free to fork and modify for your own use!

## Contact

For questions or feedback about this project, please reach out through the repository.

---

**Happy expense tracking! 💰**
