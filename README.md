# Landmark Observation Model

Range-only landmark observation likelihoods over a 2D grid map. The implementation computes single-beacon likelihood maps and joint likelihoods for multiple beacons with independent Gaussian measurement noise.

## Run

```bash
python - <<'PY'
import numpy as np
from ex4 import joint_observation_likelihood

grid = np.zeros((20, 20))
beacons = np.array([[6, 2], [8, 18], [16, 8]])
z = np.array([10, 5, 9])
sigma = np.array([1, 5, 3])

likelihood = joint_observation_likelihood(z, sigma, beacons, grid)
print(likelihood.shape, likelihood.max())
PY
```
