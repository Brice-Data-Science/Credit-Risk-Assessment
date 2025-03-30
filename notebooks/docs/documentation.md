# Documentation

### GitHub Location:
- https://github.com/Brice-Data-Science/Credit-Risk-Assessment

### Project Development Steps

1. **Initial Setup** ✅
    - Created project repository
    - Set up basic project structure
    - Added initial documentation

2. **Data Analysis Phase** (Current)
    - Created Jupyter notebook for data cleaning and EDA
    - Planned data loading approach using pandas
    - Outlined key steps for data exploration
    - Documented methodology in markdown cells

3. **Planned Next Steps**
    - Load and inspect the credit card default dataset
    - Clean and preprocess the data
    - Perform exploratory data analysis
    - Create visualizations for key insights
    - Prepare data for modeling

### Development Notes

## 2025-03-17
- Set up initial Jupyter notebook structure
- Added markdown documentation for:
    - Project overview
    - Data source information
    - Project objectives
    - Step-by-step methodology for data cleaning and EDA

### Tools and Libraries
- Python 3.10.16
- Key packages:
    - pandas (for data manipulation)
    - matplotlib/seaborn (for visualization)
    - scikit-learn (for future modeling)
    - numpy (for numerical operations)

### Best Practices Being Followed
- Clear documentation in markdown
- Structured notebook with distinct sections
- Version control with descriptive commit messages
- Step-by-step approach to data analysis


## 2025-03-29
- Loaded data from excel file via pandas into a dataframe.
- The data was imported as an object with the dtype

### 🧠 What does `dtype: object` mean in pandas?

When a column in a DataFrame has `dtype: object`, it means:

- The column is storing **Python objects**, not a specific data type like `int`, `float`, or `bool`.
- Most often, this means it's **storing strings**.
- But it can also mean **mixed types**, like some rows with strings, some with numbers, or even `NaN`.

---

### 🧪 Why is this a problem when you expect numeric data?

If a column is supposed to be numeric, but pandas sees it as an object, it could cause issues when:

- You're doing **math** (`+`, `-`, `mean()`, etc.)
- You're **plotting**
- You're running **models** (which expect numeric features)

---

### 🚨 Common Causes of `dtype: object` in Excel columns

- **Hidden characters**  
  e.g. `"123 "` (with a space), or a tab `\t`, or even a currency symbol like `"$123"`

- **Missing values entered as text**  
  e.g. `"N/A"` or `"-"` or `"missing"` instead of actual `NaN`

- **Commas in numbers**  
  e.g. `"1,234"` will be treated as a string unless cleaned

- **Mixed types in the column**  
  e.g. some values are numbers, but one rogue string like `"error"` sneaks in
