# COMP3120_Data_Store
This repository contains NSW Property Sales bulk data(https://valuation.property.nsw.gov.au/embed/propertySalesInformation) and converted JSON data.  
Raw Bulk data can be found in `raw_data`  
Converted Json data can be found in `json_data`

The raw .dat files were converted from the file format found in: `Current_Propert_Sales_data_File_Format_2001_to_Current.pdf`  
All converted JSON files follow the structure below:
#### JSON Data Structure example:

```
{"Entries":[
	{"C_Date":"2019-11-16", <- dates are handled as yyyy-MM-dd
	"D_Code":"001",         <- District Code
	"P_Sub":"ABERDARE",     <- Propert Suburb
	"Area_Type":"M",        <- Either M or H to signify Metres/Hectares respectively
	"P_Code":"2325",        <- Post Code
	"P_Purp":"RESIDENCE",   <- Purpose of Property
	"P_H_Num":"103",        <- Property House Number
	"S_Date":"2019-12-30",  <- Date of settlement
	"P_Area":"1011.83",     <- Area of Property
	"P_S_Name":"RAWSON ST", <- Property Street name
	"P_Price":"260000",     <- Property Price ($AUD)
	"D_Num":"AP807655",     <- Dealing Number
	"SL_Num":"",            <- Strata Lot Number
	"P_U_Num":""}           <- Property Unit Number
]}
```
## json_data info
Json data from the raw_data was separated into 2 datasets: **Annual** and **Suburb**  
Annual data is separated via year sold.  
Suburb data is separated via their suburbs regardless of sale date.

