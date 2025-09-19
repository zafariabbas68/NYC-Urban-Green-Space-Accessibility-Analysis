# NYC-Urban-Green-Space-Accessibility-Analysis
# Professional Report: NYC Urban Green Space Accessibility Analysis

## Executive Summary

This comprehensive geospatial analysis examines the accessibility of public parks across New York City using a 0.5-mile walking distance threshold. The study reveals that **87.6% of NYC's land area** is within walking distance of public parks, while **12.4% (37.5 square miles)** lacks adequate park access. Manhattan demonstrates the highest accessibility at 98.3%, while Staten Island shows the lowest at 80.6%.

## Project Overview

This project employs advanced geospatial analysis techniques to evaluate urban green space equity across New York City's five boroughs. The analysis combines multiple datasets to provide actionable insights for urban planners, policymakers, and community stakeholders.

## Key Findings

### 1. City-wide Accessibility Metrics
- **Total City Area**: 302.1 square miles
- **Accessible Area**: 264.6 square miles (87.6%)
- **Inaccessible Area**: 37.5 square miles (12.4%)
- **Total Parks Analyzed**: 2,054 public parks
- **Total Park Area**: 30,488 acres

### 2. Borough-level Analysis
| Borough | Area (sq mi) | Accessible Area (sq mi) | Accessibility (%) | Number of Parks | Park Density (parks/sq mi) |
|---------|-------------|------------------------|------------------|----------------|---------------------------|
| Manhattan | 22.84 | 22.45 | 98.33% | 391 | 17.12 |
| Brooklyn | 69.39 | 63.98 | 92.20% | 614 | 8.85 |
| Bronx | 42.58 | 37.51 | 88.07% | 391 | 9.18 |
| Queens | 109.10 | 93.77 | 85.95% | 466 | 4.27 |
| Staten Island | 58.24 | 46.93 | 80.58% | 153 | 2.63 |

### 3. Park Characteristics
- **Average Park Size**: 14.8 acres
- **Largest Park**: 2,771.7 acres
- **Park Size Distribution**: Wide variation from small pocket parks to large recreational areas

### 4. Population Context
- **Total Population**: 8,516,000 residents
- **Population Density Range**: 8,137 to 71,491 people per square mile
- **Highest Density**: Manhattan (71,491 people/sq mi)
- **Lowest Density**: Staten Island (8,137 people/sq mi)

## Methodology

### Data Sources
1. **NYC Borough Boundaries**: Official shapefile from NYC Department of City Planning
2. **Parks Properties**: Comprehensive dataset of NYC public parks
3. **Population Data**: Borough-level demographic statistics

### Analytical Approach
1. **Spatial Processing**: All data reprojected to EPSG:2263 (NY State Plane Feet) for accurate distance measurements
2. **Buffer Analysis**: 0.5-mile (2,640 feet) walking distance buffers around park centroids
3. **Accessibility Calculation**: Spatial intersection between buffers and city area
4. **Density Analysis**: Grid-based park density heatmap generation
5. **Borough-level Assessment**: Individual analysis for each of NYC's five boroughs

### Technical Implementation
- **Python Libraries**: GeoPandas, Matplotlib, Contextily, NumPy, Shapely
- **Coordinate System**: EPSG:2263 (NAD83 / New York Long Island)
- **Visualization**: Professional-grade maps with CartoDB basemaps
- **Export Format**: High-resolution PNG files (300 DPI)

## Critical Insights

### Strengths
1. **High Overall Accessibility**: 87.6% city-wide coverage demonstrates NYC's strong park infrastructure
2. **Manhattan Excellence**: Near-universal park access (98.3%) in the most densely populated borough
3. **Substantial Park Inventory**: 2,054 parks providing 30,488 acres of green space

### Challenges
1. **Geographic Disparities**: Staten Island has significantly lower accessibility (80.6%)
2. **Access Gaps**: 37.5 square miles without park access within walking distance
3. **Density Variations**: Park distribution uneven across boroughs

## Recommendations

