---
type: slides
---

# Selecting with Pandas

Notes: Script here.
<html>
<audio controls >
  <source src="placeholder_audio.mp3" />
</audio></html>

---

Congratulations on writing your first code! This is great! We have read in our data and know the dimensions. What now? Let's go over how we would **index**, **slice** and  **select** certain columns or rows of our data.

Notes: Script here.
<html>
<audio controls >
  <source src="placeholder_audio.mp3" />
</audio></html>


---
## Cereal Data

Before doing anything let's bring in some new data called `cereal.csv`

```python
import pandas as pd

df = pd.read_csv('cereal.csv')
df.head()
```

```out


```

<img src='module1/cereal-head.png'>


Notes: Script here.
<html>
<audio controls >
  <source src="placeholder_audio.mp3" />
</audio></html>

---
## Indexing Dataframes

```out


```

<img src='module1/cereal-head.png'>

We can see all the columns of the dataframe and the first 5 rows of the data.
let's say we only want certain rows of the whole dataframe or certain columns.

We talked about how `df.head()` will generate the first 5 rows of a df but what if we wanted rows 5-10?

The first column of this dataframe is called the `index` each row is given a name as well as a position. In this case the name and index are both numbers.
but what if we they were not?

Notes: Script here.
<html>
<audio controls >
  <source src="placeholder_audio.mp3" />
</audio></html>

---

<img src='module1/cereal15.png' width="60%">

Now the index has been set as the name of the cereal (we will talk about how to do this later)

Let's talk about `Almond Delight`.  It's index name is "Almond Delight" but it's index position is 4th.    
If you just double counted and started screaming "5!" at the screen that's ok. In the Python language we start counting at position 0 (then 1, 2, 3, and 4 for Almond Delight). So it's important that we relearn counting from childhood to include 0.

So now let's say we want 5 rows past `Almond Delight` so we want rows with the index names "Apple Cinnamon Cheerios" to "Cap'n'Crunch". How would we do this?


Notes: Script here.
<html>
<audio controls >
  <source src="placeholder_audio.mp3" />
</audio></html>

---

There are 3 main ways:
- .loc[] using index names
- .iloc[]  using index position
- Using [] brackets (we will get into that more next module)


---
In the first case:

``` Python
df.loc[ "Apple Cinnamon Cheerios": "Cap'n'Crunch"]
```


```out


```

<img src='module1/apple-captain.png'>

What about if we only wanted certain columns as well?
Perhaps we were only interested in the `calories` to `fiber` columns?

``` Python
df.loc[ "Apple Cinnamon Cheerios": "Cap'n'Crunch", "calories" :"fiber"]
```


```out


```

<img src='module1/cals-fiber.png'>


So `loc` is used to slice columns and rows by **name** and within an interval.  

Notes: Script here.
<html>
<audio controls >
  <source src="placeholder_audio.mp3" />
</audio></html>
---

# Let's practice!

Notes: Script here
<html>
<audio controls >
  <source src="572_placeholder_audio.mp3" />
</audio></html>