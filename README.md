# ===============================================================
# Author(s)     : Lukas Jaeger
# Institution   : University of Bern
#                 Institution for Financial Management
# ===============================================================
"""
Note:
This code builds on the framework from Aramyan (2025).
https://developers.lseg.com/en/article-catalog/article/building-historical-index-constituents

In order to run the code:
  1) Open Refinitiv Workspace;
  2) Generate an API app key to insert in line 46 (Refinitiv Workspace > Search "App Key Generator"))
  3) Define your universe:
          - Country of choice in line 50 (e.g., Switzerland)
          - Index of choice in line 51 (e.g., SPI)
          - Index in line 52 (e.g., SSHI - correct abbreviation can be found in Refinitiv Workspace);
  4) Enter timeframe of investigation in format YYYY-MM-DD in line 55 (start) and 56 (end);
  5) Set your own directory in line 59;
  6) Add variables of your choice in line 191 (Refinitiv Workspace > Search "Data Item Browser");
  7) Run the code (if you have not yet installed the API, use pip install lseg-data).

Saved output in folder:
    - index_constituents_(...): This dataframe includes all firms that have been included in the
                                index within the defined time window.
    - index_constituents_joiners_leavers_(...): This dataframe includes all firms joining or leaving
                                                the index within the defined time window.
    - index_ts_data_(...): This dataframe represents the historical time-series data (e.g., prices)
                           for all index constituents over the defined time window.                                       

Please report any irregularities to Lukas Jaeger (lukas.jaeger@unibe.ch).
"""
