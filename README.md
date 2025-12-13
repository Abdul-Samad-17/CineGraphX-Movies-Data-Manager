# 🎬 CineGraphX

**Movies Data Manager Using Core Data Structures (No STL)**
FAST-NUCES | Fall 2025

---

## 📌 Project Overview

CineGraphX is a C++-based Movies Data Manager designed to demonstrate the **practical power of classical data structures** by building a mini recommendation system from scratch — **without using STL**. The system processes the **IMDb 5000 Movie Dataset** and enables searching, relationship discovery, recommendations, and shortest-path analysis between movies.

This project is developed as a **Term Project** for the Department of Artificial Intelligence & Data Science, FAST‑NUCES.

---

## 🎯 Objectives

* Implement all core data structures **manually** (no STL).
* Efficiently organize and search movie data.
* Model real-world relationships between movies using graphs.
* Simulate recommendation systems using graph traversal.
* Strengthen understanding of recursion, memory management, and system design.

---

## 📂 Dataset

* **Source:** IMDb 5000 Movie Dataset (Kaggle)
* **Records:** ~5000 movies
* **Key Attributes Used:**

  * Title
  * Genres
  * Actors
  * Director
  * Release Year
  * Rating
  * Duration

The dataset is parsed from a CSV file using file handling only.

---

## 🧠 Data Structures Used

### 🌳 AVL Tree / BST

* Central storage of movies (key: movie title)
* Supports insertion, deletion, and search

### 🗂️ Hash Table

* Indexing actors and genres
* Fast mapping between movies and attributes

### 🔗 Linked List

* Stores:

  * Movie genres
  * Actor filmographies
  * Adjacency lists for graphs

### 🌐 Graph

* Each movie is a vertex
* Edges connect movies sharing actors or genres
* Enables recommendations and relationship discovery

---

## ⚙️ Core Functionalities

### 🔍 Search

* By movie title
* By actor
* By genre
* By release year
* By rating range

### 🎥 Recommendation System

* Given a movie title, recommends similar movies
* Implemented using **BFS / DFS** on the movie graph

### 🔗 Shortest Connection Path

* Finds the shortest relationship path between:

  * Two movies
  * Two actors
  * Directors
* Based on shared attributes

---

## 🧩 Class Structure (High-Level)

### `MovieNode`

* Stores all movie metadata
* Maintains linked lists of actors and genres

### `ActorNode`

* Stores actor name
* Linked list of movies acted in

### `Graph`

* Vertices: Movies
* Edges: Shared actors or genres
* Implements BFS, DFS, and shortest path

### `HashTable` & `LinkedList`

* Custom implementations for indexing and traversal

---

## 🛠️ Implementation Rules

* ❌ STL usage strictly prohibited
* ✅ Recursive algorithms used where applicable
* ✅ Dynamic memory handled carefully (no leaks)
* ❌ Global variables discouraged
* ✅ Clean formatting & meaningful naming

---

## 🧪 How to Run

1. Place the IMDb CSV dataset in the project directory
2. Compile using a standard C++ compiler:

   ```bash
   g++ *.cpp -o CineGraphX
   ```
3. Run:

   ```bash
   ./CineGraphX
   ```

---

## 🚀 Final Note

CineGraphX bridges **classic data structures** with **real-world recommender systems**, proving that powerful systems don’t need libraries — just solid fundamentals.
