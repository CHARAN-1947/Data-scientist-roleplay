# Data Profile

## Total Number of Records for Each Table

| Table Name       | Number of Records |
|------------------|-------------------|
| Attribute table  | 10,000            |
| Business table   | 10,000            |
| Category table   | 10,000            |
| Checkin table    | 10,000            |
| Elite_years table| 10,000            |
| Friend table     | 10,000            |
| Hours table      | 10,000            |
| Photo table      | 10,000            |
| Review table     | 10,000            |
| Tip table        | 10,000            |
| User table       | 10,000            |

# Distinct Records by Primary or Foreign Key

## Total Distinct Records for Each Table

| Table Name       | Key(s)            | Distinct Records |
|------------------|-------------------|------------------|
| Business table   | id                | 10,000           |
| Hours table      | business_id       | 1,562            |
| Category table   | business_id       | 2,643            |
| Attribute table  | business_id       | 1,115            |
| Review table     | id                | 10,000           |
|                  | user_id           | 9,581            |
| Checkin table    | business_id       | 493              |
| Photo table      | id                | 10,000           |
|                  | business_id       | 6,493            |
| Tip table        | user_id           | 573              |
|                  | business_id       | 3,979            |
| User table       | id                | 10,000           |
| Friend table     | user_id           | 11               |
| Elite_years table| user_id           | 2,780            |



# Null Values in Users Table

**Are there any columns with null values in the Users table? Indicate "yes," or "no."**

**Answer:** No

**SQL code used to arrive at answer:**
```sql
SELECT *
FROM user
WHERE id IS NULL OR name IS NULL OR review_count IS NULL OR yelping_since IS NULL OR useful IS NULL OR funny IS NULL OR cool IS NULL OR fans IS NULL OR average_stars IS NULL OR compliment_hot IS NULL OR compliment_more IS NULL OR compliment_profile IS NULL OR compliment_cute IS NULL OR compliment_list IS NULL OR compliment_note IS NULL OR compliment_plain IS NULL OR compliment_cool IS NULL OR compliment_funny IS NULL OR compliment_writer IS NULL OR compliment_photos IS NULL;


### SQL Query and Results

```sql
-- Query to retrieve minimum, maximum, and average values for specified columns

-- For Table: Review, Column: Stars
SELECT
    MIN(Stars) AS Min_Stars,
    MAX(Stars) AS Max_Stars,
    AVG(Stars) AS Avg_Stars
FROM
    Review;

-- For Table: Business, Column: Stars
SELECT
    MIN(Stars) AS Min_Stars,
    MAX(Stars) AS Max_Stars,
    AVG(Stars) AS Avg_Stars
FROM
    Business;

-- For Table: Tip, Column: Likes
SELECT
    MIN(Likes) AS Min_Likes,
    MAX(Likes) AS Max_Likes,
    AVG(Likes) AS Avg_Likes
FROM
    Tip;

-- For Table: Checkin, Column: Count
SELECT
    MIN(Count) AS Min_Count,
    MAX(Count) AS Max_Count,
    AVG(Count) AS Avg_Count
FROM
    Checkin;

-- For Table: User, Column: Review_count
SELECT
    MIN(Review_count) AS Min_Review_count,
    MAX(Review_count) AS Max_Review_count,
    AVG(Review_count) AS Avg_Review_count
FROM
    User;

| Table     | Column         | Min | Max | Avg     |
|-----------|----------------|-----|-----|---------|
| Review    | Stars          | 1   | 5   | 3.7082  |
| Business  | Stars          | 1.0 | 5.0 | 3.6549  |
| Tip       | Likes          | 0   | 2   | 0.0144  |
| Checkin   | Count          | 1   | 53  | 1.9414  |
| User      | Review_count   | 0   | 2000| 24.2995 |

