# Netflix Content Intelligence Dashboard | Power BI

An interactive, five-page Power BI dashboard for analyzing Netflix's content catalog, including content types, genres, ratings, geographic distribution, catalog growth, and individual titles.

## Table of Contents

- [Project Overview](#project-overview)
- [Project Objectives](#project-objectives)
- [Dataset](#dataset)
- [Tools and Technologies](#tools-and-technologies)
- [Data Cleaning and Transformation](#data-cleaning-and-transformation)
- [Data Model](#data-model)
- [DAX Measures and Calculations](#dax-measures-and-calculations)
- [Dashboard Pages](#dashboard-pages)
- [Interactivity and Design](#interactivity-and-design)
- [Key Metrics](#key-metrics)
- [Skills Practiced](#skills-practiced)

## Project Overview

Netflix Content Intelligence is a Power BI dashboard built to explore and analyze Netflix's content catalog. The report combines data preparation, data modeling, DAX calculations, and interactive visualizations in a consistent Netflix-inspired design.

The dashboard is organized into five pages, moving from an executive overview to content analysis, geographic distribution, growth trends, and title-level exploration.

## Project Objectives

- Understand the distribution of Movies and TV Shows.
- Analyze content by genre, rating, and release year.
- Explore content distribution across countries.
- Examine Netflix catalog additions over time.
- Enable title-level exploration through interactive filters.

## Dataset

- **Dataset:** Netflix Titles
- **Records:** 8,807
- **Columns:** 12

The dataset contains the following fields:

`show_id`, `type`, `title`, `director`, `cast`, `country`, `date_added`, `release_year`, `rating`, `duration`, `listed_in`, and `description`.

## Tools and Technologies

- **Power BI Desktop:** Dashboard creation and data visualization
- **Power Query:** Data cleaning and transformation
- **DAX:** Measures and calculated columns
- **Data Modeling:** Relationships between the main dataset, calendar table, genre table, and country table

## Data Cleaning and Transformation

The following transformations were performed in Power Query:

- Assigned appropriate data types to the dataset columns.
- Applied Trim and Clean transformations to relevant text columns.
- Replaced missing Director, Country, and Cast values with `Unknown`.
- Replaced missing Rating values with `Not Rated`.
- Replaced missing Duration values with `Unknown`.
- Corrected rating entries containing duration-like values, including `66 min`, `74 min`, and `84 min`, by classifying them as `Not Rated`.
- Split the `listed_in` column by comma into rows to create a genre analysis table.
- Split the `country` column by comma into rows to create a country analysis table.
- Standardized country values and cleaned and trimmed the resulting text.
- Preserved the original Duration column and created separate analytical columns for movie duration in minutes and TV show seasons.

Blank `date_added` values were retained rather than removed.

## Data Model

The project uses four tables:

| Table | Purpose |
|---|---|
| `Netflix` | Main content dataset |
| `Netflix_Genre` | Genre-level analysis |
| `Netflix_Country` | Country-level analysis |
| `Calendar` | Date-based analysis |

### Relationships

- `Calendar[Date]` → `Netflix[date_added]`
- `Netflix[show_id]` → `Netflix_Genre[show_id]`
- `Netflix[show_id]` → `Netflix_Country[show_id]`

The relationships use a one-to-many structure with single-direction filtering. The Calendar table was marked as a date table, and its Month column was sorted by Month Number.

## DAX Measures and Calculations

DAX was used to calculate KPIs and support the report's analysis.

### Content KPIs

- `Total Titles`
- `Total Movies`
- `Total TV Shows`
- `Movie %`
- `TV Show %`

### Duration Analysis

- `Avg Movie Duration (Min)`
- `Avg TV Seasons`
- `Movie Duration Minutes` — calculated column
- `TV Show Seasons` — calculated column

### Content Additions and Trends

- `Titles Added`
- `Movies Added`
- `TV Shows Added`
- `Latest Year Added`

### Genre and Geographic Analysis

- `Titles by Genre`
- `Total Countries`
- `Titles by Country`
- `Movies by Country`
- `TV Shows by Country`

Additional measures were created for the Page 4 KPI cards to preserve overall catalog totals when Calendar filters were applied.

## Dashboard Pages

### 1. Executive Overview

Provides a high-level view of the Netflix catalog.

**Includes:**
- KPI cards for total titles, movies, TV shows, and content percentages
- Netflix Titles Added Over Time
- Content Type Distribution
- Top Genres by Number of Titles
- Content Distribution by Rating

### 2. Content Analysis

Examines content characteristics and distribution.

**Includes:**
- Average movie duration
- Average TV show seasons
- Movie Duration Distribution
- TV Shows by Number of Seasons
- Content Distribution by Rating
- Total Titles by Release Year

### 3. Geographic Analysis

Explores the geographic distribution of Netflix content.

**Includes:**
- Total Countries and content KPIs
- Global Content Distribution map
- Top 10 Countries by Number of Titles
- Movie vs. TV Shows by Country
- Country Content Summary table

### 4. Content & Growth Trends

Analyzes catalog additions over time.

**Includes:**
- Netflix Content Growth Over Time
- Movie vs. TV Share of Additions
- Content Additions by Quarter
- Annual Content Addition Summary matrix

### 5. Detailed Explorer

Provides a title-level view of the Netflix catalog.

**Table columns:**
- Title
- Type
- Release Year
- Rating
- Duration
- Country
- Genre
- Date Added

The page includes filters for content type, release year, rating, and date added, along with a searchable title slicer.

## Interactivity and Design

The report includes:

- Interactive slicers
- A Clear All Slicers button
- Page navigation
- KPI cards, charts, a map, and tables
- A consistent Netflix-inspired theme across all five pages

### Color Palette

| Dashboard Element | Hex Code |
|---|---|
| Background | `#000000` |
| Cards and Visuals | `#2B2727` |
| Accent | `#FF0000` |
| Primary Text | `#FFFFFF` |
| Gray Elements | `#808080` |

## Key Metrics

The completed dashboard displays the following values:

| Metric | Value |
|---|---:|
| Total Titles | 8,807 |
| Total Movies | 6,131 |
| Total TV Shows | 2,676 |
| Movie Share | 69.6% |
| TV Show Share | 30.4% |
| Average Movie Duration | Approximately 99.6 minutes |
| Average TV Seasons | Approximately 1.8 |
| Latest Year Added | 2021 |

## Skills Practiced

- Data cleaning and transformation using Power Query
- Data modeling and relationship management
- DAX measures and calculated columns
- Date-based analysis using a Calendar table
- Data visualization and KPI design
- Interactive slicers and report navigation
- Multi-page dashboard development
- Data presentation through a consistent visual theme

## Conclusion

The Netflix Content Intelligence dashboard brings together data preparation, data modeling, DAX calculations, and interactive visualizations in a five-page Power BI report. The project demonstrates practical application of Power BI for analyzing a content catalog and presenting the results in a structured, interactive format.

**Project Status:** Completed  
**Primary Tool:** Microsoft Power BI Desktop
