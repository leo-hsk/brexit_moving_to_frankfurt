# Brexit: Moving to Frankfurt
This is an submission to the Final Assignment of the ‘Applied Data Science’-Course provided by Coursera and hosted by IBM.

Since Great Britain left the European Union on the 31st of January this year, the employees of 30 banks and 20 financial service providers are going to move to Frankfurt. At least 1500 new jobs were created in the banking sector in Frankfurt. Since a good connection to restaurants, green spaces and cultural offers is more and more important for townspeople it is important to provide information about the different boroughs and neighourhoods of the financial capital of Germany. Employers are interested in the smooth relocation of employees so that they can return to work as soon as possible.

The goal is to compare the boroughs and neighbourhoods of London with the boroughs and neighbourhoods from Frankfurt, using data science techniques and machine learning. The employers and employees can use the information to find places in Frankfurt that are quite similar (e.g. same diversity of venues) to their home in London.

## Acknowledgments
This repo uses the [Foursquare](https://de.foursquare.com/) API to get information about top venues of different boroughs of Frankfurt.  
I also used [Folium](https://python-visualization.github.io/folium/) to create an interactive map of Frankfurt and [geopy](https://geopy.readthedocs.io/en/stable/) to get coordinates.  
My thanks to [Alex Aklson](https://github.com/aklson-datascientist) for leading the [‘Applied Data Science’-Course](https://www.coursera.org/specializations/applied-data-science) and for teaching different tools and techniques to make this exciting work possible!  

## Approach
### Prepare Data - ‘Data Preparing.iynb’
For the London and Frankfurt data there exist Wikipedia pages that got a table of the bouroughs.
<https://en.wikipedia.org/wiki/List_of_London_boroughs>  
<https://de.wikipedia.org/wiki/Liste_der_Stadtteile_von_Frankfurt_am_Main>  
So I am going to scrape the page to get the data and  I have to structure the data. Then I am going to add latitude and longitude using geopy and I will export the datasets as csv.  

###  Data Analysis – ‘Data Analyses.ipynb’
After we got the data in a right structured format, we apply some data analysis to the data to get more Insights about the two locations. More concretely I will create folium maps to get a visual feedback of the data I am working with. Then I will use Foursquare API to get the top 100 venues of the boroughs and I will apply the KMeans machine learning algorithm to cluster the boroughs and to assign the London boroughs to the boroughs of Frankfurt.

### Final Results – ‘Final Results.ipynb’
In this notebook I am going to present the clustered data using a folium map and make some assumption.
