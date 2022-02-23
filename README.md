<h4>Purpose and Analytical Goals</h4>
The database's primary objective is to enable the startup company, Sparkify, to analyze user activity, particularly the songs that their users are listening on their music streaming app. Moreover, it is also crucial that the database design is optimized for the song play analysis queries.
<br>
<h4>Database Schema design and ETL pipeline</h4>
The idea behind the star schemas is simple for analysts and developers to understand and enables end-users to analyze large, multidimensional data sets quickly. Furthermore, since the star schema database has a small number of tables coupled with easy to understand table relationships, queries execute faster. Also, the dimensions are associated with the central fact table, which enforces specific and consistent query results.
<br>
<h4>Instructions (Executing Python Scripts)</h4>
<ol>
<li>Run via terminal the create_tables.py to reset the tables.</li>
<li>Execute the etl.py to process the entire datasets.</li>
</ol>

<h4>File Description</h4>
<ol>
<li>etl.ipynb - notebook to develop ETL processes for each table</li>
<li>test.ipynb - notebook to validate if records were successfully inserted in each table.</li>
<li>create_tables.py - creates the required tables and drops if the tables already exists.</li>
<li>sql_queries - SQL codes for dropping, creating, selecting, and inserting records in the database.</li>
<li>etl.py - the final ETL Pipeline script. Processes the datasets</li>
</ol>

<h4>Schema for Song Play Analysis</h4>
<h4>Fact Table</h4>
<ul>
<li>songplays - records in log data associated with song plays i.e. records with page NextSong
<ul>
<li>songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent</li>
</ul>
</li>
</ul>

<h4>Dimension Tables</h4>
<ul>
<li>users - users in the app
<ul>
<li>user_id, first_name, last_name, gender, level</li>
</ul>
</li>
    
<li>songs - songs in music database
<ul>
<li>song_id, title, artist_id, year, duration</li>
</ul>
</li>

<li>artists - artists in music database
<ul>
<li>artist_id, name, location, latitude, longitude</li>
</ul>
</li>
    
<li>time - timestamps of records in songplays broken down into specific units
<ul>
<li>start_time, hour, day, week, month, year, weekday</li>
</ul>
</li>
    