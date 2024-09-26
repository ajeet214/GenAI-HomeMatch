# GenAI-HomeMatch

# Real Estate Listings Search with Embedding-Based Filtering

## Project Summary

This project is focused on building an advanced real estate listings search engine using machine learning-based embeddings for efficient text matching, combined with filter-based search capabilities. The core components of the project include:

### 1. Data Ingestion and Embeddings Generation
- Real estate listings are provided in JSON format, containing attributes like location, price, bedrooms, bathrooms, square footage, school rating, and descriptions.
- Descriptions of the listings are converted into numerical vector embeddings using OpenAI’s `text-embedding-ada-002` model. This allows for semantic search capabilities based on property preferences and descriptions.

### 2. Database Management with LanceDB
- The listings data, along with the generated description embeddings, are stored in a LanceDB database.
- The schema of the database includes fields such as location, list price, number of bedrooms and bathrooms, square footage, school ratings, and the description vectors (1536-dimensional embeddings).

### 3. Full-Text Search and Vector-Based Filtering
- A full-text search (FTS) index is created on the `description` column to enable fast and relevant searches based on user queries.
- Users can specify property preferences such as maximum price, minimum bedrooms and bathrooms, square footage, school rating, and textual preferences (e.g., "modern home" or "pool"). The search engine filters results based on these parameters and ranks properties using the vector embeddings for relevance to the user's preferences.

### 4. User Interface with Jupyter Widgets
- A user-friendly interface is created using Jupyter widgets, allowing users to adjust filters like price, number of rooms, and square footage using sliders, and specify property preferences in a text area.

### 5. Natural Language Response Generation
- A response generation system utilizes the filtered search results to provide users with property summaries. Using OpenAI’s GPT-3.5 model, the engine generates natural language descriptions of the top properties that match the user’s preferences.

### 6. Optimized Performance
- The `.gitignore` file ensures that unnecessary files and directories, like Python cache files, virtual environments, and the LanceDB database, are excluded from version control, improving project maintainability and collaboration.

## Key Technologies:
- **LanceDB** for database management and efficient vector-based search.
- **OpenAI API** for generating embeddings and providing property description vectors.
- **Jupyter Widgets** for user input and interface interaction.
- **GPT-3.5** for generating natural language summaries of property listings.

This project combines modern data storage, machine learning, and user-friendly interfaces to create an efficient and intuitive real estate search platform.
