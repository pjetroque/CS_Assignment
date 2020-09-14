The title of the following papers pivotal to our knowledge:
* MCC Van Dyke et al., 2019: Fantastic yeasts and where to find them: the hidden diversity of dimorphic fungal pathogens.
* JT Harvey, Applied Ergonomics, 2002: An analysis of the forces required to drag sheep over various surfaces.
* DW Ziegler et al., 2005: Reading acquisition, developmental dyslexia, and skilled reading across languages: a psycholinguistic grain size theory.

![alttext]()

```python
import pandas as pd
import matplotlib.pyplot as plt

data = pd.read_csv("istherecorrelation.csv", delimiter=';')
plt.figure(dpi=300)

plt.scatter(data['WO [x1000]'], data['NL Beer consumption [x1000 hectoliter]'])

for x_pos, y_pos, label in zip(data['WO [x1000]'], data['NL Beer consumption [x1000 hectoliter]'], data['Year']):
    plt.annotate(label,
                xy=(x_pos, y_pos),
                xytext=(7, 0),
                textcoords='offset points',
                ha='left',
                va='center')

plt.xlabel('WO [x1000]')
plt.ylabel('NL Beer Consumption [x1000 hectoliter]')
plt.title('Beer in the Netherlands')

plt.show()
```
