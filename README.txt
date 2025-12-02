This repository contains the processed passenger arrival data used in the computational experiments of the paper.

The dataset is reported in the file minute_passenger_arrivals_avg_method.csv, which provides minute-level passenger arrivals at each station between 07:00 and 09:00.
The data is obtained by disaggregating AFC half-hour aggregated counts into high-resolution time profiles using the randomized sampling procedure described in the paper.

The repository includes a single CSV file:

minute_passenger_arrivals_avg_method.csv
This file contains the simulated passenger arrival data at each station at a resolution of one minute.

Each row of the CSV file corresponds to the arrival of passengers at one station at one specific minute.
The data is organized according to the following structure:

Column	Description
station	Name of the metro station
time	Time step in minutes within the window 07:00–09:00
arrivals	Number of new passengers arriving at the station at that minute


Data Structure

The data can be interpreted as a 2-dimensional matrix indexed by station s and minute t.
Element q[s,t] represents the number of arriving passengers at station s during minute t.

In the CSV file, the matrix is flattened in a row-major order along the time axis, and reported according to the following format:


Thus, all minutes of station 1 are reported first, followed by those of station 2, and so on for all stations included in the case study.
