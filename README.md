# Aviation Accident Analysis

**Authors**: Andy Shen, Andrei Hushcha

## Business Problem

Our client is expanding into the aircraft industry. Specifically, they are interested in purchasing and operating airplanes for commercial and private enterprises, and want to know more about the potential risks of aircraft. 

We are here to determine which airplane manufacturer is the lowest risk for the company to start this new business endeavor.

## Data

The dataset we are using is derived from the [NTSB aviation accident database](https://www.kaggle.com/datasets/khsamaha/aviation-accident-database-synopses).

We are choosing to look at the top 5 commercial and top 5 private manufacturers based on revenue, from [Assets America](https://assetsamerica.com/aircraft-manufacturers/).

The data we will be working with will involve make, engine type, accident type, and number of injuries and fatalities. 

This will give a good idea of what which manufacturers are most reliable to invest in. 

## Methods

We first prepared the data set by creating a column called fatality rate. This was done by summing together the number of injured passengers with the number of uninjured to get the total number of people onboard. We then divide number of fatalities by total onboard to get the fatality rate. 

We then identified the necessary and unnecessary columns based on the business needs and dropped the unneccesary ones. 

Lastly, we removed duplicate entries, removed rows with NULL values, and tidied up formatting. 

## Results

Looking at our results, our recommendations is to go with Boeing and Bombardier for a Commercial manufacturer. For private, go with Cessna and Piper. 

### Fatality Rate by Manufacturers
![graph1](./images/comm_make_fatality_rate.jpg)


![graph2](./images/private_make_fatality_rate.jpg)

Boeing and Bombardier are almost equal at the lowest fatality rate of the manufacturers. Cessna leads the private manufacturers in this area.

### Fatality Rate by Engine Type
![graph3](./images/comm_engine_fatality_rate.jpg)

![graph4](./images/private_engine_fatality_rate.jpg)

Go with a Turbo Fan or Turbo Jet as the engine for commercial makes. For a private make, go with a Reciprocating or Turbo Fan engine. 

### Correlation of Total Passengers Onboard and Uninjured Passengers

![graph5](./images/size_corr_heatmap.jpg)

For both, size matters. The bigger the airplane, the safer. 

## Conclusions

**Commercial make:**

- Boeing and Bombardier are the best options with 3.9% and 4.1% average fatality rate per event.
- When choosing a model client should pay attention to the type of engine: Turbo Fan and Turbo Jet have the lowest fatality rate per event with 3.8% and 4.9% correspondingly.
- Size matters. The bigger airplane, the safer. There is a very strong positive correlation of 0.98 between total on board and uninjured passengers

**Private make:**

- Cessna and Piper are the best options with 17% and 20 % average fatality rate per event.
- Reciprocating and Turbo Fan have the lowest fatality rate per event with 19% and 20% correspondingly.
- Size matters. There is a strong positive correlation of 0.76 between total on board and uninjured passengers

**Other remarks:** 

Despite 2 private makes being involved in 87% of all the events (Cessna 55% and Piper 32%), we still consider them as the top option.

The lowest aircraft damage type "destroyed" between all the private makes is considered to be a strong indirect evidence: Cessna 10% and Piper 12%.

Numbers of events could indicate a big popularity of these 2 makes among clients.

## Future Investigations

- Gather a larger dataset for more accurate analysis. This could include international flights.
- Gather information about general flights such as total flight hours and plane lifetimes. 
- Weigh financial options between the top makes

## For More Information

Please review our full analysis in our [Jupyter Notebook](./Index.ipynb) or our [presentation](./presentation.pdf).

Please review our [Tableau public](https://public.tableau.com/app/profile/andy.shen6894/viz/AirsafetyProject10_05_23/Dashboard4) as well.

For any additional questions, please contact **Andy Shen | itsahaotian@gmail.com, Andrei Hushcha | andrei.hushcha@gmail.com

## Repository Structure

You are in the README.md. 

'Index.ipynb' contains the jupyter notebook that explains our data science steps for you to replicate. In 'notebooks' contains past versions of the jupyter notebook. 'Slides.pdf' contains our slides presentation that sums up important information for the client or audience. In 'data' you will be able to see the dataset we worked with. Likewise, 'images' will contain images used in this 'README.md' generated from code and as well as from the web.

```
├── README.md                           <- The top-level README for reviewers of this project
├── Index.ipynb                         <- Documentation of analysis in Jupyter notebook
├── Slides.pdf                          <- PDF version of project presentation
├── data                                <- Both sourced externally and generated from code
├── images                              <- Both sourced externally and generated from code
├── notebooks                           <- Contains past versions of Jupyter notebook
