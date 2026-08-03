# Model-Rocket

A basic model rocket flight simulator built in MATLAB, using App Designer for the GUI. You enter rocket and motor parameters and it calculates the flight (thrust, drag, gravity) and plots altitude, velocity and acceleration over time.

## What it does

- Simple GUI made in App Designer, no need to touch code to run a simulation
- Takes inputs like rocket mass, diameter, drag coefficient (Cd)
- Uses either a motor thrust curve or an average thrust value
- Plots altitude/velocity/acceleration vs time
- Gives estimated apogee and total flight time

## Physics model

The rocket is treated as a 1D point mass. Forces considered:

- Thrust, from the motor curve or average thrust input
- Drag: F_d = 0.5 * rho * v^2 * Cd * A
- Gravity (g = 9.81 m/s^2, constant)

The equations of motion are solved with numerical integration over small time steps (Euler / ode45).

## Requirements

- MATLAB R2020b or newer
- App Designer (comes bundled with MATLAB)
- No extra toolboxes needed unless noted otherwise in the code

## How to run

1. Clone or download this repo.
2. Open the folder in MATLAB.
3. Open the `.mlapp` file, it launches in App Designer.
4. Fill in rocket/motor parameters in the GUI.
5. Hit the simulate button.
6. Check the plots and the apogee/flight time output.

## Why this exists

Made for quick pre-design estimates of model rocket performance before committing to a motor or airframe geometry, mainly for use within SİMURG Roket Takımı. Not validated against real flight data, so treat numbers as rough estimates, not certainties.

## License

Apache License 2.0, see [LICENSE](LICENSE).
