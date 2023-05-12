# RecipeIS – Recipe recommendation system based on recognition of food ingredients

Currently, food waste is a global concern, a problem that arises mainly at the
consumption level, which generates environmental, economic, and social impacts. One way to
reduce the food waste problem is to use the food we already have at home. However, this causes
another concern, which is what to cook with certain foods. Sometimes we do not know what
recipes can be made. Knowing which ingredients can be mixed and how to mix them can be a
difficult task for a beginner cook, so selecting the right ingredients for a recipe is essential.
Therefore, it is proposed a recipe recommendation system through image recognition of food
ingredients. Presently, the system is a web application that recognizes an image given by the user
and recommends recipes containing the recognized ingredient. For this, a convolutional neural
network model, the ResNet50, was built to perform image recognition, which was trained with a
dataset, which contains about 36 classes of vegetables and fruits. Through this training, the model
reached **96% of accuracy** in classifying the dataset images. The recommendation system uses the
label of the recognized ingredient to obtain the recipes, which are searched through the Edamam
API.


### 1. Image Recognition

The goal of this food ingredient recognition component is to recognize the
ingredient desired by the user so that it is possible to identify which ingredient it is and
later, which recipes contain that recognized ingredient.  
The image input is given by the user through an upload option on the
homepage of the web application. Next, the ingredient will be recognized through the
implemented model, ResNet50.
To perform the task of recognizing food ingredients, the Flask micro-framework was
utilized. Flask is a framework that allows for the creation of web applications and is
widely used for implementing CNN models. Therefore, a web application was developed
using the Flask framework to implement our CNN model, with two routes established:
- Route 1 - An index page that allows users to upload an image of the food ingredient;
- Route 2 - A prediction page that recognizes the food ingredient image and sends it
to the created model to determine the food ingredient class.

### 2. Recipes recommendation system
To make the recommendation of recipes from the ingredient chosen by the user,
the JavaScript language was used to search the database, API Edamam, by the
recognized ingredient, to return the recipes that contain the recognized ingredient.
We have also made some options for the user, in which the user can choose diets
or preferences from the recommended recipes. From the options selected by the user,
the program will perform a search in the database, with the result of the recognized
ingredient together with the diet options and preferences chosen by the user.
