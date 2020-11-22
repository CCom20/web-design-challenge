# Weather Analysis Dashboard
Here you will find the dashboard for the weather analysis project, which provides the basic findings when comparing latitude to max temperature, humidity, cloudiness, and wind speed. 

## About the Dashbaord
The dahsboard was built using Bootstrap. A small amount of CSS was written to mainly provide some additional spacing and a color scheme. I was able to locate some code on stackoverflow to detect the mobile viewport and display appropriately. So the website is not just resposive when changing the size of the window, but if you use any of the browsers' inspect tools and change the viewport to mobile, the website renders appropriately. 

**Navigation**
A simple navigation with a dropdown and is mobile friendly. It is nested in the `<head>` tag, since the body uses the `.container` functionality. The container adds padding left and right of the body, and I wanted the navigation to fully across the page rather than having padding to its left/right. There is dropdown (`plots`) that contains a link to each visualization. 

**Note** It does seem like sometimes you have to clear your cache for the dropdown to work. I updated it code and compared it to Bootstrap's documentation. This could be a server rendering issue, or it could be that I am missing something. However, it does work after waiting a minute and refreshing the page with `ctrl f5`. 

**Landing Page**
The landing page provides a brief overview of the project, and four visualizations all with a brief description and linking to their corresponding page. For these, I used Bootstrap's `card` functionality, which provides a clean and distinguished layout. 

**Data Page**
Data used for the project was read with Panda's CSV reader. The dataframe was then converted to HTML using the `to_html` function. This converted it into an HTML table, and I used some of Bootstrap's library to give it a cleaner look. 

**Other / Lessions Learned**
The rest of the pages follow a simple layout, and all pages use the same navigation. I did creating my website with a slightly different architecture, using `_files` as the asset folder where the CSS and images and data could be referenced. This worked well on my local machine, but in deploying to GitHub pages the `_files` folder was not being read/found. At first I thought this was due to relative paths, but noticed that my other folders were being found (e.g., /visualizations/ for the plots, and /data and /comparisons). 

After a few different path times, a random thought came to me that the `_` might be an issue, since in some programming languages it is an escape character or an ignored variable. I removed it, and all CSS and images loaded perfectly. It took me about 15 or so pushes to GitHub to find this solution. 