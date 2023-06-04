# -IntroToSQLMoviesFinal

1.  insert into movies (title, runtime, genre, IMDB_score, rating)
    -> VALUES
    -> ('Incredibles 2', 118, 'Animation', 7.8, 'PG'),
    -> ('Red Notice', 118, 'Action', 6.3, 'PG-13');
    
2.  select * from movies where genre = 'Sci-Fi';
3.  select * from movies where IMDB_score >=6.5;
4.  select * from movies where rating in ('G', 'PG') and runtime <100;
5.  select genre, AVG (runtime) as average_runtime FROM movies WHERE IMDB_score <7.5 GROUP BY genre;
6.  Update movies set rating = 'R' where title = 'Starship Troopers';
7.  ((((need to create a new ID column thn)))) 
    select ID, rating from movies where genre IN ('Horror', 'Documentary');
8.  select rating, Avg(IMDB_score) As average_score,
    -> max(IMDB_score) As maximum_score,
    -> min(IMDB_score) As minimun_score
    -> from movies group by rating;
9. select rating, Avg(IMDB_score) As average_score,
    -> max(IMDB_score) As maximum_score,
    -> min(IMDB_score) As minimun_score
    -> from movies group by rating
    -> Having COUNT(*) >1;
    
10. delete from movies where rating = 'R';
11. drop table movies;
12. drop database products;
