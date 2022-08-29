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

    $r$ = Solar panel efficiency (default value = 0.2)[<sup>1</sup>](https://www.energy.gov/eere/solar/crystalline-silicon-photovoltaics-research)

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

<!-- TODO: how to get installed capacity -->
<!-- TODO: read https://www.sciencedirect.com/science/article/pii/S2352484722012288 -->

1. Solar per unit output

    $$
    cf = P / \bar{P}
    $$

    where,

    $cf$ = Capacity factor (p.u.)

    $P$ = Solar panel power output (W)

    $\bar{P}$ = Maximum power output of the installed solar panel (Wp)
