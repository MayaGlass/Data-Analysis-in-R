# Data-Analysis-in-R

The following project is written in R and consists of an RMD file, and an HTML file, with all of the results.

### part 1 calculation of average distances on the face of the earth and in the USA with a simulation I created, and custom functions
* I calculated the mean geodesic and euclidean distance on the face of the earth, using a simulation of 1000 pairs of points. Then I compared the disttribution of both distances.
* I created a function that generates n random points from a specific country using rejection sampling. It samples a point. If it is in the desired country, then the point is returned. Otherwise, while the point is not in the country, it keeps sampling again and again. Than I used that function to sample 2000 points from the USA, and calculate the mean geodesic distance in the country.

### part 2 - annalization of the world's population and countries, from data extracted from tables from different Wikipedia pages
* First, I extracted and manipulated the data from the HTML pages, using the rvest library, and regex. Additional information about the manipulations performed can be found in the comments within the code.. 
* I merged the two dataframes by the country-name. In order to do so, I annalyzed diffrences and similarities between the two tables.
* I used the merged info in order to calculate the density for each country, and presented the top 3 least dense countries in the world. In addition, I created a world map, colored by density.
* Next, I used the function that samples a point from a desired country in order to calculate the average distance between *two people* living on the planet. Instead of sampeling random points, I sampled two countries, and that sampled a point from each country. I calculated the distance between the two points, and repeated this process 1000 times. I then compared the results with the average geodesic distance calculated in part 1.

### part 3 - estimation of each country's size
* Using a simulation, I reapeatedly sampled thousands of points from the face of the earth. I than matched each point to a country.
* For each country, I calculated its size as the relative size of the samples found in its territory, out of all the samples taken, times the surface area of ​​the earth.
* Then, I compared my estimation with the true size extraced from Wikipedia. I used a plot to present the real size vs. the estimation.

### Part 4 -  Analysis and visualization of earthquake geographical data
* In this part, I annalysed and visualised information about all the earthquakes from 2022.
* Then, I used a statistic to check the hypothesis that the distribution of earthquakes over the time of the day is uniform.