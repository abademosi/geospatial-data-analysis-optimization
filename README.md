# Geospatial Restaurant Analytics & Optimization

## Overview

This project applies geospatial data analysis and computational optimization techniquesto explore restaurant distribution, ratings, and spatial clustering across multiple UK cities. Using latitude and longitude data, I analyze proximity-based patterns, cuisine distributions, and rating dispersion while comparing different implementation strategies for performance and scalability.

A central focus of the project is code efficiency and optimization, including the use of vectorized operations, modular design, and parallel computing with Numba.

## Key Objectives

- Analyze restaurant distributions within defined geographic radii
- Compare cuisine prevalence and average ratings by location
- Identify spatial clustering of high- and low-rated restaurants
- Efficiently compute large pairwise distance matrices
- Evaluate and optimize alternative coding approaches

## Data

Structured restaurant dataset containing:

  - Geographic coordinates (latitude, longitude)
  - Review counts by rating category
  - Cuisine indicators
  - City-level identifiers
Data is used for educational and analytical purposes


## Methods & Tasks

### 1. Cuisine Distribution Near Points of Interest

- Calculated distances between restaurants and reference locations using the Haversine formula
- Identified cuisine type distributions within a 1 km radius
- Converted dummy-encoded cuisine variables into interpretable labels



### 2. Top-Rated Restaurant Recommendation

- Computed weighted average ratingsusing review count distributions
- Filtered restaurants based on minimum review thresholds
- Implemented user-defined distance and cuisine filters
- Visualized restaurant locations with dynamic map scaling



### 3. Average Ratings by Cuisine Type

- Expanded multi-cuisine entries using `explode()` for accurate aggregation
- Compared average ratings across cuisine types within geographic constraints
- Applied modular filtering functions for reuse and clarity



### 4. Distance Matrix Construction (Optimized)

- Built symmetric pairwise distance matrices between restaurants
- Implemented the Haversine formula using:

  - NumPy for numerical efficiency
  - Numba with parallelization(`prange`) for scalability
- Compared loop-based, vectorized, and parallel implementations



### 5. Spatial Dispersion of Restaurant Ratings

- Analyzed clustering behavior of top-rated vs bottom-rated restaurants
- Used percentile-based thresholds to define rating groups
- Calculated median inter-restaurant distances to assess spatial concentration



## Code Evaluation & Optimization

For each task, I:

- Implemented an original solution
- Compared it against an AI-generated alternative
- Critically evaluated performance, clarity, and scalability
- Refined the final implementation to balance readability and efficiency

This approach emphasizes responsible and informed use of AI tools in data science workflows.



## Tools & Technologies

Python:pandas, NumPy, matplotlib, Numba (parallel computing), Geospatial distance calculations (Haversine)


