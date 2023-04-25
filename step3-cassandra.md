<!-- TOP -->
<div class="top">
  <img class="scenario-academy-logo" src="https://datastax-academy.github.io/katapod-shared-assets/images/ds-academy-2023.svg" />
  <div class="scenario-title-section">
    <span class="scenario-title">Exercise 1.2: Basic CQL Fundamentals</span>
    <span class="scenario-subtitle">ℹ️ For technical support, please contact us via <a href="mailto:academy@datastax.com">email</a>.</span>
  </div>
</div>


<!-- NAVIGATION -->
<div id="navigation-top" class="navigation-top">
 <a href='command:katapod.loadPage?[{"step":"step2-cassandra"}]' 
   class="btn btn-dark navigation-top-left">⬅️ Back
 </a>
<span class="step-count"> Step 3 of 4</span>
 <a href='command:katapod.loadPage?[{"step":"step4-cassandra"}]' 
    class="btn btn-dark navigation-top-right">Next ➡️
  </a>
</div>

<!-- CONTENT -->

<div class="step-title">Load the CSV dataset into the table and execute queries</div>

✅ Load the newly created table with the `videos.csv` file using the `COPY` command:
```
COPY videos FROM 'assets/videos.csv' WITH HEADER=true;
```

✅ Use `SELECT` to verify the data loaded correctly. Include `LIMIT` to retrieve only the first 10 rows.
```
SELECT * FROM videos LIMIT 10;
```

✅ Use `SELECT` to `COUNT(*)` the number of imported rows. It should match the number of rows `COPY` reported as imported.
```
SELECT COUNT(*) FROM videos;
```

✅ Use `SELECT` to find a row where the `video_id = 6c4cffb9-0dc4-1d59-af24-c960b5fc3652`.
```
SELECT * FROM videos WHERE video_id = 6c4cffb9-0dc4-1d59-af24-c960b5fc3652;
```


<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
 <a href='command:katapod.loadPage?[{"step":"step2-cassandra"}]'
   class="btn btn-dark navigation-bottom-left">⬅️ Back
 </a>
 <a href='command:katapod.loadPage?[{"step":"step4-cassandra"}]'
    class="btn btn-dark navigation-bottom-right">Next ➡️
  </a>
</div>
