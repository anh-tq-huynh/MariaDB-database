# Week 3

## Exercise 3

### Assignment 1
select country.name as "country name", airport.name as "airport name"
    -> from airport, country
    -> where airport.iso_country = country.iso_country and
    -> country.name = "Iceland";
![screenshot](Ex3-Assignment1.png)

### Assignment 2
select name as "airport name"
    -> from airport
    -> where airport.iso_country = "FR" and
    -> airport.type = "large_airport";
![screenshot](Ex3-Assignment2.png)

### Assignment 3
select country.name as "country name", airport.name as "airport name"
    -> from airport, country
    -> where airport.iso_country = country.iso_country and
    -> airport.continent = "AN";
![screenshot](Ex3-Assignment3.png)

### Assignment 4
select elevation_ft
    -> from airport, game
    -> where game.location = airport.gps_code and
    -> game.screen_name = "Heini";
![screenshot](Ex3-Assignment4.png)

### Assignment 5
select elevation_ft *0.3048 as "elevation_m" 
    -> from airport, game
    -> where airport.gps_code = game.location and
    -> game.screen_name = "Heini";
![screenshot](Ex3-Assignment5.png)

### Assignment 6
select name
    -> from airport, game
    -> where location = gps_code and
    -> screen_name = "Ilkka";
![screenshot](Ex3-Assignment6.png)

### Assignment 7
select country.name
    -> from airport, country, game
    -> where airport.iso_country = country.iso_country and
    -> location = gps_code and
    -> screen_name = "Ilkka";
![screenshot](Ex3-Assignment7.png)

### Assignment 8
select goal.name
    -> from goal, game, goal_reached
    -> where game.id = goal_reached.game_id and
    -> goal_reached.goal_id = goal.id and
    -> screen_name = "Heini";
![screenshot](Ex3-Assignment8.png)

### Assignment 9
select airport.name 
    -> from airport, game, goal, goal_reached
    -> where game.id = goal_reached.game_id and
    -> goal.id = goal_reached.goal_id and
    -> location = gps_code and
    -> screen_name = "Ilkka";
![screenshot](Ex3-Assignment9.png)

### Assignment 10
select country.name
    -> from airport, country, game, goal, goal_reached
    -> where goal_reached.goal_id = goal.id and
    -> goal_reached.game_id = game.id and
    -> location = gps_code and
    -> airport.iso_country = country.iso_country and
    -> screen_name = "Ilkka" and
    -> goal.name = "CLOUDS";
![screenshot](Ex3-Assignment10.png)

# Week 4

## Exercise 4

### Assignment 1
select country.name as "country name" , airport.name as "airport name"
    -> from airport
    -> inner join country on airport.iso_country = country.iso_country
    -> where country.name = "Finland" and
    -> scheduled_service = "Yes";
![screenshot](Ex4-Assignment1.png)

### Assignment 2
select game.screen_name, airport.name 
    -> from game
    -> inner join airport on game.location = airport.gps_code
    -> ;
![screenshot](Ex4-Assignment2.png)

### Assignment 3
select screen_name, country.name
    -> from game
    -> inner join airport on location = gps_code
    -> inner join country on airport.iso_country = country.iso_country;
![screenshot](Ex4-Assignment3.png)

### Assignment 4
select airport.name, game.screen_name
    -> from airport
    -> left join game on location = gps_code
    -> where airport.name like "%Hels%";
![screenshot](Ex4-Assignment4.png)

### Assignment 5
select goal.name, screen_name
    -> from goal
    -> left join goal_reached on goal_reached.goal_id = goal.id
    -> left join game on goal_reached.game_id = game.id
    -> ;
![screenshot](Ex4-Assignment5.png)

## Exercise 5

### Assignment 1



