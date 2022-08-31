# variable-renewable-energy-process

Collection of tools to process and interact with variable renewable energy data

## Photovoltaic

1. Solar energy output

    $$
    E = A * r * GHI * \mu
    $$

    where,

    $E$ = Energy (Wh)

    $A$ = Total solar panel area (m<sup>2</sup>)

    $r$ = Solar panel efficiency (default value = 0.159) [[1]][Osama Ayadi, 2022]

    $GHI$ = Global Horizontal Irradiation (Wh / m<sup>2</sup>)

    $\mu$ = Coefficient for losses (range between 0.5 and 0.9, default value = 0.9)

1. Solar power output

    $$
    P = E / \Delta t
    $$

    where,

    $P$ = Solar panel power output (W)

    $E$ = Energy (Wh)

    $\Delta t$ = Time step (hour)

1. Solar per unit output

    $$
    \begin{aligned}
    cf &= P / \bar{P}
    \\
    &= \frac{A * r * GHI * \mu}{\Delta t * \bar{P}}
    \end{aligned}
    $$

    where,

    $cf$ = Capacity factor (p.u.)

    $P$ = Solar panel power output (W)

    $\bar{P}$ = Maximum power output of the installed solar panel (Wp)

    $A$ = Total solar panel area (m<sup>2</sup>)

    $r$ = Solar panel efficiency (default value = 0.159) [[1]][Osama Ayadi, 2022]

    $GHI$ = Global Horizontal Irradiation (Wh / m<sup>2</sup>)

    $\mu$ = Coefficient for losses (range between 0.5 and 0.9, default value = 0.9)

    $\Delta t$ = Time step (hour)

## Typical Value

| Symbol    | Value         | Unit          | Note                                  |
| --------- | ------------- | --------------| ------------------------------------- |
| $A$       | 1.63350       | m<sup>2</sup> | [[1]][Osama Ayadi, 2022]              |
| $r$       | 0.159         | -             | [[1]][Osama Ayadi, 2022]              |
| $\mu$     | 0.90          | -             | -                                     |
| $\bar{P}$ | 260           | W             | [[1]][Osama Ayadi, 2022]              |

[Osama Ayadi, 2022]: https://doi.org/10.1016/j.egyr.2022.06.12

<!-- NOTE: this markdown can be rendered using `pandoc README.md -o README.pdf`-->
