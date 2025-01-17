# Computer Name Extractor
This Python script processes a file containing DHCP information and extracts computer names based on specific identifying characters. It leverages the standardized format of the input documentation to isolate and clean hostnames for further use.
## Features
- **File Parsing**: Reads and processes a text file (`EchoHealth_DHCP.txt`) containing network-related information.
- **Hostname Extraction**: Identifies and extracts computer names containing the identifying substring `"NTD"`.
- **Data Cleaning**: Removes unnecessary domain suffixes (`".teleperformanceusa.com"`) and duplicates, ensuring a clean output.
- **File Outputs**: Produces three output files at different stages of data processing:
 1. `ECH_Hostname.csv`: Contains raw extracted hostnames.
 2. `Hostnames_Cleaned.txt`: Contains hostnames cleaned of domain suffixes.
 3. `FinalValues.txt`: Contains unique and cleaned hostnames.
## How It Works
1. **Input File**: The script reads from the file `EchoHealth_DHCP.txt`.
2. **Extraction**: Hostnames containing the substring `"NTD"` are identified and written to `ECH_Hostname.csv`.
3. **Cleaning**: Removes the domain suffix `".teleperformanceusa.com"` and stores the cleaned data in `Hostnames_Cleaned.txt`.
4. **Deduplication**: Filters out duplicate hostnames, saving unique results in `FinalValues.txt`.
5. **Summary**: Outputs the total number of identified hostnames.
## Usage
1. Place the file `EchoHealth_DHCP.txt` in the same directory as the script.
2. Run the script using Python:
  ```bash
  python script_name.py
3. Processed files (ECH_Hostname.csv, Hostnames_Cleaned.txt, and FinalValues.txt) will be generated in the same directory.
Requirements
• Python 3.x
• Input file (EchoHealth_DHCP.txt) containing DHCP information in a standardized format.
Output Example
Final Hostnames (FinalValues.txt):
NTD-PC1
NTD-PC2
NTD-PC3
Notes
• The script assumes that the input file follows a specific standardized format for extracting relevant information.
• You can modify the substring "NTD" in the script to adapt it to different naming conventions.
