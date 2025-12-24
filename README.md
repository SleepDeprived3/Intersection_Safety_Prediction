# Prediction model of intersection safety
by: James Hatch

---

# Motivation and Context:

Neural networks are used in many fields to predict a lot of different events. While data comes in all shapes in sizes, more and more location-based data is becomming accessible to the public through platforms such as Open Street Maps (OSM), ArcGIS, Google Maps, and more.

That being said, predictive models are also prone to accumulate biases from their training data. This has led to the creation of models that, while displaying high categorical accuracy, are prone to making biased predictions in response to data. Since models are now being heavily incorporated into highly consequential fields such as incarceration and security, analyzing models for bias has become just as important as analyzing model accuracy.

Each year, thousands of people are killed in fatal car accidents. While accident-predicting models have the potential to save a lot of lives, biases in these models have the potential to reveal even deeper socioeconomic patterns (such as road maintenance and management relative to regional government funding differences). Ultimately, identifying and addressing these patterns might allow us to tackle the more systemic issues that are connected to fatal car crashes.

---

# Model Overview:

I intend to create a multimodal model that identifies fatal crash hotspots in U.S. cities using static street map images (collected using google static street view and fed into a CNN) and weather features (fed into an ANN). This model will be trained and tested using street intersection data collected using OSM (open street maps) and fatal car crash data provided by the FARS dataset.

In order to examine the development of biases in the trained model, I plan on using this model to predict the most common accident hotspots in Chicago. While having a high number of fatal car crashes each year, Chicago is a city know for having significant wealth disparities in different areas of the city. Since factors such as wealth may influence crash-related variables such as road maintenance, I hope to examine the model's predictions for patterns involving the most accident-prone areas in the city.

_Note: I was not able to make it to a full Chicago-level analysis this semester due to google API cost issues, but I will be able to run these tests next semester. Additionally, experimentation revealed that weather data is incompatible with my current model setup. As a result, I plan to use street features in my ANN instead._

## Target City
- Chicago (testing city - high population density)

---

# What you need to run this notebook:
- Street view imagery API key. Use to replace "StreetViewProject" in the notebook

---

## Predictive data
Street Imagery (CNN)
- Static street view google API
- OSM

Additional data
- Census data (estimated population sizes)

---

##Ground truth data
- FARs (fatal car accidents data)


Notes for the data:
- All data must come from 2015-2019 (inclusive) as 2020-2021 was COVID years and 2022-onward has corrupted pathways on the FARS dataset.
