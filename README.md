# pandemic_simulator

This is a generic exponential growth pandemic simulator.

Please note that this was written by a software developer and not an
epidemiologist. It's not intended to be used for any sort of serious
public policy planning. It is rather intended to be a tool for people
to get some sense of how exponential doubling goes. It was initially
written during the 2020 COVID-19 pandemic for the author to be able to
have some personal idea of when a major crisis would occur.

Please especially note that this tool doesn't do any complex modeling
of an epidemic over time. In a real epidemic, as the infected
population increases, people will self-isolate and measures will be
taken to e.g., reduce public events. This will slow the spread of the
disease in reality, but this tool makes no attempt to model any of
that.

## Usage

pandemic_simulator

The following options are supported:

### --start
The start date, in format YYYY-MM-DD. If the initial population is
more than one, this will be run back at the calculated increase rate
to find patient one and start the simulation from there.

### --end
The end date, in format YYYY-MM-DD. The date to end the simulation if
the --infected ceiling is not ever achieved.

### --infected
The starting infected population.

### --daily
Output information daily instead of weekly

### --doubling
Number of days it takes for the infected population to double

### --mean-hospital-stay
The mean time in days for a hospital stay.

### --hospitalization-rate
The rate at which infected patients are hospitalized, as a multiplier
(i.e., ".1" is "10%"). Patients go into the hospital at this rate,
stay for mean-hospital-stay days, then at the end of that time,
hospitalized-death-rate of them die, and the rest are discharged.

### --hospitalized-death-rate
The rate at which hospitalized patients die at the end of their stay,
as a multiplier (i.e., ".1" is "10%")

## Output

### INFECTED
The total number of people who have ever been infected

### HOSP
The total number of people *currently* in the hospital

### DEAD
The total number of people dead

## License
[MIT](https://choosealicense.com/licenses/mit/)
