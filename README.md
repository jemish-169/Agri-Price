# Agri-price

## Features

### Android App

- **Offline-first architecture**: Reduces network calls by caching market and crop data locally using Room database.
- **Home**: Shows recently sold prices for selected markets and crops.
- **Crop**: Selecting a crop shows markets with min/max prices of last sold in each market.
- **Market**: Selecting a market displays all sold crops with min/max prices of last updated date.
- **Date filtering**: Users can view data of past 100 days in both crop and market sections.
- **Settings**: Users can reselect their preferences and switch the app theme.

### Backend & Database

- **Data pipeline**: A Python script periodically collects crop pricing data from public sources, processes it, and pushes it to Supabase.
- **Centralized storage**: Supabase acts as the single source of truth for all crop names, market names, and price entries.
- **Data handling**: Only the latest 100 days of data are retained, and unused crop or market records are automatically removed.

## Technology Stack

- **Android-App**:
  - **Android (Kotlin)** – Native Android development using Jetpack Compose  
  - **Jetpack Compose** – Declarative UI toolkit for clean, efficient layouts  
  - **Coroutines** – Managing background tasks smoothly  
  - **Koin** – Lightweight Dependency injection  
  - **MVVM + Clean Architecture** – Ensures a scalable, maintainable, and test-friendly codebase  
  - **Material Design** – Follows Google’s UI/UX guidelines for intuitive design  
  - **Animations** – Enhances user experience with meaningful transitions and effects
  - **Room Database** – For offline first approach and serving cached data on failure
  - **Navigation-3** – Navigation between modules with Back-stack ownership
  - **Jetpack-DataStore** – Flow based user preference saving

- **Backend**:
  - **Python** – Getting data from public data-sources and updating database

- **Database & Cloud**:
  - **Supabase** – Backend-as-a-service for Database, Single source of truth  

## Screenshots


<table>
  <tr>
    <td align="center"><img src="Agri-Price%20app%20ss/1.png" width="250"/></td>
    <td align="center"><img src="Agri-Price%20app%20ss/2.png" width="250"/></td>
    <td align="center"><img src="Agri-Price%20app%20ss/3.png" width="250"/></td>
    <td align="center"><img src="Agri-Price%20app%20ss/4.png" width="250"/></td>
  </tr>
  <tr>
    <td align="center"><img src="Agri-Price%20app%20ss/5.png" width="250"/></td>
    <td align="center"><img src="Agri-Price%20app%20ss/6.png" width="250"/></td>
    <td align="center"><img src="Agri-Price%20app%20ss/7.png" width="250"/></td>
    <td align="center"><img src="Agri-Price%20app%20ss/8.png" width="250"/></td>
  </tr>
</table>
