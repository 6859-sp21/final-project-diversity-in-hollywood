# 6.859 Final Project: Diversity in Hollywood

Jenning Chen, Ashwin Srinivasan, Cindy Yang, Lisa Yoo

[Link to our visualization](https://6859-sp21.github.io/final-project-diversity-in-hollywood/)    
[Link to our video](https://youtu.be/vTpfYm6oH8Y)     
[Link to our paper](final/6_859_Final_Project.pdf)  

## Abstract
Inspired by the #OscarsSoWhite movement in 2015, our visualization experience empowers users to explore diversity in Hollywood, and how the distribution of race and ethnicity relate to different measures of success: movie reception and awards. We bring together datasets on major awards (Oscars, Golden Globes, Screen Actors' Guild) and box office statistics and create digestible visualizations to see how white Hollywood really is. 

## Summary Image
![alt text](images/summary_image.png)

## Running Instructions
Clone the repository. In the terminal, run `python -m http.server`. Navigate to `http://localhost:8000/` to view the landing page.

## Project Process & Contributions
The contributions made by each team member are listed below.

### Jenning
- Aided in gathering datasets and scraped supplementary data for actor races
- Worked with Lisa to brainstorm and develop the reception bubble plot 
- Designed the home page
- Reformatted and restyled the awards cluster graph visualization
### Ashwin 
- Added cluster graph visualization for Screen Actors Guild
- Helped create the line graphs on awards pages
- Helped style the awards cluster graph visualization
### Cindy
- Added cluster graph visualization for Golden Globes   
- Helped create the line graphs on awards pages   
- Helped style the awards pages   
### Lisa
- Created dropdown autocomplete search bar
- Implemented and styled reception comparison visualization
- Helped preprocess movies dataset
- Initial reception page styling & bubble plot

### Project Process
For our final project, we chose to extend the work we'd done for A4 because we thought there was still much to explore. We began by brainstorming potential extensions and additional visualizations to build on the narrative we already had, which included the new perspective of box office reception, inclusion of other acting/directing award datasets, and extra visualizations to better break down our awards datasets. Ashwin + Cindy worked on the awards page, while Jenning + Lisa worked on the reception page -- the process for each team was to gather/scrape datasets, spec out visualizations, then implement. 

## Resources Used
D3 code references: [https://www.d3-graph-gallery.com/](https://www.d3-graph-gallery.com/graph/circularpacking_basic.html), [https://dev.to/nenadra/how-to-make-a-search-box-with-a-dropdown-in-javascript-4j9p](https://dev.to/nenadra/how-to-make-a-search-box-with-a-dropdown-in-javascript-4j9p)


Data and images retrieved from:
- Oscars: [data.world](https://data.world/crowdflower/academy-awards-demographics)
- Golden Globes: [kaggle](https://www.kaggle.com/unanimad/golden-globe-awards)
- SAG: [kaggle](https://www.kaggle.com/unanimad/screen-actors-guild-awards)
- Race data: [NNDB](https://nndb.com/), 
- Top movies metadata: [boxofficemojo.com](https://www.boxofficemojo.com/chart/top_lifetime_gross/?area=XWW), [kaggle](https://www.kaggle.com/stefanoleone992/imdb-extensive-dataset)
- Industry-wide data: [datausa.io](https://datausa.io/profile/soc/actors)
- Movie posters: [TMDB](https://www.themoviedb.org/)
