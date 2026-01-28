# Data-Visualization-with-Seaborn-Package-Python-
Developed an interactive data visualization dashboard to analyze and compare nutritional content across popular cereal brands. This project transforms complex nutritional data into intuitive visual insights, helping health-conscious consumers make informed breakfast choices based on their dietary preferences and nutritional goals.


# Dataset Information
#### Source: Kaggle - Cereal Dataset
#### Records: 77 different cereal products
#### Manufacturers: 7 major cereal companies

# Features:
| Column    | Description           | Unit/Values         |
|-----------|----------------------|------------------|
| name      | Cereal brand name     | Text             |
| mfr       | Manufacturer code     | A, G, K, N, P, Q, R |
| type      | Serving temperature   | cold, hot        |
| calories  | Calories per serving  | kcal             |
| protein   | Protein content       | grams            |
| fat       | Fat content           | grams            |
| sodium    | Sodium content        | mg               |
| fiber     | Dietary fiber         | grams            |
| carbo     | Carbohydrates         | grams            |
| sugars    | Sugar content         | grams            |
| potass    | Potassium             | mg               |
| vitamins  | Vitamin percentage    | 0, 25, 100%      |
| shelf     | Display shelf         | 1, 2, 3         |
| weight    | Serving weight        | ounces           |
| cups      | Cups per serving      | cups             |
| rating    | Consumer rating       | 0-100 scale      |

# Manufacturer Key:
* A = American Home Food Products
* G = General Mills
* K = Kelloggs
* N = Nabisco
* P = Post
* Q = Quaker Oats
* R = Ralston Purina

# Some outputs:
```
fig, ax = plt.subplots(figsize = (10,8))
sns.heatmap(adjusted_cereal_corr, mask =adjusted_mask, xticklabels ='auto', annot = True, fmt='.2f', cmap ='Blues',
           vmin = -1, vmax = 1,annot_kws ={"fontsize":13}, linecolor = 'white', linewidth =0.5
           ); #fmt: limit decimals

yticks = [i.upper() for i in adjusted_cereal_corr.index];
xticks = [i.upper() for i in adjusted_cereal_corr.columns];

ax.set_yticklabels(yticks, rotation = 0, fontsize = 10);
ax.set_xticklabels(yticks,fontsize = 10);

title = 'CORRELATION MATRIX\nSAMPLED CEREALS COMPOSITION\n'
ax.set_title(title, loc='center', fontsize = 18);
```
<img width="899" height="590" alt="image" src="https://github.com/user-attachments/assets/42793986-c77f-4467-a842-16b2844070ca" />

