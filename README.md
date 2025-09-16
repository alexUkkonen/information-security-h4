m## OSWAP
### Broken Access Control
* I do a lot of force browsing but for a different purpouse, mainly accesing sites in english rather than finish when the site has no language change option.
### Security Misconfiguration
* This basically gave me the idea of the les you have the easier it is to manage, if you don't need it don't use it. Also make shure you disable all default apps and such since these have known flaws. Directory listing also needs to be disabled.
### Vulnerable and Outdated Components
* This is fairly basic as it basically is just something being out of date. To prevent this, update everything when it becomes availible.
* This is also an issue as sometimes updates might be corrupt in some way. Example: Windows pushed a new W10 update, this new update fried the bios on Dell Q956 computers making them imposible to start without engineers on site.
### Injection
* This is what we did in class. It basically means that data sent by an unveriufied source will be read or that the code can execute code sent by the client.

## Installing WebGoat
* When i was installing the Jdk it wasn't working. I had to look it up and install it with the command ``` $ sudo apt-get install defauld-jdk ``` So i don't know if this is the correct jdk

## SQLZoo
### SQLZoo 0 Basics
<img width="901" height="1200" alt="image" src="https://github.com/user-attachments/assets/41e37a58-b82c-43c8-baef-ef4a352f32be" />

### SQLZoo 2 SELECT_from_WORLD_Tutorial
1. The first excercice is a simple Print (SELECT) ```SELECT name, continent, population FROM world```
2. Here we need to use WHERE witch is like a if true print ```SELECT name FROM world WHERE population >= 200000000```
3. ``` SELECT name, gdp / population AS 'gdp/population' FROM world WHERE population >= 200000000 ```
4. ``` SELECT name, ROUND(population / 1000000.0, 4) AS 'population/1000000' FROM world WHERE continent = 'South America' ```
5. ``` SELECT name, population FROM world WHERE name IN ('France', 'Germany', 'Italy') ```
6. ``` SELECT name FROM world WHERE name LIKE '%United%' ```
7. ``` SELECT name, population, area FROM world WHERE area > 3000000 or population > 250000000 ```
8. ``` SELECT name, population, area FROM world WHERE area > 3000000 xor population > 250000000 ```
9. ``` SELECT name, ROUND(population / 1000000.0, 2) AS 'population/1000000', ROUND(gdp/ 1000000000.0, 2) AS 'gdp/1000000000' FROM world WHERE continent = 'South America' ```
10. ``` SELECT name, ROUND(gdp / population, -3) AS 'gdp/population' FROM world WHERE gdp >= 1000000000000 ```
11. ``` SELECT name, capital FROM world WHERE LENGTH(name) = LENGTH(capital) ```
12. ``` SELECT name, capital FROM world WHERE LEFT(name, 1) = LEFT(capital,1) AND NOT name = capital ```
13. ``` SELECT name FROM world WHERE name LIKE '%a%' AND name LIKE '%i%' AND name LIKE '%u%' AND name LIKE '%e%' AND name LIKE '%o%' AND name NOT LIKE '% %' ```
