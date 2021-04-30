# 6.859 A4: Oscars

Jenning Chen, Ashwin Srinivasan, Lisa Yoo

[Link to our visualization](https://6859-sp21.github.io/a4-oscars/)

## Background
Our visualization is motivated by the #OscarsSoWhite hashtag, and empowers users to explore trends of diversity among the nominees and winners of the annual Academy Awards (1927-2020). 

## Design Decisions
### Dataset
We started with an open source dataset on Oscar winners in five categories (Best Actor, Best Actress, Supporting Actor, Supporting Actress, Best Director) with some demographic information, [linked here](https://data.world/crowdflower/academy-awards-demographics). Since we were interested in the demographics of the nominees as well, we augmented this with information from the [Academy Awards website](http://awardsdatabase.oscars.org/) and Wikipedia [1](https://en.wikipedia.org/wiki/List_of_black_Academy_Award_winners_and_nominees), [2](https://en.wikipedia.org/wiki/List_of_Hispanic_Academy_Award_winners_and_nominees), [3](https://en.wikipedia.org/wiki/List_of_Asian_Academy_Award_winners_and_nominees).

In assembling our dataset, we wanted the focus of our visualization to be racial diversity. We could have represented more fields about each actor, including gender or age, but thought that these fields were not necessary for the central focus of the visualization. In our original dataset, there were ten different races, but we chose to keep four primary races (White, Black, Hispanic, Asian) and group the rest in an Other category. Since these smaller groups only had one or two points in the whole dataset, we thought this was reasonable in order to make the visualization more succinct and not use too many colors to confuse the user. The alternative, including all races, may have provided more granular information, but having so many races may have caused overly similar colors in our encoding scheme.

### Visual Encodings & UI
We encoded individual people (actors and directors) as dots in our visualization, and used color to encode their race. Since the core aspect we want to examine is race, we decided to make the other information about individuals (name, year, film) in hidden tooltips, which are shown after hovering over a certain dot. 

In terms of positional encoding, to best represent the process of winning an Oscar, from nominee to winner, we thought that the concentric circle arrangement of these dots worked well. We have an Oscar statue in the center, the winners' circle directly around it, then the outer nominee layer being further away. When the user is viewing individuals from multiple categories, we thought it made most intuitive sense to divide the circles into sectors per category. To communicate all of these UI decisions to the user, we made sure to include two legends (one for race, one for the nominees/winners arrangement) and big labels for each of the categories in the visualization. We thought that the color and position encoding were primary factors, so instead of putting them in a tooltip and overcrowding text, we had legends on the side for easy referral. 

Some alternatives we considered were to have use area/bar encodings instead of dots. These would've kept the color encoding by race and the difference between races may have been more easily quantified. However, we thought that the dots conveyed (1) the sheer magnitude of individuals and (2) the fine-grained information per individual, better than our other options. We also thought about arranging the dots in a different way -- one option we considered was a grid of dots, organized by race. Although this might have made the ratio of races more apparent, we thought it would be difficult to portray the distinction between nominees/winners in this arrangement.

On the left side panel, we included some summary statistics: percentages of the white nominees/winners out of the total pools. These percentages are dynamic and change with the selection of years and categories. We thought that this was important to quantify how white the Oscar pool was, since counting individual dots would be difficult for users. We initially considered doing a breakdown by race, using pie charts, but decided that this might be too redundant and would take the focus off of the main visualization. We thought that using these two numbers would be succinct and informative. Although the data wasn't available for comparison (since censuses data is decennial), it would be nice to have a third statistic of overall US white population percentage to compare to. Perhaps there would be other potential bases of comparison for these numbers for a future iteration of this visualization.

Lastly, we used a color scheme reminiscent of the Oscars ceremony, black and gold, and kept the backgrounds and text quite muted. For the main focus, the race color encodings, we used bright colors to contrast against the background and each other, and to draw interest. 

### Interactivity
In order to best engage users and encourage them to explore the data, we incorporated several interactive elements. First, we allow filtering of the data, by an interval of years and by award category. An alternative we considered would have been to filter by singular years instead of a range, but we thought that the interval of years would allow users the flexibility to examine diversity across any time period. When filtering for different categories, we use object physics to animate and reorganize the dots into sectors by category to make the distinctions per category clear. Users can select any combination of categories out of the five. For our main visualization, we allow dynamic zooming so that users can easily adjust the scale.

Additionally, we have tooltips over individual dots, that display the name, film, year per actor or director. Since each dot represents an individual, we thought users might be curious about this fine-grained information, and we wanted to make it available at a glance. Taking inspiration from our MVP feedback, we added a feature that highlights appropriate dots when the mouse hovers over the legend. For instance, in the race legend, when the mouse hovers over a label like White, the White dots are highlighted. In the circles legend, when the mouse hovers over the nominees circle, the nominee dots are highlighted. 

## Development Process & Contributions
Throughout the whole development process, we collaborated, discussed design decisions, and divided the work to implement, by meeting one or two times a week. Overall, this took 50 people-hours, and figuring out the physics in the UI and finding the appropriate data took the most time.

Jenning assembled the dataset via web scraping, worked on the concentric circles UI, and implemented the slider/category filtering. Ashwin worked on the initial circle packing implementation and the tooltips for individual circles and the legends. Lisa added the legend and the summary statistics, as well as the CSS styling.


## Resources Used
D3 Circular packing reference: [https://www.d3-graph-gallery.com/graph/circularpacking_basic.html](https://www.d3-graph-gallery.com/graph/circularpacking_basic.html)

Data retrieved from: [https://data.world/crowdflower/academy-awards-demographics](https://data.world/crowdflower/academy-awards-demographics), 
[Academy Awards website](http://awardsdatabase.oscars.org/), and Wikipedia: [1](https://en.wikipedia.org/wiki/List_of_black_Academy_Award_winners_and_nominees), [2](https://en.wikipedia.org/wiki/List_of_Hispanic_Academy_Award_winners_and_nominees), [3](https://en.wikipedia.org/wiki/List_of_Asian_Academy_Award_winners_and_nominees).

Image from: [https://www.flaticon.com/free-icon/oscar_206982](https://www.flaticon.com/free-icon/oscar_206982)