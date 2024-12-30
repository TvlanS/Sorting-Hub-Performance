# Sorting-Hub-Performance

### Sort Hub Performance

Evaluate the productivity of company Z's sorting hubs, specifically focusing on the performance of sort hubs in the Malaysia region.  
A query is to be writen to calculate the total number of parcels processed at each sort hub in East Malaysia daily, categorized by parcel size, for the period from 1th Dec 2024 to 25th Dec 2024.

**Requirements:** 
- **Datetime format:** All datetime values are in UTC. Convert them to local time by adding 8 hours and display the results accordingly.  
- **Parcel size mapping:** The `orders.parcel_size_id` column determines the parcel size. Replace the `parcel_size_id` values with descriptive labels as follows:

| Parcel Size ID | Description |
|----------------|-------------|
| 0              | XXSMALL     |
| 1              | XSMALL      |
| 2              | MEDIUM      |
| 3              | LARGE       |
| 4              | XLARGE      |
| 5              | JUMBO       |

- **Guidelines:**
  - Count a parcel only once per day, even if it is scanned multiple times on the same day.
  - For parcels scanned across multiple days, count them separately for each day.
  - If a parcel is processed at multiple sort hubs, count it once for each hub.
  - Exclude all records associated with test shippers, test hubs, or tracking IDs that include the words "test".
  - Sort the output by sort hub name, date, and parcel size.
 
HUBS
Name	Type	Description	Paraphrased Description
id	INTEGER	This is the unique identifier of each hub.	A unique numeric identifier for each hub.
name	VARCHAR	This is the name of the hub.	The hub’s name.
state	VARCHAR	This is the state of the hub.	The state where the hub is situated.
region	VARCHAR	This is the region of the hub.	The geographical region the hub serves.
type	VARCHAR	This denotes if a hub is a sort hub or a delivery hub.	Indicates if the hub functions as a sort hub or delivery hub.


### Required Output Columns:
| Date       | Sort Hub Name     | Parcel Size   | Total Parcels   |  
|------------|-------------------|---------------|-----------------|  
| ...        | ...               | ...           | ...             |  

