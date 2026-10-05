# Fix_Finder
ServiceAI is an AI-powered multi-service recommendation system that helps users find the right service provider by simply describing their problem in natural language. Instead of manually selecting a service category, users can enter a query .

# 🤖 ServiceAI – AI-Powered Problem-to-Service Recommendation System

## 📌 Project Overview

**ServiceAI** is an AI-powered multi-service recommendation system that helps users find suitable service providers by simply describing their problem in natural language.

Instead of manually selecting a service category, users can type a query such as:

> "My bike is not starting and I need a mechanic near Perinthalmanna."

The system uses **Natural Language Processing (NLP)** to understand the user's request, identify the required service category and location, and recommend suitable service providers.

---

## 🎯 Objectives

* Understand user problems using NLP.
* Identify the required service category.
* Detect the location mentioned by the user.
* Find relevant service providers from the dataset.
* Rank providers based on multiple factors.
* Display the best recommendations through a simple user interface.

---

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Regular Expressions (re)**
* **Natural Language Processing (NLP)**
* **Gradio**
* **Google Colab**
* **CSV Dataset**

---

## 🧠 How the System Works

```text
User enters a problem
        ↓
NLP preprocessing
        ↓
Service category detection
        ↓
Location detection
        ↓
Find matching service providers
        ↓
Calculate recommendation score
        ↓
Rank service providers
        ↓
Display Top 5 Recommendations
```

---

## 📊 Dataset

The project uses a structured CSV dataset containing information about different service providers.

### Main Dataset Columns

| Column                | Description                     |
| --------------------- | ------------------------------- |
| `Service_ID`          | Unique service/provider ID      |
| `Service_Category`    | Main service category           |
| `Service_Name`        | Name of the service             |
| `Service_Type`        | Specific service type           |
| `Problem_Description` | Problems handled by the service |
| `Location`            | Service provider location       |
| `Distance_KM`         | Distance from the user          |
| `Rating`              | Provider rating                 |
| `Price`               | Estimated service price         |
| `Availability`        | Service availability            |
| `Experience_Years`    | Provider experience             |

### Supported Service Categories

* 🚗 Automobile
* 🔧 Plumber
* ⚡ Electrician
* ❄️ AC Technician
* 🧺 Appliance Repair
* 💻 Computer Repair

---

## 🔤 NLP Component

The NLP component processes the user's natural-language query.

For example:

```text
"My bike is not starting near Perinthalmanna"
```

The system identifies:

```text
Service Category → Automobile
Location → Perinthalmanna
```

The extracted information is then used to search the service-provider dataset.

### Current NLP Approach

The current version uses:

* Text cleaning
* Lowercase conversion
* Keyword matching
* Service-category detection
* Location detection

Future versions can use **Word2Vec, FastText, or sentence embeddings** for better semantic understanding.

---

## ⭐ Recommendation System

After identifying the required service, the system ranks available providers.

The recommendation score considers:

```text
Rating          → 35%
Distance        → 20%
Price           → 15%
Experience      → 20%
Availability    → 10%
```

Higher-rated, closer, reasonably priced, experienced, and available providers receive better recommendation scores.

---

## 🖥️ User Interface

The project uses **Gradio** to create an interactive web interface.

Users can:

1. Enter their problem.
2. Click **Find Best Service**.
3. View the detected service and location.
4. Get the top 5 recommended service providers.

Example:

```text
User:
"My AC is not cooling properly near Perinthalmanna."

AI:
Service Detected → AC Technician
Location → Perinthalmanna

Output:
Top 5 Recommended Service Providers
```

---

## 📁 Project Structure

```text
ServiceAI/
│
├── vehicle_service_dataset.csv
├── serviceai.py
├── README.md
└── requirements.txt
```

---

## ⚙️ Installation

Install the required Python libraries:

```bash
pip install pandas numpy gradio
```

---

## ▶️ Running the Project

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/ServiceAI.git
```

### 2. Open the project folder

```bash
cd ServiceAI
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the application

```bash
python serviceai.py
```

The Gradio interface will launch and provide a local web link.

---

## 💡 Example Queries

Try queries such as:

```text
My bike is not starting near Perinthalmanna.
```

```text
There is a water pipe leakage in my house.
```

```text
My AC is not cooling properly.
```

```text
I have an electrical wiring problem.
```

```text
My washing machine is not working.
```

```text
My laptop is not turning on.
```

---

## 🚀 Future Scope

The project can be improved by adding:

* 🧠 Semantic NLP using Word2Vec/FastText
* 🌐 Malayalam + English NLP
* 📍 Real-time GPS location
* 🗺️ Google Maps integration
* 📞 Contact service providers
* 📅 Online service booking
* ⭐ User reviews and ratings
* 🤖 AI chatbot
* 📱 Mobile application
* 🔐 User and service-provider accounts

---

## 🌟 Advantages

* Easy natural-language interaction
* Reduces manual searching
* Supports multiple service categories
* Provides ranked recommendations
* Simple and user-friendly interface
* Can be expanded into a real-world service marketplace

---

## 🎓 Project Type

**Domain:** Data Science / Artificial Intelligence / NLP

**Project:** ServiceAI

**Main Concepts:**
NLP + Recommendation System + Data Processing + Gradio

---

## 👨‍💻 Author

**Muhammed Abnas**

Data Science with AI Student

---

## 📜 License

This project is created for educational and learning purposes.
