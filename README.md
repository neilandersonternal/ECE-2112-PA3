# **ECE-2112-PA3**

**This is made by Neil Anderson D. Ternal from 2ECE-D**

This is mainly for the content of the repository that I've submitted which covers the three Python problems from our assignment from the course
ECE 2112(Advanced Computer Programming). In which includes Base Computing using Python as a language.


# **A. POSITIONAL AND LABEL-BASED SLICING**

**Objectives:**

After loading cars, complete the following operations.

a. Display the shape and complete list of column names of cars.
b. Using positional slicing, create cars 6 to 10 containing rows 6 through 10 of the dataset, where
the first data row is row 1.
c. From cars 6 to 10, display only the columns Model, mpg, cyl, hp, and gear, in that order.

The functions that are used in this problem are:

● ```.iloc()``` - is an indexing property used for purely integer-location based data selection. 
It allows you to select specific rows and columns from a DataFrame or Series by their 0-indexed numerical positions.

This function is used to locate the rows and columns in the data frame. In this case I used it to locate the
cars in row 6 to row 10.

● ```.loc()``` - is a property used for label-based indexing to select, extract, or manipulate specific rows and columns in a DataFrame.

This function was used in this problem to locate the specific rows and columns which was needed for the instruction.
With the format of [rows, columns], I managed to locate the cars from row 6 to 10, and specific columns which are:
Model, mpg, hp, wt. 

```python
cars_6_to_10 = cars.iloc[6:10]

cars_6_to_10 = cars.loc[6:10, ['Model', 'mpg', 'hp','wt']]
```


# **B. MODEL LOOKUP**

**Objectives:**

Use Boolean indexing on the Model column to answer both requests.

a. Display the complete row for Toyota Corolla.
b. For Pontiac Firebird, display only Model, mpg, hp, and wt.

Store the two results in toyota and pontiac, respectively. Do not use a hard-coded row number to
locate either model.

The functions that are used in this problem are:

```python

toyota = cars[cars["Model"] == "Toyota Corolla"]
pontiac = cars[cars["Model"] == "[Pontiac Firebird"][["Model", "mpg", "hp", "wt"]]

```
For the toyota-named function, I mainly navigated the Toyota Corolla by locating in the cars dataframe,
locate in the model section, and find "Toyota Corolla" itself using the "==" operator. This 
'==' operator is used to find exactly an element and in this case is the Toyota Corolla.

For the pontiac-named function, it is like the toyota function. However, there is an additional
manipulation for the function, which is to get only the Model, mpg, hp, and wt datas from the dataframe.


# **C. MULTI-MODEL SUBSETTING**

**Objectives:**


Create a DataFrame named selected cars containing only the records for three models: Datsun 710,
Lotus Europa, and Ferrari Dino.

For these records, retain only Model, mpg, cyl, hp, and gear. Select the rows by their model values
rather than by row numbers. Display selected cars and its shape.

Required check: The final DataFrame must contain exactly three rows and five columns.

For this problem I used this function:

● ```.loc()``` - is a property used for label-based indexing to select, extract, or manipulate specific rows and columns in a DataFrame.

Which I also used for this user-defined function:
```python

selected_cars = cars.loc[[2,27,29],['Model', 'mpg', 'cyl', 'hp', 'gear']]

```

This is a function that navigates through the dataframe to locate specifically the 
models: Datsun 710, Lotus Europa, and Ferrari Dino. Another catch for this problem is that we only
need to particularly get the Model, mpg, cyl, hp, gear. I used the row numbers since there is no
restriction on this problem, but only in letter B, which is a model lookup problem. The 'loc'
immediately navigates through the row 2,27,29 specifically. And search for the Model, mpg, cyl, hp, gear,
which is in the columns section.


That's all for my second assignment. Thank you for reading!!

**README** file version history:

September 5, 2026: Initial README output uploaded.



































