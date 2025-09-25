# 🧹 Data Cleaning Steps  

1. **Remove Duplicates**  
   - Checked for duplicate rows based on `Order ID`.  
   - Dropped duplicates to avoid double-counting sales.  

2. **Handle Missing Values**  
   - Identified null values in key fields (`Order Date`, `Customer Name`, `Sales`, etc.).  
   - Dropped rows with missing IDs or dates.  
   - Filled missing numeric values (`Sales`, `Quantity`, `Profit`) where appropriate.  

3. **Standardize Date Formats**  
   - Converted `Order Date` and `Ship Date` into proper `datetime` format.  
   - Ensured consistent formatting (`YYYY-MM-DD`).  

4. **Fix Data Types**  
   - Converted numerical fields (`Sales`, `Quantity`, `Discount`, `Profit`) to numeric types.  
   - Kept categorical fields (`Segment`, `Region`, `Product Category`) as text.  

5. **Check Outliers & Inconsistent Values**  
   - Validated that `Quantity` values are positive.  
   - Ensured `Discount` values fall between 0 and 1.  
   - Flagged extreme `Sales` or `Profit` values for review.  

6. **Standardize Categorical Fields**  
   - Ensured consistent naming for categories (e.g., avoided “Tech” vs. “Technology”).  
   - Standardized customer names, region names, and segment labels.  

7. **Derive New Fields (Optional)**  
   - Created `Order Month` and `Order Year` columns for trend analysis.  
   - Calculated `Profit Margin` = `Profit / Sales`.  

8. **Final Verification**  
   - Re-checked for missing or invalid values after cleaning.  
   - Confirmed row counts align with expectations.  
