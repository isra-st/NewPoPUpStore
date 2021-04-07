# NewPoPUpStore
The problem to resolve of this repository is about opening a new Pop Up Store for a furniture Retailer in the center of Madrid. We will get this insight through the analysis of empty apartments for renting and selling in Madrid.

# Presentation
If you want to see the presentation click on the below picture.
[![Web Scraping](https://github.com/isra-st/NewPoPUpStore/blob/master/Plots/Circle_map_with_green_area_for_sale_rent.png)](https://github.com/isra-st/NewPoPUpStore/files/6273112/New.PopUpStore.pptx)


* The green circle mark the best suitable area to open a new PopUp store based on real state market.
* The size of the bubbles indicate the number of appartments.
* The marker pins a current PopUp store.

# The insights: 
1. The neighborhoods with the highest number of apartments on sale and renting are Center (sol) and Salamanca’s neighborhoods. The business competition is in the area. The price per meter is expensive in both locations, the hypothesis is that these areas have not a regular turnover. This hypothesis needs to be validated with other kind of data. 
2. Chamberi, Tetuan and Chamartín are adjacent districts. Together have the 18.03% of the real state current Market. According to the analysis. A location between the three districts will be suitable. 
3. Carabanchel and Puente de Vallecas are two areas with potential but the average squared meters and the number of rooms are smaller than the same values in the above districts. 

# Steps of this project: 
1. Select one of the top real state web sites in Madrid:
   URL: www.fotocasa.es
2. Design and preparation of the projects.
3. Web Scraping all rent and sale apartments in Madrid center. 
4. Clean the data. 
5. Import the data to MySQL Workbench.
6. Analyze the data.
7. The insights

# Design and preparation of the project: 
1. I have used Miro to create a visualization of the data I need to get from website. Here the Miro link: https://miro.com/app/board/o9J_lT6lKyU=/
2. I have used Trello as a productive tool to register the requirements needed to the project. https://trello.com/b/jU4yORwC

# Web Scrapping:
After the analysis www.fotocasa.es I have seen that the website is API based.
1. Check if the request to the site web is allowed (get 200).
2. Find the right headers of the site. 
3. Create a function to iterate through the different pages and recollect all the data in two json files. One for selling apartments and another for renting apartments. I've got around 18000 rows and 58 columns of selling apartments and 2300 rows and 8 columns of renting apartments.

# Clean the data: 
1. Get rid of the duplicated rows. I have discovered that half of the flats for selling where duplicated. So, I finalized with 9000 rows of selling flats.
2. The json files were dictionaries oriented and I have normalized all the dictionaries to extract all the values related to the Price, Squared meters, Rooms, Location, terrace, parking, elevator, description of the announce and the links of the flat pictures.
3. I have dropped all the unnecessary columns.
4. I have searched the outliers through boxplot, IQR and Z-Score.
5. I have removed the extreme values. 
6. I have created a new column with the price per squared meter. 
7. Same process for the Rent apartments. 
8. Export the files to CSV. 

# Import to MySQL
1. Create a new schema. "Madrid"
2. Import table sale
3. Import table rent.
4. I have prepared some queries in MySQL Workbench to be used in the analysis of the data. 

# Analyze the data.
1. I've analyzed the places were the business competition has some locations in the center of Madrid. 
2. I have imported to Jupyter notebook the tables and I've filtered and group them base on Qty of apartments, neighborhood, price, surface, rooms and percentage of apartments per districts.

# Conclusions: 
Based in the data and the analysis of the real state current situation. An adjacent location between Chamberi, Tetuan and Chamartin will be the most suitable location to open a PopUpStore for the furniture retailer. 
