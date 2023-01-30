# variable-renewable-energy-process

Collection of tools to process and interact with variable renewable energy data.

## Data sources

Historical data: <https://power.larc.nasa.gov/data-access-viewer/>

Photovoltaic GIS map: <https://globalsolaratlas.info/>

Wind GIS map: <https://globalwindatlas.info/>

NOTE:

1. Use Mean Power Density instead of Mean Wind Speed in locating the best wind location.

## Photovoltaic

### Photovoltaic Equations

#### Photovoltaic energy output

$$
E = A * r * GHI * \mu
$$

where,

$E$ = Energy (Wh)

$A$ = Total solar panel area (m<sup>2</sup>)

$r$ = Solar panel efficiency (default value = 0.159) [[1]][Osama Ayadi, 2022]

$GHI$ = Global Horizontal Irradiation (Wh / m<sup>2</sup>)

$\mu$ = Inverter efficiency (range between 0.92 and 0.99, default value 0.96) [[2]][Aron P. Dobos, 2014]

#### Photovoltaic power output

$$
P = E / \Delta t
$$

where,

$P$ = Solar panel power output (W)

$E$ = Energy (Wh)

$\Delta t$ = Time step (hour)

#### Photovoltaic per unit output

$$
\begin{aligned}
cf &= P / \bar{P}
\\
   &= \frac{A * r * GHI * \mu}{\Delta t * \bar{P}}
\\
   &= GHI * \frac{A * r * \mu}{\Delta t * \bar{P}}
\\
   &= GHI * K
\\
K  &= \frac{A * r * \mu}{\Delta t * \bar{P}}
\end{aligned}
$$

where,

$cf$ = Capacity factor (p.u.)

$P$ = Solar panel power output (W)

$\bar{P}$ = Maximum power output of the installed solar panel (Wp)

$A$ = Total solar panel area (m<sup>2</sup>)

$r$ = Solar panel efficiency (default value = 0.159) [[1]][Osama Ayadi, 2022]

$GHI$ = Global Horizontal Irradiation (Wh / m<sup>2</sup>)

$\mu$ = Inverter efficiency (range between 0.92 and 0.99, default value 0.96) [[2]][Aron P. Dobos, 2014]

$\Delta t$ = Time step (hour)

$K$ = Coefficient factor constant (constant parameter based on solar panel m<sup>2</sup>/Wh)

### Photovoltaic Typical Value

| Symbol    | Value         | Unit              | Note                                  |
| --------- | ------------- | ------------------| ------------------------------------- |
| $A$       | 1.63350       | m<sup>2</sup>     | [[1]][Osama Ayadi, 2022]              |
| $r$       | 0.159         | -                 | [[1]][Osama Ayadi, 2022]              |
| $\mu$     | 0.96          | -                 | [[2]][Aron P. Dobos, 2014]            |
| $\bar{P}$ | 260           | W                 | [[1]][Osama Ayadi, 2022]              |
| $K$       | 0.000979      | m<sup>2</sup>/Wh  | -                                     |

[Osama Ayadi, 2022]: https://doi.org/10.1016/j.egyr.2022.06.121
[Aron P. Dobos, 2014]: https://www.nrel.gov/docs/fy14osti/62641.pdf

## Wind

### Wind Equations

1. Wind power output

...

### Wind Typical Value

| Symbol    | Value         | Unit              | Note                                  |
| --------- | ------------- | ------------------| ------------------------------------- |
|           |               |                   |                                       |

## Contributing

1. Git FIlter

    We use [`nb-clean`](https://github.com/srstevenson/nb-clean) to clean notebooks metadata.

    ```shell
    pip install nb-clean
    nb-clean add-filter --preserve-cell-outputs
    ```

1. Render README.md

    The README.md can be rendered using `pandoc README.md -o README.pdf`
