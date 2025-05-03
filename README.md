# ADM HOMEWORK 3

This is a GitHub repository created to submit the third homework of the Algorithmic Methods for Data Mining (ADM) course for the MSc. in Data Science at the Sapienza University of Rome.

### GROUP 15
Nihal Yaman Yılmaz - nihalyaman20@gmail.com<br>
Matteo Sorrentini - sorrentini.2023085@studenti.uniroma1.it<br>
Arian Gharehmohammadzadehghashghaei - Gharehmohammadzadehghashghaei.2103465@studenti.uniroma1.it<br>
Andrea Stella - astella0303@gmail.com
             
### **Interactive Map Visualization**

Due to GitHub's rendering limitations, interactive maps created using libraries like `Plotly` or `Folium` cannot be displayed directly in this repository. To overcome this, we have provided an **nbviewer** link where you can view our interactive maps and visualizations.

You can view the interactive maps and visualizations by clicking the link below:

👉 **[View Interactive Maps on nbviewer](https://nbviewer.org/github/Nihal-yaman/ADM-HW3/blob/main/Main.ipynb)**




# Homework 3: Purpose and Tasks

## 1. Data Collection
### **Purpose**: To create a dataset of Michelin restaurants.
### **Tasks**:
- **1.1 Get the List of Michelin Restaurants**:
  - Scrape restaurant URLs from the Michelin Guide website and save them into a `restaurants_urls.txt` file.
- **1.2 Crawl Michelin Restaurant Pages**:
  - Download the HTML pages of the scraped URLs.
  - Organize the downloaded pages into folders, grouping 20 restaurants per folder.
- **1.3 Parse Downloaded Pages**:
  - Extract information like restaurant names, addresses, price ranges, and more.
  - Save the extracted data for each restaurant into `.tsv` files.

---

## 2. Search Engine
### **Purpose**: To allow users to query and retrieve restaurant information.
### **Tasks**:
- **2.0 Preprocessing**:
  - Clean and standardize restaurant descriptions by removing stopwords, punctuation, and applying stemming.
- **2.1 Conjunctive Search Engine**:
  - **2.1.1 Create an Index**:
    - Create a vocabulary file (`vocabulary.csv`) mapping each word to a unique `term_id`.
    - Build an inverted index linking terms to document IDs.
  - **2.1.2 Execute the Query**:
    - Process the user query.
    - Return restaurants where all query terms appear in their descriptions.
- **2.2 Ranked Search Engine**:
  - **2.2.1 Create an Index with TF-IDF Scores**:
    - Compute TF-IDF scores for terms in restaurant descriptions.
    - Build an inverted index with TF-IDF scores.
  - **2.2.2 Execute the Query**:
    - Rank restaurants based on Cosine Similarity with the query.
    - Return the most relevant restaurants.

---

## 3. Define a New Scoring Metric
### **Purpose**: To create a ranking mechanism that better reflects user preferences.
### **Tasks**:
- Define a new scoring function:
  - Evaluate query relevance based on TF-IDF scores.
  - Add weight for matching cuisine types.
  - Increase scores for facilities/services matching user preferences.
  - Factor in price ranges for prioritization.
- Use the new scoring function to rank restaurants and compare results with the previous scoring function.

---

## 4. Visualizing the Most Relevant Restaurants
### **Purpose**: To display restaurants on a map, providing a geographic overview to users.
### **Tasks**:
- Gather restaurant coordinates from city and region data (using Google API, OpenStreetMap, or manual methods).
- Create a map with price ranges visualized through marker color or size.
- Highlight the top-ranked restaurants (based on the custom scoring function) on the map.

---

## 5. BONUS: Advanced Search Engine
### **Purpose**: To allow users to perform more detailed and specific queries about restaurants.
### **Tasks**:
- Add the following features for user queries:
  - Search by restaurant name, city, or cuisine type.
  - Filter by price range.
  - Filter by city or region.
  - Filter by accepted credit card types.
  - Filter by services and facilities (e.g., Wi-Fi, air conditioning, parking).
- Create new inverted indexes for fields like `restaurantName`, `city`, and `cuisineType` and apply filters to queries.

---

## Algorithmic Question
### **Purpose**: To develop and analyze an algorithm for a robot collecting packages on a coordinate grid.
### **Tasks**:
1. **Lexicographically Smallest Path**:
   - Ensure the robot moves only upward and rightward to find the shortest path.
   - Select the lexicographically smallest path among all possible shortest paths.
2. **Greedy Algorithm Analysis**:
   - Analyze whether a greedy approach (moving to the nearest package) minimizes total travel distance.
   - Prove the algorithm is optimal or provide a counterexample showing it is not.
