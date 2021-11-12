# Marvin classification
Python classification algorithm deployment using Marvin Apache.
Marvin is a ML-Ops tool created by B2W Digital to help deploying ML models.

## Installing marvin and python virtualenv
https://marvin.apache.org/marvin-platform-book/ch2_toolbox_installation/overview/
 
## First approach
### Cloning the repo
> the easiest way tbh



1. Clone the example engine from the repository 


``` 
git clone git@github.com:letMarchezi/marvinClassification.git
```

2. Generate a new Marvin engine environment for the Iris species engine

```
workon python-toolbox-env
marvin engine-generateenv ../engines/marvinClassification/
```
3. Run the classification engine

```
workon marvinClassification-engine-env
marvin engine-dryrun 
```

4. Deploy

```
marvin engine-httpserver
```
 
 5. (Optional) Predicting through API

In your internet browser type ``` localhost:8000/docs ``` and find the predictor section

Then click on the third label from top to bottom and on "Try Out"

In the white box type something like this: ``` {"message": ["Hobbit"]} ```
You can change the content inside bracket to any game, makeup, toy or book name.
Click on "Execute" and you should see the prediction output bellow.


 
## Second approach
### Creating your engine on your own


1. Clone the repo containing python notebook 

``` 
git clone git@github.com:letMarchezi/marvinClassification.git
```

2. Create engine

Follow the Creating a new engine section in this link https://github.com/marvin-ai/marvin-python-toolbox
naming the project as marvinClassification

3. Entering the env 
```
workon marvinClassification-engine-env
```

4. Inserting notebook
```
marvin notebook
```
then upload the downloaded file sample.ipynb to the notebook and run it

5. Mark every step as the respective function in the pipeline

6. Test the project by executing dryrun
```
marvin engine-dryrun
```

7. If no errors appear, you can deploy the project in your localhost
```
marvin engine-httpserver
```

8. Using API's to predict


The steps are the same as section 5 from the first approach.
