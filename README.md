Basic implementation of the Gradient Descent algorithm, mainly used to minimize the MSE (Mean Squared Error) of a regression model.

## Relevant files
- `alegrete.py`: where the algorithm lies; 
- `alegrete.csv`: the data used during the training section. It's composed of two columns: the first represents the area of property in Alegrete, and the second represents the value of the property. The following figure is a plot of `alegrete.csv`  

![image](https://user-images.githubusercontent.com/63553534/222920542-f5a5526c-b3f1-4fb6-9b5e-5467cf266fb8.png)

- `alegrete.ipynb`: a notebook that basically displays how good is the trained model.

## Algorithm overview
#### `compute_mse(theta_0, theta_1, data)`
Just calculates the Mean Squared Error of the linear function `theta_0 + theta_1 * X`. This function is being used as a prediction model for the land value in Alegrete.

#### `step_gradient(theta_0, theta_1, data, alpha)`
Updates the values of `theta_0` and `theta_1` by using the Gradient Descent algorithm.

#### `fit(data, theta_0, theta_1, alpha, num_iterations)`
For each iteration, executes one gradient descent step and registers the new values of `theta_0` and `theta_1` in the progress history. When all iterations have been completed, returns the final values of `theta_0` and `theta_1`.

## Good initial values for `theta_0` and `theta_1` and alpha
The following initial values gave us a good MSE for our model:
```python
theta_0 = 0
theta_1 = 0
alpha = 0.01
num_iterations = 100
```

## Final results
### Mean Squared Error
After a number of iterations, the MSE stop getting smaller and ended up being `Final MSE = 10.702138366187492`, as the following plot shows.  

![image](https://user-images.githubusercontent.com/63553534/222920415-217be6ca-e2de-4a20-8002-1b0563b20636.png)

### Resulting linear model
The next figure is a simple plot of the resulting linear model we got using the Gradient Descent algorithm.  

![image](https://user-images.githubusercontent.com/63553534/222920472-eac87294-a3be-430a-b34a-7366499382af.png)  

## Developers

- Enzo Pedro Bonacina [Turma B] 00313316;
- Thales Junqueira Albergaria Moraes Perez [Turma B] 00303035;
- Hiram Artnak Martins [Turma B] 00276484;
