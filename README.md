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
reached 96% of accuracy in classifying the dataset images. The recommendation system uses the
label of the recognized ingredient to obtain the recipes, which are searched through the Edamam
API.
