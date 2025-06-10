# Solar Rooftop Analysis Tool

An AI-powered tool for analyzing rooftop satellite imagery to assess solar installation potential, built for the Solar Industry AI Assistant Internship Assessment.

## Features
- Upload PNG/JPG rooftop images for analysis.
- Uses OpenRouter API for area, orientation, shading, and obstruction detection.
- Fallback to placeholder data (100m², south-facing, 10% shading, 1 chimney).
- Calculates annual energy production (~7,300 kWh/year).
- Estimates cost (~$10,500 after 30% incentive) and payback period (~7 years).
- Provides installation recommendations (e.g., monocrystalline panels, ~50 panels).

## Setup Instructions
1. **Install Python**: Ensure Python 3.8+ ([python.org](https://www.python.org/downloads/)).
2. **Clone Repository**:
   ```cmd
   git clone https://github.com/harshitvishnoi08/Rooftop_analysis.git
To access the app follow https://rooftop-image-analysis.streamlit.app/
