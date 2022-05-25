# li-ion-cells_lifetime-prediction_comparative-study
A comparative study of 9 different Machine Learning models for predicting the EOL(end of life / 85% initial capacity).

### Details:
Li-ion cells have a limited life after which their capacity degrades to a point where they are no longer useful for many applications. This is called end of life(EOL) generally this value is taken to be 80-85% of the initial capacity of the cells. 
The objective of this project was to predict the end of life of a given Li-ion cell using parameters obtained from its initial cycles. We have used 7 parameters from each cycle for each cell :  
1. IR : Internal Resistance
2. Qc : Charge capacity
3. Qd : Discharge capacity
4. Tavg : Average temperature during cycle
5. Tmin : Minimum temperature during cycle
6. Tmax : Maximum temperature during cycle
7. Charge time : Time taken for charging the cell

The first 75 cycles of a cell is used for collecting these parameters after which predictions of *cycle_life* which is the actual number of cyles when cell reached EOL.  

The [original dataset](https://data.matr.io/1/projects/5c48dd2bc625d700019f3204) was created and used in [this repository](https://github.com/rdbraatz/data-driven-prediction-of-battery-cycle-life-before-capacity-degradation) and has been used by multiple research studies. We have used 115 cells out of the 124 in the dataset due to some irregularities and outliers in the dataset.  

Our comparison focuses on practical approach hence we have used minimal amount of data and only 75 cycles.The MAPE(mean absolute percentage error) of the ML models ranges from **18.14%** (*Linear Regression*) to **14.43%** (*XGBoost*).

This repository consists of python code for all the 9 Machine Learning models that were compared along with the processed dataset in csv format.

#### Contributers:
[Gopal Pandey](https://github.com/Ahamasmi)  
[Yash Bhoyar](https://github.com/yashbhoyar)  
[Saksham sharma](https://github.com/sakshamji)  
