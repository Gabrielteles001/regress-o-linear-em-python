# Regressão linear em python
import numpy as np
import matplotlib.pyplot as plt
from scipy.stats import linregress

# Dados
x = np.array(
    [0, 4, 7, 7, 11, 18, 24, 30, 32, 43, 46, 60, 64, 70, 71, 71, 73, 74, 84, 88, 95, 102, 106, 109, 115, 122, 133, 137,
     140, 143, 147, 148, 149, 150, 153, 156, 161, 165, 165, 170, 173, 176, 179, 198, 214, 218, 221, 225, 233, 238, 241, 246])
y = np.array(
    [184.35, 182.51, 180.45, 179.91, 177.91, 175.81, 173.11, 170.06, 169.31, 165.10, 163.11, 158.30, 155.80, 154.31,
     153.86, 154.20, 152.20, 152.80, 150.30, 147.80, 146.10, 145.60, 142.50, 142.30, 139.40, 137.90, 133.70, 133.70,
     133.30, 131.20, 133.00, 132.20, 130.80, 131.30, 129.00, 127.90, 126.90, 127.70, 129.50, 128.40, 125.40, 124.90,
     124.90, 118.20, 118.20, 115.30, 115.70, 116.00, 115.50, 112.60, 114.00, 112.60])

# Ajuste da reta de regressão
slope, intercept, r_value, p_value, std_err = linregress(x, y)
line = slope * x + intercept

# Plotagem dos dados e da linha de regressão
plt.scatter(x, y, label='Dados')
plt.plot(x, line, color='red', label='Regressão Linear')

plt.xlabel('X')
plt.ylabel('Y')
plt.title('Gráfico de Regressão Linear')
plt.legend()

plt.show()
