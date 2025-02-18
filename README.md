

---

# UDEMY CRUD SQL Challenge

This project demonstrates SQL CRUD (Create, Read, Update, Delete) operations using a sample `shirts_db` database with a `shirts` table. The file includes examples of common SQL operations for learning and practice purposes.

## Database Structure

**Database Name:** `shirts_db`

**Table Name:** `shirts`

**Table Columns:**
- `shirt_id` (INT, PRIMARY KEY)
- `article` (VARCHAR(30))
- `color` (VARCHAR(25))
- `shirt_size` (VARCHAR(1))
- `times_worn` (INT)

## SQL Operations

### 1. **Database Creation**
CREATE DATABASE shirts_db;
USE shirts_db;

CREATE DATABASE shirts_db;
USE shirts_db;


### 2. **Table Creation**
```sql
CREATE TABLE shirts (
    shirt_id INT PRIMARY KEY,
    article VARCHAR(30),
    color VARCHAR(25),
    shirt_size VARCHAR(1),
    times_worn INT
);
```

### 3. **Data Insertion**
Initial data insertion:
```sql
INSERT INTO shirts (shirt_id, article, color, shirt_size, times_worn) VALUES
(1, "tshirt", "white", "S", 10),
(2, "tshirt", "green", "S", 200),
...
(8, "tanktop", "blue", "M", 15);
```
Additional insertion example:
```sql
INSERT INTO shirts VALUES (9, "polo shirt", "purple", "M", 50);
```

### 4. **Data Retrieval**
- Retrieve all columns:
  ```sql
  SELECT * FROM shirts;
  ```
- Retrieve specific columns:
  ```sql
  SELECT article, color FROM shirts;
  ```
- Filtered retrieval with conditions:
  ```sql
  SELECT article, color, shirt_size, times_worn FROM shirts WHERE shirt_size = "M";
  ```

### 5. **Data Updates**
- Change `shirt_size` for all `polo shirt` entries:
  ```sql
  UPDATE shirts SET shirt_size = "L" WHERE article = "polo shirt";
  ```
- Update multiple fields:
  ```sql
  UPDATE shirts SET shirt_size = "T", color = "off white" WHERE color = "white";
  ```

### 6. **Data Deletion**
- Delete entries with `times_worn >= 200`:
  ```sql
  DELETE FROM shirts WHERE times_worn >= 200;
  ```
- Delete all rows in the table:
  ```sql
  DELETE FROM shirts;
  ```

### 7. **Table Dropping**
Remove the `shirts` table:
```sql
DROP TABLE shirts;
```

## Notes
- The table demonstrates basic SQL operations for learning.
- The `AUTO_INCREMENT` feature could be used for `shirt_id` for real-world scenarios.

## License
This project is for educational purposes only.

---
