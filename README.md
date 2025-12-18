# TradePlanCalculator
A single html &amp; javascript based calculator to help you decide what price and num to sell/buy

# Stock Trade Plan Calculator

This is a web-based, client-side tool designed to help stock investors create and evaluate potential trading plans based on their existing positions and market expectations. It provides data-driven support for intra-day or short-term trading decisions by dynamically calculating buy/sell price points under various scenarios.

## ✨ Features

- **Dynamic Trade Plan Generation**: Automatically calculates the required buy or sell prices to achieve your target profit based on parameters you set, such as desired profit and estimated support levels.
- **Multiple Data Loading Options**:
    - **File Import**: Quickly import all your stock positions from a Tab-separated `.csv` file (e.g., `positions.csv`).
    - **Manual Management**: Add, edit, and delete individual stock positions directly within the user interface.
- **Flexible Calculation Parameters**:
    - **Base Trading Volume**: Freely set a base number of shares (in lots) to generate trading plans, rather than always using the total position size.
    - **Price Limit (%)**: Customize the daily price fluctuation limit for risk assessment.
    - **Estimated Support Price / Desired Total Profit**: Core parameters used to back-calculate trade prices.
- **Interactive Holdings List**:
    - **Select All**, **Invert Selection**, and **Delete** controls for managing the loaded data.
    - **Inline Editing** for quantity, cost price, and current price. Calculations and validations will react instantly to your changes.
- **Real-time Risk Validation**:
    - As you input parameters, the system instantly checks if the prices fall outside the next day's price limits and provides clear warnings.
    - In the final generated plans, theoretically actionable and non-actionable trades are highlighted based on the price limits.
- **Pure Client-Side, No Backend**: Built with zero external dependencies. All calculations are performed in your browser, ensuring data privacy and security.

## 🚀 How to Use

1.  **Open the Application**
    - Download the project and open the `股票交易计划计算器.html` file in any modern web browser to get started.

2.  **Step 1: Load and Select Holdings**
    - **Option A: Load from File**:
        - Prepare a `.csv` file separated by **Tabs**.
        - The file must contain the following headers and corresponding data columns: `证券代码` (Stock Code), `证券名称` (Stock Name), `证券数量` (Quantity), `成本价` (Cost Price), `当前价` (Current Price).
        - Click the **"Click to select '...' file"** button and choose your file.
    - **Option B: Add Manually**:
        - Click the **"Add Position Manually"** button.
        - Fill in the stock information in the form that appears and click **"Confirm Add"**.
    - **Interact with Data**:
        - The loaded data table is interactive. You can click directly on the **Quantity**, **Cost Price**, and **Current Price** cells to edit their values, or click the **Delete** button to remove a record.
    - **Select Holdings**:
        - Check the box next to one or more stocks for which you want to create a trading plan.
        - Click the **"Next"** button.

3.  **Step 2: Set Parameters and Calculate**
    - Fill in the separate calculation parameters for each stock you selected.
        - The **"Estimated Support Price"** field will be pre-filled with the stock's current price by default.
    - Once all parameters are set, click **"Start Calculation"**.

4.  **Step 3: Review the Comprehensive Plan**
    - The system will generate a plan card for each selected stock, containing both a **Decrease Plan (Sell)** and an **Increase Plan (Buy)**.
    - The plan clearly lists the specific order prices required to meet your desired profit for various trade sizes.
    - It also uses distinct colors to highlight which plans are theoretically actionable within the next day's price fluctuation limits.

## 🛠️ Tech Stack

- **HTML**
- **CSS**
- **Vanilla JavaScript (ES6+)**

This project is built entirely with native web technologies, without any third-party frameworks or libraries, ensuring it remains lightweight and high-performance.
