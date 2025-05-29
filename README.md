
# PriceHeram.com

A **Django-based e-commerce price comparison web application** that allows users to search for products and compare prices across multiple marketplaces in real time.

---

## 🎯 Features

* 🔍 **Product Search**: Enter a product name or keyword to fetch matching items.
* 🛒 **Multi-Marketplace Comparison**: View prices for the same item from different online stores.
* 📊 **Discount & Offer Insights**: See available discounts and special offers side by side.
* ⚙️ **Admin Panel**: Manage products, marketplaces, and view usage statistics.
* 🔗 **Modular Scraping**: Easily add or update web scrapers for new marketplaces.

---

## 🚀 Tech Stack

* **Backend**: Django 4.x
* **Frontend**: HTML5, CSS3, JavaScript
* **Database**: SQLite (default) / PostgreSQL (recommended for production)
* **Web Scraping**: Selenium (via `chromedriver.exe`)
* **Dependencies**: See [`requirements.txt`](requirements.txt)

---

## 📥 Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/nishan2582/PriceHeram.com.git
   cd PriceHeram.com
   ```

2. **Create a virtual environment** (Python 3.8+)

   ```bash
   python -m venv venv
   source venv/bin/activate    # Linux / macOS
   venv\Scripts\activate     # Windows
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Set up database**

   ```bash
   python manage.py migrate
   ```

5. **Download ChromeDriver**

   * Place your `chromedriver.exe` in the project root (already included) or update `settings.py` with its path.

6. **Run the development server**

   ```bash
   python manage.py runserver
   ```

7. **Access the app**

   Open your browser at `http://127.0.0.1:8000/` and start searching!

---

## 🗂️ Project Structure

```plaintext
PriceHeram.com/
├── DjPriceCompare/        # Django project settings
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── myapp/                 # Core application
│   ├── migrations/
│   ├── templates/
│   ├── static/
│   ├── views.py
│   ├── models.py
│   ├── urls.py
│   └── ...
├── media/                 # Scraped images / assets
├── db.sqlite3             # Default SQLite database
├── chromedriver.exe       # Selenium WebDriver binary
├── manage.py
├── requirements.txt
└── README.md
```

---

## ⚙️ Usage

1. **Run a product search**

   * Enter a keyword in the search bar and hit **Search**.

2. **View Comparison Results**

   * Results page displays a table of product titles, prices, and direct links to each marketplace.

3. **Inspect Discounts**

   * Any available discounts or coupons are highlighted.

---

## 🛠️ Customization

* **Add New Marketplace**:

  1. Create a new scraper module in `myapp/scrapers/`.
  2. Implement `fetch_products(query)` that returns a list of items.
  3. Register it in `settings.py` under `MARKETPLACE_SCRAPERS`.
* **Switch to PostgreSQL**:

  1. Install `psycopg2-binary`.
  2. Update `DATABASES` in `settings.py`.

---

## 📈 Future Roadmap

* 📱 Responsive UI with React/Vue frontend
* ⚡ Caching & rate-limiting for faster responses
* 🔐 User authentication & favorites
* ☁️ Docker containerization

---

## 🤝 Contributing

1. Fork the repo
2. Create a new branch (`git checkout -b feature/YourFeature`)
3. Commit your changes
4. Push to your fork
5. Open a Pull Request

Please follow [PEP8](https://www.python.org/dev/peps/pep-0008/) style guidelines.

---



---

## 📬 Contact

* **GitHub**: [nishan2582](https://github.com/nishan2582)
* **Email**: [baniya.parbesh@gmail.com](mailto:baniya.parbesh@gmail.com)

Feel free to reach out with questions, feedback, or collaboration ideas!
