# NewPoPUpStore
The problem to resolve of this repository is about oppening a new Pop Up Store for a furniture Retailer in the center of Madrid- We will get this insight through the analysis of empty appartments for renting and saling in Madrid.
# Steps of this project: 
1. Select one of the top realstates web sites in Madrid:
   URL: www.fotocasa.es
2. Design and preparation of the projects .
3. Web Scraping all rent and sale appartments in Madrid center. 
4. Clean the data. 
5. Import the data to MySql Workbench.
6. Analyse the data.
7. The insights

# Design and preparation of the project: 
1. I've used Miro to create a visualization of the data I need to get from website. Here the miro link: https://miro.com/app/board/o9J_lT6lKyU=/
2. I've used Trello as a productive tool to register the requirements needed to the project. https://trello.com/b/jU4yORwC

# Web Scrapping:
After the anlysis www.fotocasa.es I've seen that the website is API based.
1. Check if the request to the site web is allowed (get 200).
2. Find the right headers of the site. 
3. Create a function to iterate throught the different pages and recolect all the data in two json files. One for saling appartments and another for renting appartments. I've got arround 18000 rows and 58 columns of saling appartments and 2300 rows and 8 columns of renting appartments.

# Clean the data: 
1. Get rid of the duplicated rows. I've discovered that half of the flats for saling where duplicated. So I finalized with 9000 rows of saling flats.
2. The json files were dictionaries oriented and I've normalized all the dictionaries to extract all the values related to the Price, Squared metters, Rooms, Location, terrace, parking, elevator, description of the announce and the links of the flat pictures.
3. I've dropped all the unecessary columns.
4. I've search the outliers through boxplot, IQR and Z-Score.
5. I've removed the extreme values. 
6. I've created a new column with the price per squared metter. 
7. Same proccess for the Rent appartments. 
8. Export the files to CSV. 

# Import to MySQl
1. Create a new schema. "Madrid"
2. Import table sale
3. Import table rent
4. I've prepare some queries in MySql Workbench to be used in the analysis of the data. 

# Analyse the data and provide the insights.
1. I've analysed the places were the business comptetion has some locations in the center of Madrid. 
2. I've imported to Jupyter notebook the tables and I've filtered and group them base on Qty of appartments, neighborhood, price, surface, rooms and percentage of appartaments per dictrics.

# The insights: 
1. The neighborhods with the highiest number of appartments on sale and renting are Center (sol) and Salamancas neighborhoods. The business competition is located in the area. The price per metter is expensive in both locations, the hypotesis is that, these areas have not a regular turnover. This hyptosis need to be validated with other kind of data. 
2. Chamberi, Tetuan and Chamartin are adjacents districts. Together have the  18.03 of the realstate current Market. According the analysis. A location between the three districes will be suitable. 
3. Carabanchel and Puente de Vallecase are tow areas with pottential but the average squared metters and the number of rooms are smaller than the same values in the above districs. 

# Conclussions: 
Base in the data and the analysis of the realstate current situation. An adjacent location between Chamberi, Tetuan and Chamartin will be the most suitable location to open a PopUpStore for the furniture retailer. 

