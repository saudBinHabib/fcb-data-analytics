# FC Bayern Analytics Dashboard

A comprehensive analytics system for processing and visualizing FC Bayern Munich match data, featuring player performance metrics and team statistics.

## 📊 Features

### Player Performance Analysis

- Pass metrics (total, success rate, key passes, etc.)
- Shooting statistics
- Aerial duel performance
- Interactive radar charts for player comparison

### Data Processing

- Custom Python package for match data processing
- Efficient event data extraction
- Real-time metric calculations

### Interactive Dashboard

- Player comparison views
- Team performance analytics
- Historical trend analysis
- Customizable visualizations

## 🛠 Tech Stack

### Backend

- Python 3.11+
- PostgreSQL
- SQLAlchemy
- FastAPI

### Frontend

- Streamlit
- Plotly

### Development

- Poetry (dependency management)
- Docker & Docker Compose
- pytest (testing)
- Black & isort (code formatting)

## 🚀 Quick Start

### Prerequisites

- Python 3.11 or higher
- Docker and Docker Compose
- Poetry (Python package manager)
- PostgreSQL (if running locally)

### Installation

1. Clone the repository

   `git clone https://github.com/your-username/fcbayern-analytics.git`
   `cd fcbayern-analytics`

2. Set up environment variables

   `poetry env use python3`

3. Install dependencies

   `Install Poetry if you haven't already`
   `curl -sSL https://install.python-poetry.org | python3 -`
   Install project dependencies
   `poetry install`

4. Initialize the database

Using Docker
`docker-compose up -d db`

Run database initialization
`poetry run python scripts/init_db.py`

5. Load sample data

   `poetry run python scripts/load_data.py`

6. Start the application

Using Docker Compose
`docker-compose up`

Visit http://localhost:8501 to access the dashboard.

## 📁 Project Structure

fcb_data_analytics/
├── fcb_data_analytics/ # Core analysis package
│ ├── data/ # Data loading and processing
│ ├── metrics/ # Metric calculations
│ └── utils/ # Utility functions
├── dashboard/ # Streamlit application
│ ├── components/ # Reusable UI components
│ └── pages/ # Dashboard pages
├── tests/ # Test suite
├── scripts/ # Utility scripts
└── docker/ # Docker configuration

## 🧪 Development

Setting up Development Environment

1. Install development dependencies

   `poetry install --with dev`

2. Set up pre-commit hooks

   `poetry run pre-commit install`

3. Running Tests

   Run all tests
   `poetry run pytest`
   Run specific test file
   poetry run pytest tests/test_metrics/test_passing.py

4. Code Quality

   Format code
   `poetry run black .`
   `poetry run isort .`

5. Building Documentation

   Generate documentation
   `poetry run sphinx-build docs/source docs/build`

6. 🐳 Docker

   #### Building and Running

   i. Build images
   `docker-compose build`

   ii. Start services
   `docker-compose up -d`

   iii. View logs
   `docker-compose logs -f`

   iv. Stop services
   `docker-compose down`

#### Development with Docker

    i. Run tests in container
        `docker-compose run --rm app pytest`

    ii. Access database
        `docker-compose exec db psql -U fcbayern -d analytics`

📊 Data Schema

## 🔄 CI/CD Pipeline

The project uses GitHub Actions for continuous integration and deployment:

- Automated testing
- Code quality checks
- Docker image builds
- Deployment to staging/production

## 📝 Contributing

- Fork the repository
- Create a feature branch (git checkout -b feature/amazing-feature)
- Commit your changes (git commit -m 'Add amazing feature')
- Push to the branch (git push origin feature/amazing-feature)
- Open a Pull Request

### Commit Guidelines

    We follow the Conventional Commits specification:

    - feat: New features
    - fix: Bug fixes
    - docs: Documentation changes
    - style: Code style changes
    - refactor: Code refactoring
    - test: Adding or modifying tests
    - chore: Maintenance tasks

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 📧 Contact

    For questions and support, please contact:

    Project Maintainer: Saud Bin Habib
    Technical Support: saud.bin.habib@outlook.com

Made with ⚽️ for FC Bayern Munich
