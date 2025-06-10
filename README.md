# **Solar Rooftop Analysis Tool**

## **Overview**
The Solar Rooftop Analysis Tool is an AI-powered application designed to estimate solar energy potential, calculate ROI, and provide actionable recommendations for solar panel installation. By analyzing rooftop images, this tool helps homeowners and solar professionals make informed decisions about adopting solar energy.

---

## **Features**
- **Image Upload**: Accepts PNG/JPG rooftop images for analysis.
- **AI-Powered Analysis**:
  - Uses OpenRouter API to detect rooftop area, orientation, shading percentage, and obstructions.
  - Falls back to placeholder data when API results are unavailable (e.g., 100m², south-facing, 10% shading, 1 chimney).
- **Solar Potential Calculation**: Estimates annual energy production (~7,300 kWh/year).
- **ROI Estimation**:
  - Calculates installation costs (~$10,500 after a 30% incentive).
  - Predicts payback period (~7 years).
- **Actionable Recommendations**:
  - Panel Type: Monocrystalline (20% efficiency).
  - Estimated Number of Panels: ~50 (2m² per panel).
  - Maintenance Tips: Annual cleaning, app-based monitoring.

---

## **Setup Instructions**
### **Option 1: Access the Live App**
Visit the deployed app: [Solar Rooftop Analysis Tool](https://rooftop-image-analysis.streamlit.app/)

---

### **Option 2: Run Locally**
1. **Install Python**: Ensure you have Python 3.8+ installed. Download from [python.org](https://www.python.org/downloads/).
2. **Clone the Repository**:
   ```bash
   git clone https://github.com/harshitvishnoi08/Rooftop_analysis.git
   cd Rooftop_analysis
   ```
3. **Install Dependencies**:
   - Use `pip` to install required packages:
     ```bash
     pip install -r requirements.txt
     ```
4. **Set Up Environment Variables**:
   - Create a `.env` file in the project root:
     ```plaintext
     OPENROUTER_API_KEY=your_api_key
     ```
5. **Run the Application**:
   ```bash
   streamlit run app.py
   ```
6. Open the app in your browser at `http://localhost:8501`.

---

## **Key Calculations**
1. **Solar Potential (kWh/year)**:
   - Formula:
     ```text
     Annual Energy = Usable Area (m²) × Insolation (hours/day) × 365 × Panel Efficiency
     ```
   - Defaults:
     - Panel Efficiency: 20%.
     - Insolation: 5 hours/day.
     - Orientation Adjustment: South-facing yields maximum efficiency.

2. **ROI (Return on Investment)**:
   - Formula:
     ```text
     Payback Period = Total Cost (after incentives) ÷ Annual Savings
     ```
   - Defaults:
     - Cost per Watt: $3.
     - Incentives: 30% subsidy.
     - Electricity Rate: $0.12/kWh.

---

## **Assumptions and Limitations**
- Placeholder data used when API fails.
- Insolation fixed at 5 hours/day (does not consider regional variations).
- Simplistic shading percentage estimation.
- Assumes static electricity rates and incentives.

---

## **Future Enhancements**
- Integration of location-based weather and sunlight data.
- Dynamic shading analysis using advanced AI models.
- Batch image processing for large-scale projects.
- Cost breakdown for detailed financial insights.

---

## **Contact**
For questions, feedback, or collaboration:
- **Name**: Harshit Vishnoi
- **Email**: vishnoih10@gmail.com
- **GitHub**: [harshitvishnoi08](https://github.com/harshitvishnoi08)

---

### **License**
This project is licensed under the MIT License. See the `LICENSE` file for details.
