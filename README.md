



# Project1_DA_Ironhack
![img](https://th.bing.com/th/id/OIP.BKAQJ2Yd21yuXxALpBHqFAHaEK?w=271&h=180&c=7&r=0&o=5&dpr=1.34&pid=1.7)

## Introduction

This repo contains the work done in the first project of the Data Analytics Bootcamp (June 2022). During two weeks I've been teached Python and different notebooks as Pandas. This first project entails cleaning a dataset, using Pandas and extract some insights after that.

## Data import & raw data information.

The data comes from the following webpage (it is suposed to contain historical data of worlwide shark attacks).
URL: https://www.sharkattackfile.net/index.htm

In this webpage, some inputs are given:

1. **Why study shark attacks?** 

1. **Shark species** 

1. **Report an incident**

1. **Investigators** 


## Data Cleaning.

As a first step of cleaning the data, the following process has been done: deleating the rows containing null values in all the columns. Also, as null values kept being present, I chose 4 columns that were explanatory for the purpose of this project. If the value was null for any of the following columns, this means not enough information was given so the row was eliminated as well: fatal accident or not, specie type, sex, and activity that was doing the victim.



## Determination of data type per column:

Once this step was done, the following one was cleaning the data set column by column so that the final data type was the following:

**case_number** --> This would be usefull for each case identification. As we have the index for identifying each case, let's take this column as irrelevant. That is why it is not going to be cleaned. Column type will be unchanged and it will remain as "Object".

**date** --> This must be in date time as data type. Let's going to fix it.

**year** --> This column should be integer. Let's going to fix it.

**type** --> Let's fix this column so the type of attack is reduced to 5-6 different attacks.

**country** --> Let's fix this column so no repeated countries are found.

**area & location** --> For the purpose of this analysis we do not need extactly to know the location and area in each country. So let's just solve the null values.

**activity** --> Let's try to clean this column so no same activities are described differently.

**name** --> Irrelevant for our purpose. With the age and sex we have enough information about the victims.

**age** --> Let's clean this column so at the end all the values of the columns are integers.

**fatal** --> This should be boolean. True if it was fatal and False if it was not fatal.

**time** --> Irrelevant for our purpose.

**species** --> Irrelevant for our purpose.

**Rest of the columns** --> Irrelevant ofr our purpose.

Final data type acomplished:
![DataTypes]("C:\Users\alexd\Ironhack\Project1_DA_Ironhack\Images\DataTypes.png")

## Final insigts

### Insight 1
Conclusión: sesgo temporal. No han incrementado los ataques de tiburones a lo largo de los años. Simplemente hay más datos.

### Insight 2
Conclusión: La gran mayoría de los ataques son no provocados. El tiburón ataca por propia supervivencia. No porque alguien le ataque.

### Insight 3
Conclusión: Los ataques se producen mientras la víctima realiza una actividad en el medio natural de los tiburones: el mar.

### Insight 4
Conclusión: La gran mayoría de las victimas son de sexo masculino. Esto no significa que la comida preferida de los tiburones sean hombres. Sino porque los deportes marinos son practicados principalmente por hombres.



End of Project 1!!