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
## WebGoat GENERAL/DEVTOOLS
<img width="2722" height="1491" alt="image" src="https://github.com/user-attachments/assets/8c043090-a3b6-4de7-8318-e2d9af53af78" />

WebGoat 4 was relatively simple, just type a command in to the console

<img width="2723" height="1629" alt="image" src="https://github.com/user-attachments/assets/112a6ad9-96a4-457a-994a-dfaeea53f817" />

WebGoat 6 was harder as it took me 5 min of touoble shooting to relize i hadn't opend the request tab.

## SQLZoo
### SQLZoo 0 Basics
<img width="901" height="1200" alt="image" src="https://github.com/user-attachments/assets/41e37a58-b82c-43c8-baef-ef4a352f32be" />

### SQLZoo 2 SELECT_from_WORLD_Tutorial
1. The first excercice is a simple Print (SELECT) ```SELECT name, continent, population FROM world```
2. Here we need to use WHERE witch is like a if true print ```SELECT name FROM world WHERE population >= 200000000```
3. Here we incorperate some renaming and math ``` SELECT name, gdp / population AS 'gdp/population' FROM world WHERE population >= 200000000 ```
4. We simply have a if string = x ``` SELECT name, ROUND(population / 1000000.0, 4) AS 'population/1000000' FROM world WHERE continent = 'South America' ```
5. Here we use the IN function to shorten the 3 or statements ``` SELECT name, population FROM world WHERE name IN ('France', 'Germany', 'Italy') ```
6. LIKE means it searches for something containing a string. the % in the string indicates that tehre can be anything in that direction, so if i go 'a%' that means anything starting with a ``` SELECT name FROM world WHERE name LIKE '%United%' ```
7. Simple or statement ``` SELECT name, population, area FROM world WHERE area > 3000000 or population > 250000000 ```
8. same but using xor which is "OR not AND" ``` SELECT name, population, area FROM world WHERE area > 3000000 xor population > 250000000 ```
9. We do some more math in the SELECT, but we have to round this time. the number afther the "," is the decimal we round to ``` SELECT name, ROUND(population / 1000000.0, 2) AS 'population/1000000', ROUND(gdp/ 1000000000.0, 2) AS 'gdp/1000000000' FROM world WHERE continent = 'South America' ```
10. the "Decimal" has to be negative in order to round past 0 ``` SELECT name, ROUND(gdp / population, -3) AS 'gdp/population' FROM world WHERE gdp >= 1000000000000 ```
11. We simply compare length ``` SELECT name, capital FROM world WHERE LENGTH(name) = LENGTH(capital) ```
12. You are supposed to use <> but i prefer the clarity of using NOT for the reader ``` SELECT name, capital FROM world WHERE LEFT(name, 1) = LEFT(capital,1) AND NOT name = capital ```
13. Here we use the LIKE statement liberally utlilzing AND statements ``` SELECT name FROM world WHERE name LIKE '%a%' AND name LIKE '%i%' AND name LIKE '%u%' AND name LIKE '%e%' AND name LIKE '%o%' AND name NOT LIKE '% %' ```