### Immediate Priorities
1. **Targeted Development**: Focus on the 12.4% of NYC without park access, particularly in low-accessibility areas
2. **Pocket Parks**: Implement small-scale green spaces in high-density, underserved neighborhoods
3. **Pedestrian Infrastructure**: Improve walking routes and connectivity to existing parks

### Strategic Initiatives
4. **Borough Equity**: Prioritize park development in Staten Island and other lower-accessibility areas
5. **Size Diversity**: Ensure mix of large destination parks and neighborhood pocket parks
6. **Community Engagement**: Involve local residents in park planning and design processes

### Long-term Planning
7. **Climate Resilience**: Integrate green infrastructure with park development
8. **Health Equity**: Align park access with public health objectives
9. **Transit Integration**: Coordinate park development with public transportation networks

## Technical Outputs

The analysis generated comprehensive visualizations and data products:

### Visualizations
1. **Main Accessibility Map**: Parks with 0.5-mile walking distance buffers
2. **Park Density Heatmap**: Spatial distribution of park density
3. **Inaccessibility Analysis**: Areas lacking park access
4. **Borough Accessibility**: Choropleth map of borough-level performance
5. **Park Size Distribution**: Histogram of park acreage
6. **Accessibility Pie Chart**: City-wide access proportion
7. **Top 10 Largest Parks**: Horizontal bar chart of largest green spaces

### Data Products
- **CSV Export**: Borough-level accessibility statistics
- **High-resolution PNGs**: All visualizations (300 DPI)
- **Composite Figure**: Comprehensive overview visualization

## Conclusion

This analysis demonstrates NYC's strong foundation in park accessibility while identifying specific areas for improvement. The 87.6% city-wide accessibility rate is commendable, but the remaining 12.4% without access represents significant opportunity for targeted urban planning interventions.

The borough-level disparities highlight the need for equitable distribution of resources, particularly benefiting Staten Island residents. The combination of large destination parks and neighborhood pocket spaces provides a model for other cities seeking to enhance urban livability through green space accessibility.

This project provides a replicable framework for urban green space analysis that can be applied to other cities worldwide, contributing to the global conversation about sustainable urban development and equitable access to public amenities.

---

# README.md

# NYC Urban Green Space Accessibility Analysis

![NYC Park Accessibility](nyc_park_analysis_output/nyc_park_accessibility_composite.png)

## Project Overview

A comprehensive geospatial analysis evaluating public park accessibility across New York City using a 0.5-mile walking distance threshold. This project identifies areas with limited park access and provides data-driven recommendations for urban planning interventions.

## Key Findings

- **87.6%** of NYC's area has park access within walking distance
- **12.4%** (37.5 sq miles) lacks adequate park access
- **Manhattan** shows highest accessibility (98.3%)
- **Staten Island** shows lowest accessibility (80.6%)
- **2,054** public parks analyzed totaling **30,488 acres**

## Project Structure

```
nyc-park-accessibility/
│
├── data/                    # Raw data files (not included in repo)
├── nyc_park_analysis_output/ # Generated outputs
│   ├── nyc_park_accessibility_composite.png
│   ├── 01_accessibility_map.png
│   ├── 02_park_density_heatmap.png
│   ├── 03_inaccessibility_analysis.png
│   ├── 04_borough_accessibility.png
│   ├── 05_park_size_distribution.png
│   ├── 06_accessibility_pie_chart.png
│   ├── 07_top_10_parks.png
│   └── nyc_park_accessibility_analysis.csv
│
├── nyc_park_analysis.ipynb  # Main analysis notebook
├── requirements.txt         # Python dependencies
└── README.md               # Project documentation
```

## Data Sources

1. **NYC Borough Boundaries**: NYC Department of City Planning
2. **Parks Properties**: NYC OpenData - Parks Properties
3. **Population Data**: NYC Neighborhood Tabulation Areas

## Installation & Setup

### Prerequisites
- Python 3.8+
- Jupyter Notebook
- GeoPandas and spatial dependencies

