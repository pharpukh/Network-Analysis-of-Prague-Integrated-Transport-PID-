# Network Analysis of Prague Integrated Transport (PID)

## Overview
This project is a university assignment focused on **network analysis** of the Prague Integrated Transport (PID) system using a dataset of **consecutive stops from various transit routes**. The goal is to **analyze the network structure, visualize the transport network, and study key stop centralities** over a given week.

## Dataset
The dataset is derived from **[Prague Integrated Transport Open Data](https://pid.cz/o-systemu/opendata/)** and formatted as `d.csv`, which contains sequential stop connections.

### Dataset Structure (`d.csv`)
| stop_from | stop_from_name | stop_to | stop_to_name | depart_from | arrive_to | route_type | is_night | mon | tue | wed | thu | fri | sat | sun |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| U699Z3P | Stadion Strahov | U981Z1P | Koleje Strahov | 7:24:00 | 7:25:00 | 3 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0 |

Additionally, `stops.txt` provides **geographical coordinates** (latitude and longitude) for each stop.

## Project Structure
```
├── assignment02.ipynb    # Jupyter Notebook with network analysis
├── d.csv                 # Dataset containing sequential stop data
├── stops.txt             # Geographic data for each stop
├── README.md             # Documentation
```

## Requirements
To run this project, install the following dependencies:
```sh
pip install pandas numpy matplotlib seaborn networkx
```

## How to Run
1. **Ensure `d.csv` and `stops.txt` are in the project directory**.
2. **Open Jupyter Notebook**:
   ```sh
   jupyter notebook
   ```
3. **Run `assignment02.ipynb`** step by step, following the markdown explanations.

## Tasks Completed

### 1. Data Preprocessing
- Handling missing or invalid values
- Converting departure and arrival times
- Merging additional stop metadata from `stops.txt`

### 2. Network Construction & Visualization
- **Nodes**: Unique stop names representing stations
- **Edges**: Direct connections between consecutive stops
- **Edge Weights**: Number of trips passing through the connection over a week
- **Graph Visualization** of the transit network

### 3. Centrality Analysis
- **Degree Centrality**: Number of direct connections per stop
- **Betweenness Centrality**: How often a stop is on the shortest path between two others
- **Closeness Centrality**: Average shortest path distance from a stop to all others
- **Visualization of Key Centralities**

### 4. Custom Questions & Insights
- **Are key stops different for daytime vs. nighttime routes?**
- **Do important stops change between weekdays and weekends?**
- **Which stops are critical for overall network connectivity?**

## Evaluation
The analysis includes:
- **Comprehensive data cleaning and transformation**
- **Graph construction using NetworkX**
- **Detailed visualization of network structure**
- **Interpretation of stop importance based on centrality measures**

## Author
Farukh Rustamov

