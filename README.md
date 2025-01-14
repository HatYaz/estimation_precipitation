# estimation_precipitation
yes or no precipitation 

This script estimates the potential for precipitation enhancement using atmospheric stability and cloud water content. It calculates the **Lifted Index (LI)**, an indicator of atmospheric instability, and combines it with cloud water content to produce a precipitation potential score.

### Steps:

1. **Calculate Lifted Index (LI)**:
   - The function `calculate_lifted_index` calculates the difference between the temperature of a rising air parcel and the environmental temperature at 500 hPa. A negative value of the LI indicates instability, which is more favorable for precipitation.

2. **Normalize Cloud Water Content**:
   - The function `calculate_cloud_water_potential` normalizes cloud water content (CWC), scaling it to a value between 0 and 1. This represents the potential for precipitation based on available moisture in the atmosphere.

3. **Estimate Precipitation Potential**:
   - The `estimate_precipitation_potential` function combines the LI (representing atmospheric instability) and the cloud water potential into a final precipitation score. The score is weighted at 60% for instability potential and 40% for cloud water potential.
   - A score closer to 1 indicates higher potential for precipitation.

### Key Functions:
- **calculate_lifted_index**: Calculates LI based on surface temperature, parcel temperatures, and pressure levels.
- **calculate_cloud_water_potential**: Normalizes cloud water content.
- **estimate_precipitation_potential**: Combines LI and cloud water potential to estimate precipitation potential.

### Example Data:
- **Surface Temperature**: 303.15 K (around 30°C).
- **Parcel Temperatures**: Vary with height (1000 hPa to 500 hPa).
- **Pressure Levels**: 1000, 850, 700, and 500 hPa.
- **Cloud Water Content**: 2.5 g/kg.

### Output:
The script prints the **estimated precipitation enhancement potential** based on the input data. The final score ranges from 0 to 1, with 1 indicating the highest potential for precipitation enhancement.

### Example Output:
```
Li: 0.0
Estimated precipitation enhancement potential: 0.00
```

This approach can be used in meteorological modeling to predict the likelihood of precipitation based on atmospheric conditions.
