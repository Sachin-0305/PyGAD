# Simple GA based optimization of weight for given linear equation.
## Date:18/10/2025

## AIM/OBJECTIVE
To  develop a Simple GA based optimization of weight for given linear equation.



## PROGRAM
```

import pygad
import numpy  

function_inputs = [4, -2, 3.5, 5, -11, -4.7]
desired_output = 44

def fitness_func(ga_instance, solution, solution_idx):
    output = numpy.sum(solution * numpy.array(function_inputs))  # ensure both are numpy arrays
    fitness = 1.0 / numpy.abs(output - desired_output)
    return fitness
…parent_selection_type = "sss"
keep_parents = 1

crossover_type = "single_point"
mutation_type = "random"
mutation_percent_genes = 10

ga_instance = pygad.GA(num_generations=num_generations,
                       num_parents_mating=num_parents_mating,
                       fitness_func=fitness_func,
…ga_instance.run()

solution, solution_fitness, solution_idx = ga_instance.best_solution()
print(f"Parameters of the best solution : {solution}")
print(f"Fitness value of the best solution = {solution_fitness}")

prediction = numpy.sum(numpy.array(function_inputs) * solution)
print(f"Predicted output based on the best solution : {prediction}")

```

## OUTPUT
<img width="1094" height="77" alt="Screenshot 2025-10-18 084546" src="https://github.com/user-attachments/assets/513d5e7c-fb24-4dba-a50b-8c91e81b60ea" />


## RESULT
Thus,a Simple GA based optimization of weight for given linear equation is developed
