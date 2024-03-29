# [DFL - Bundesliga Data Shootout](https://www.kaggle.com/competitions/dfl-bundesliga-data-shootout/overview)
## Task
Currently, event data is mostly collected manually by human operators, who gather data in several steps and through numerous personnel involved. This manual process has room for innovation as in its current shape and form it involves a lot of resources and multiple iterations/quality checks. As a result, event data collection is usually reserved for professional competitions only.

Automatic event detection could provide event data faster and with greater depth. Having access to a broader range of competitions, match conditions and data scouts would be able to ensure no talented player is overlooked.
## Data
The competition dataset includes video recordings of nine football games divided into halves. It is necessary to detect three types of player events in these videos: the time of their occurrence and the type. Folders with videos for training and for tests are given, there are also short videos from ten additional games provided without event annotations.
## My solution
Videos were provided as data, but for the correct operation and training of the model, I translated these videos into images with a resolution of 521 by 512. I chose the final model efficientnetv2xl, but I also trained efficientnetb5, reset50, reset101, resnet152, but they did not give the best result. The average precision of detected events was taken as a metric, averaged by threshold values of timestamp errors, averaged by event classes.
## Resualt
With this solution, I managed to get 0.485421 on the private leaderboard and take 92nd place out of 530
