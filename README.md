### User Table

| Column   | Type         |
|----------|--------------|
| UserId   | Primary Key  |
| Username | VARCHAR(50)  |
| Email    | VARCHAR(100) |
| Password | VARCHAR(100) |
| Role     | VARCHAR(10)  |

### Profile Table

| Column      | Type        |
|-------------|-------------|
| ProfileId   | Primary Key |
| UserId      | Foreign Key |
| ProfileName | VARCHAR(50) |
| ThemeId     | UUI         |

### Genre Table

| Column  | Type        |
|---------|-------------|
| GenreId | Primary Key |
| Name    | VARCHAR(50) |
| ...     | ...         |

### Movie Table

| Column      | Type         |
|-------------|--------------|
| MovieId     | Primary Key  |
| Title       | VARCHAR(100) |
| Description | TEXT         |
| ReleaseDate | DATE         |
| ...         | ...          |

### Series Table

| Column   | Type        |
|----------|-------------|
| SeriesId | Primary Key |
| MovieId  | Foreign Key |
| Season   | INT         |
| Episode  | INT         |
| ...      | ...         |

### UserMovieWatchlist Table

| Column      | Type        |
|-------------|-------------|
| WatchlistId | Primary Key |
| UserId      | Foreign Key |
| MovieId     | Foreign Key |
| ...         | ...         |

### MovieGenre Table (Many-to-Many)

| Column  | Type        |
|---------|-------------|
| MovieId | Foreign Key |
| GenreId | Foreign Key |

### Project Stack:

<img src="src/angular.png"  width="200px" height="200px">
<img src="src/dotnet.png"  width="200px" height="200px">
<img src="src/postgres.png"  width="200px" height="200px">
