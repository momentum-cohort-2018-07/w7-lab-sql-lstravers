# SQL Query Answers

For each of the questions below, add the following information to a Markdown file in your homework repo:

- Your final SQL query (which you must have run and validated on the included database)
- The number of results returned (if more than one)
- The specific result returned (if a single record is returned)

1) **Find all time entries.**  
    -SELECT *  
    -FROM time_entries;  
    _500 rows returned_  
    (https://github.com/momentum-cohort-2018-07/w7-lab-sql-lstravers/blob/development/images/q1_image.png)

2) **Find the developer who joined most recently.**  
    -SELECT *  
    -FROM developers  
    -ORDER BY joined_on DESC;  
    _50 rows returned_  
    -RESULT: Dr. Danielle McLaughlin; joined on 2015-07-10  
    (https://github.com/momentum-cohort-2018-07/w7-lab-sql-lstravers/blob/development/images/q2_image.png)


3) **Find the number of projects for each client.**
    -SELECT COUNT (name), client_id  
    -FROM projects  
    -GROUP BY client_id;  
    _9 rows returned_  
    (https://github.com/momentum-cohort-2018-07/w7-lab-sql-lstravers/blob/development/images/q3_image.png)

4) **Find all time entries, and show each one's client name next to it.**
    -tables needed: time_entries, projects, clients  
    -data columns needed: duration(from time_entries); name(from clients)  
    -JOIN tables clients and projects to match client name with project name 
    -JOIN tables time_entries and projects to match project name with duration  
    -SELECT time_entries.duration and clients.name

5) **Find all developers in the "Ohio sheep" group.**
    -SELECT *  
    -FROM group_assignments  
    -WHERE group_id = 3  
    _3 rows returned_  
    (https://github.com/momentum-cohort-2018-07/w7-lab-sql-lstravers/blob/development/images/q5_image.png)

6) **Find the total number of hours worked for each client.**  
    -tables needed: time_entries, projects  
    -data columns needed: time_entries.duration; projects.client_id  
    -not sure where to go from here??


7) **Find the client for whom Mrs. Lupe Schowalter (the developer) has worked the greatest number of hours.**  
    -tables needed: clients, projects, time_entries  
    -data columns needed: client_id; projects.client_id; projects.id; time_entries.project_id  
    -JOIN tables clients and project to match client_id with projects  
    -JOIN tables projects and time_entires to match project_id with time_entry  
    -not sure where to go from here??


8) **List all client names with their project names (multiple rows for one client is fine).  Make sure that clients still show up even if they have no projects.**  
    -  


9) **Find all developers who have written no comments.**
    -tables needed: comments, developers  
    -data columns needed: comment(from comments); id(from developer)  
    JOIN (both tables) comments.comment_id AND developers.developer_id
    WHERE comment IS NULL


Unless otherwise specified, return all columns in the requested table (e.g. developers).

## **Challenges**

Try these queries if you have time:

- Find all developers with at least five comments.
- Find the developer who worked the fewest hours in January of 2015.
- Find all time entries which were created by developers who were not assigned to that time entry's project.
- Find all developers with no time put towards at least one of their assigned projects.
- Find all pairs of developers who are in two or more different groups together.

### Resources

- [DB Browser for SQLite](https://sqlitebrowser.org/)
- [Markdown](https://guides.github.com/features/mastering-markdown/)