### Installation
```bash
# Clone repository
git clone https://github.com/yourusername/nyc-park-accessibility.git
cd nyc-park-accessibility

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

### Required Python Packages
```python
geopandas>=0.12.0
pandas>=1.5.0
matplotlib>=3.6.0
contextily>=1.3.0
numpy>=1.23.0
shapely>=2.0.0
openpyxl>=3.0.0
```

## Usage

1. **Data Preparation**: Download required shapefiles and place in `data/` directory
2. **Run Analysis**: Execute the Jupyter notebook `nyc_park_analysis.ipynb`
3. **Review Outputs**: Generated visualizations saved in `nyc_park_analysis_output/`

### Key Analysis Steps
1. Data loading and preprocessing
2. Coordinate system standardization (EPSG:2263)
3. Park buffer creation (0.5-mile walking distance)
4. Accessibility calculation
5. Borough-level analysis
6. Visualization generation
7. Report compilation

## Methodology

### Spatial Analysis
- **Coordinate System**: EPSG:2263 (NY State Plane Feet)
- **Buffer Distance**: 2,640 feet (0.5 miles)
- **Accessibility Calculation**: Spatial intersection analysis
- **Density Analysis**: Grid-based heatmap generation

### Metrics Calculated
- City-wide accessibility percentage
- Borough-level accessibility scores
- Park density per square mile
- Park size distribution statistics
- Population context analysis

## Results

### Visual Outputs
The analysis generates 8 high-resolution visualizations:

1. **Composite Overview**: All analysis components combined
2. **Accessibility Map**: Parks with walking distance buffers
3. **Density Heatmap**: Spatial distribution of parks
4. **Inaccessibility Map**: Areas without park access
5. **Borough Choropleth**: Accessibility by borough
6. **Size Distribution**: Histogram of park sizes
7. **Pie Chart**: Accessible vs inaccessible areas
8. **Top Parks**: Largest parks in NYC

### Data Outputs
- CSV file with borough-level statistics
- High-resolution PNG images (300 DPI)
- Comprehensive analysis report

## Key Statistics

| Metric | Value |
|--------|-------|
| Total City Area | 302.1 sq miles |
| Accessible Area | 264.6 sq miles |
| Inaccessible Area | 37.5 sq miles |
| Accessibility Rate | 87.6% |
| Total Parks | 2,054 |
| Total Park Area | 30,488 acres |
| Average Park Size | 14.8 acres |

## Recommendations

Based on the analysis, we recommend:

1. **Targeted Development**: Focus on areas with less than 80% accessibility
2. **Pocket Parks**: Implement small green spaces in high-density areas
3. **Pedestrian Infrastructure**: Improve connectivity to existing parks
4. **Equity Focus**: Prioritize boroughs with lower accessibility scores
5. **Mixed-size Approach**: Combine large parks with neighborhood spaces

## Applications

This analysis supports:
- Urban planning decisions
- Park development prioritization
- Environmental justice initiatives
- Public health planning
- Community development programs

## Limitations

1. **Walking Distance Assumption**: 0.5-mile threshold may not suit all populations
2. **Park Quality**: Analysis considers access but not park quality or amenities
3. **Population Distribution**: Borough-level data rather than neighborhood-level
4. **Temporal Factors**: Analysis represents a snapshot in time

## Future Enhancements

Potential improvements include:
- Neighborhood-level population data
- Park quality and amenity analysis
- Seasonal accessibility variations
- Public transportation integration
- Environmental justice indicators

## Contributing

Contributions to this project are welcome. Please ensure:

1. Code follows PEP8 guidelines
2. New features include appropriate tests
3. Documentation is updated accordingly
4. Spatial data sources are properly cited

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Citation

If you use this analysis in your work, please cite:

```
NYC Urban Green Space Accessibility Analysis. (2024). GitHub repository. 
https://github.com/yourusername/nyc-park-accessibility
```

## Contact

For questions about this project:
- Email: ghulamabbas.zafari@gmal.com
- GitHub: (https://github.com/zafariabbas68)

## Acknowledgments

- NYC Department of City Planning for boundary data
- NYC OpenData for parks information
- Open-source geospatial Python community

---

This project demonstrates the power of geospatial analysis in informing urban planning decisions and promoting equitable access to public amenities.
