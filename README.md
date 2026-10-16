# Metro Advertising Optimization — Bachelor's Project

A final project for a Business Analytics course, using mathematical optimization to plan an advertising campaign targeting students in the Moscow Metro.

## Objective

Determine which metro stations should host advertisements and how many advertisements to place at each station to maximize estimated profit within a fixed budget.

The business scenario considers a company offering paid courses to university students.

## Data

The analysis combines Moscow Metro passenger traffic data for the third quarter of 2023 with information on university and student dormitory locations.

Stations are assigned advertising costs according to their location relative to the Circle Line and the Big Circle Line. Estimated conversion rates depend on the presence of universities near a station and along its metro line.

## Methods

The project formulates an integer optimization problem in CVXPY. The decision variables represent the number of advertisements placed at each station.

The model maximizes estimated revenue minus advertising costs, subject to constraints on:

- The total advertising budget.
- The maximum number of students the company can serve.
- The number of advertisements at each station.
- A requirement to advertise on every metro line included in the analysis.

Scenario analysis examines how the optimal allocation changes when student capacity, advertising prices, and the total budget change. An extended model introduces university-ranking coefficients to represent differences in students’ assumed likelihood of purchasing a course.

## Findings

Under the baseline assumptions, the optimal allocation mainly favors stations outside the city center, while retaining selected central stations with strong student acquisition potential.

Increasing student capacity makes more stations with high passenger traffic attractive. Lower central advertising prices also change the allocation, while reducing the budget from RUB 15 million to RUB 5 million leaves the baseline solution unchanged.

The findings depend on the assumed conversion rates and advertising costs. They demonstrate how optimization can support advertising decisions under different business scenarios.

## Tools

Python, pandas, NumPy, CVXPY, and Matplotlib.
