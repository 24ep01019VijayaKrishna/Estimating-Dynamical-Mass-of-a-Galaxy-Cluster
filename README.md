# Estimating-Dynamical-Mass-of-a-Galaxy-Cluster
Estimating the dynamical mass of a galaxy cluster using SDSS spectroscopic data by analyzing galaxy redshifts, velocity dispersion, and cluster size. The virial theorem is applied to determine the cluster's total mass and compare it with luminous mass, highlighting the presence of dark matter.

## Project Overview

Galaxy clusters are the largest gravitationally bound structures in the universe.  
By studying the velocities and spatial distribution of galaxies within a cluster, we can estimate the cluster's total mass, including the contribution from **dark matter**.

This project performs the following steps:

1. Identify cluster members using **redshift dispersion (3σ cut)**.
2. Compute the **mean cluster redshift**.
3. Calculate **galaxy velocities and velocity dispersion**.
4. Estimate the **physical size of the cluster**.
5. Apply the **virial theorem** to estimate the cluster's dynamical mass.
6. Compare **dynamical mass vs luminous mass** to infer dark matter content.

---

## Dataset

The dataset was obtained from the **SDSS SkyServer** database and contains:

- Galaxy coordinates (RA, Dec)
- Spectroscopic redshift (`specz`)
- Photometric redshift (`photoz`)
- Apparent magnitudes (u, g, r bands)
- Projected separation from cluster center

Number of galaxies analyzed: **~92**

---

## Methodology

### 1. Cluster Member Identification

Cluster members are selected using a **3σ redshift cutoff**:

$$
z \in [\bar{z} - 3\sigma, \bar{z} + 3\sigma]
$$

This removes foreground and background galaxies.

---

### 2. Velocity Calculation

Galaxy recession velocity is calculated from redshift:

$$
v = cz
$$

Relative velocity with respect to the cluster is computed using the **relativistic Doppler formula**.

---

### 3. Velocity Dispersion

Velocity dispersion measures how fast galaxies move relative to the cluster center:

$$
\sigma = std(v)
$$

This is an important indicator of the cluster's gravitational potential.

---

### 4. Cluster Size

The cluster diameter is estimated from the maximum angular separation:

$$
D = D_A \times \theta
$$

where


- $D_A$ = angular diameter distance 
- $\theta$ = angular separation in radians 

---

### 5. Dynamical Mass (Virial Theorem)

The total cluster mass is estimated using:

$$
M = \frac{3\sigma^2R}{G}
$$

where

- $\sigma$ = velocity dispersion
- $R$ = cluster radius
- $G$ = gravitational constant

---

## Results

| Parameter | Value |
|----------|------|
| Mean Cluster Redshift | 0.08003 |
| Velocity Dispersion | 1203 km/s |
| Cluster Diameter | 0.891 Mpc |
| Dynamical Mass | 4.50 × 10¹⁴ M☉ |
| Luminous Mass | 1.31 × 10¹³ M☉ |
| Mass Ratio (M_dyn / M_lum) | ~34 |

The large mass ratio indicates the **dominance of dark matter** in galaxy clusters.

---

## Visualizations

The project includes several plots:

- Redshift distribution histogram
- Galaxy velocity distribution
- Angular separation distribution

These plots help visualize cluster membership and spatial structure.

---

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Astropy
- Jupyter Notebook

---

## Installation

Clone the repository:

```bash
git clone https://github.com/24ep01019VijayaKrishna/Estimating-Dynamical-Mass-of-a-Galaxy-Cluster
