---
title: idle1 obsolete ex data
layout: default
---

This information describe EX before the October 2026 update.
It is now obsolete.

### Formula for POW $\rightarrow$ EX

Total POW consists of what the creation screen calls "POW" and "IDLE",
which are sometimes referred to as "normal POW" and "idle POW".
Total POW is also sometimes (confusingly) referred to as just "POW".

When you do a nuclear reset, both forms of POW are converted to EX.
The sum is all that matters, so there is no need to switch it
to/from idle POW.  Both forms of POW then go back to their initial
values of 1.  With low values of EX, world 1 won't go much faster than
the initial slog through it.

The formula for EX is as follows.
The $\lfloor x\rfloor$ notation means to round down.

$$\text{EX}_\text{gain} =
  0.04 + \left(0.01 *
  \left\lfloor\frac{\text{pow}_\text{total}}{2}\right\rfloor\right)$$

This includes the 2 total POW that you start with
(1 normal POW and 1 idle POW).
This means that if you beat W1-W7 with no earned POW, you get 0.05 EX
since you have the initial 2 total POW.
If you want the formula to start with the 0.05 value,
then you need to subtract those 2 initial total POW,
so the formula can also be written as follows:

$$\begin{aligned}\text{EX}_\text{gain} &=
  0.05 + \left(0.01 *
  \left\lfloor\dfrac{(\text{pow}_\text{total}-2)}{2}\right\rfloor\right)\\
  &=0.05 + \left(0.01 *
  \left\lfloor\dfrac{\text{pow}_\text{earned}}{2}\right\rfloor\right)\\ \end{aligned}$$

The rounding means that each 2 total POW yields 0.01 EX,
and the POW in between those points has no effect.
However, for unknown reasons, sometimes the EX value goes up a bit late.
The community has seen 0.08 EX occur at 8.5 total POW$^*$ instead of 8
and 0.15 EX occur at 22.5 total POW$^{**}$ instead of 22.

The following is a chart of some conversion values.
Different measures of POW are included.
POW$\_{\text{normal}}$ assumes an POW$\_{\text{idle}}$ value of 1.
Therefore, the different POWs are related by a simple relationship:

$\text{POW}\_{\text{total}}
  =\text{POW}\_{\text{normal}}+1
  =\text{POW}\_{\text{earned}}+2$

{: .column-table .quad-column-table}

| POW$_\text{total}$  |    2 |    4 |    6 | 8.5$^*$ |   10 |   12 |   14 |   16 |   18 |   20 | 22.5$^{**}$ |
| POW$_\text{normal}$ |    1 |    3 |    5 | 7.5$^*$ |    9 |   11 |   13 |   15 |   17 |   19 | 21.5$^{**}$ |
| POW$_\text{earned}$ |    0 |    2 |    4 | 6.5$^*$ |    8 |   10 |   12 |   14 |   16 |   18 | 20.5$^{**}$ |
| EX                  | 0.05 | 0.06 | 0.07 |    0.08 | 0.09 | 0.10 | 0.11 | 0.12 | 0.13 | 0.14 | 0.15 |
| POW$_\text{total}$  |   32 |   42 |   52 |      62 |   72 |   82 |   92 |  192 |  292 |  392 |  492 |
| POW$_\text{normal}$ |   31 |   41 |   51 |      61 |   71 |   81 |   91 |  191 |  291 |  391 |  491 |
| POW$_\text{earned}$ |   30 |   40 |   50 |      60 |   70 |   80 |   90 |  190 |  290 |  390 |  490 |
| EX                  | 0.20 | 0.25 | 0.30 |    0.35 | 0.40 | 0.45 | 0.50 | 1.00 | 1.50 | 2.00 | 2.50 |

### 8/10/26

EX provides a small fixed bonus to each color.  It increases as EX goes up but is not impacted by any multipliers.  It starts at 1 for each 0.5 EX, rounded up (so +1 for 0.05 to 0.50, +2 for 0.51 to 1.0, +3 for 1.01 to 1.5, and so on).  However, at 9.05 EX it gives an extra +2 instead of +1, so the bonus is +18 instead of +17.  After that, the increases occur on each half point of EX rather than after them, and the amounts of the increases continue to go up.  In table form:

{: .right-table .double-third-table}

|  Displayed EX | Bonus | Added |  Displayed EX | Bonus | Added |
| ------------: | ----: | ----: | ------------: | ----: | ----: |
|          1.00 |    +0 |     - | 13.50 - 13.99 |   +80 |   +12 |
|  1.05 -  1.50 |    +1 |    +1 | 14.00 - 14.49 |   +95 |   +15 |
|  1.51 -  2.00 |    +2 |    +1 | 14.50 - 14.99 |  +112 |   +17 |
|  2.01 -  2.50 |    +3 |    +1 | 15.00 - 15.49 |  +131 |   +19 |
|           ... |   ... |   ... | 15.50 - 15.99 |  +152 |   +21 |
|  7.51 -  8.00 |   +14 |    +1 | 16.00 - 16.49 |  +176 |   +24 |
|  8.01 -  8.50 |   +15 |    +1 | 16.50 - 16.99 |  +203 |   +27 |
|  8.51 -  9.00 |   +16 |    +1 | 17.00 - 17.49 |  +233 |   +30 |
|  9.01 -  9.49 |   +18 |    +2 | 17.50 - 17.99 |  +265 |   +32 |
|  9.50 -  9.99 |   +21 |    +3 | 18.00 - 18.49 |  +301 |   +36 |
| 10.00 - 10.49 |   +24 |    +3 | 18.50 - 18.99 |  +340 |   +39 |
| 10.50 - 10.99 |   +28 |    +4 | 19.00 - 19.49 |  +382 |   +42 |
| 11.00 - 11.49 |   +33 |    +5 | 19.50 - 19.99 |  +428 |   +46 |
| 11.50 - 11.99 |   +40 |    +7 | 20.00 - 20.49 |  +478 |   +50 |
| 12.00 - 12.49 |   +48 |    +8 | 20.50 - 20.99 |  +532 |   +54 |
| 12.50 - 12.99 |   +57 |    +9 | 21.00 - 21.49 |  +589 |   +57 |
| 13.00 - 13.49 |   +68 |   +11 | 21.50 - ????? |  +651 |   +62 |

To be clear about the fixed nature of the bonus, here is what the income for each tick of C1 looks like (with no earn or speed bonuses).  10 is where the first levelup bonus appears (and is 3x):

{: .right-table}

|    # C1 | 1 EX | 1.2 EX | 10 EX |
| ------: | ---: | -----: | ----: |
|       1 |    4 |      5 |    28 |
|       2 |    8 |      9 |    32 |
|       3 |   12 |     13 |    36 |
|     ... |  ... |    ... |   ... |
|       9 |   36 |     37 |    60 |
| (3x) 10 |  120 |    121 |   144 |
|      11 |  132 |    133 |   156 |

The EX fixed bonus makes buying C1s faster.  We can describe this by
writing the number of C1s after doing a "buy all" after each tick.  With no EX, W1 goes $1 \rightarrow 2 \rightarrow 3 \rightarrow 5 \rightarrow 8 \rightarrow 10$ (5 ticks).  After an initial small EX reset, it changes to $1 \rightarrow 2 \rightarrow 4 \rightarrow 6 \rightarrow 9 \rightarrow 11$.  The effect is minor as it still takes 5 ticks.  At 2.01 EX, it shortens to $1 \rightarrow 2 \rightarrow 4 \rightarrow 7 \rightarrow 10$ (4 ticks), which saves 4+ seconds.  At 5.01 EX, it shortens to $1 \rightarrow 3 \rightarrow 6 \rightarrow 10$ (3 ticks).  At 10 EX, it shortens to $1 \rightarrow 6 \rightarrow 10$ (2 ticks).

### 8/15/26

Here is a chart that shows which EX values reduce the number of ticks required to get C1 to a count of 10.  See the table above explaining C1 costs to determine the base cost for a particular world.

{: .right-table}

|   Base |   EX | Bonus | Ticks | Path |
| -----: | ---: | ----: | ----: | :--- |
|      2 |    1 |    +0 |     4 | $1 \rightarrow 2 \rightarrow 4 \rightarrow 7 \rightarrow 11$ |
|        | 1.51 |    +2 |     3 | $1 \rightarrow 3 \rightarrow 6 \rightarrow 10$ |
|        | 6.01 |   +11 |     2 | $1 \rightarrow 5 \rightarrow 10$ |
|        |   12 |   +48 |     1 | $1 \rightarrow 10$ |
| 3 (W1) |    1 |    +0 |     5 | $1 \rightarrow 2 \rightarrow 3 \rightarrow 5 \rightarrow 8 \rightarrow 10$ |
|        | 2.01 |    +3 |     4 | $1 \rightarrow 2 \rightarrow 4 \rightarrow 7 \rightarrow 10$ |
|        | 5.01 |    +9 |     3 | $1 \rightarrow 3 \rightarrow 6 \rightarrow 10$ |
|        |   10 |   +24 |     2 | $1 \rightarrow 6 \rightarrow 10$ |
|        |   13 |   +68 |     1 | $1 \rightarrow 10$ |
|      4 |    1 |    +0 |     7 | $1 \rightarrow 1 \rightarrow 2 \rightarrow 3 \rightarrow 5 \rightarrow 7 \rightarrow 9 \rightarrow 11$ |
|        | 1.05 |    +1 |     6 | $1 \rightarrow 1 \rightarrow 2 \rightarrow 4 \rightarrow 6 \rightarrow 8 \rightarrow 10$ |
|        | 2.51 |    +4 |     5 | $1 \rightarrow 2 \rightarrow 4 \rightarrow 6 \rightarrow 8 \rightarrow 10$ |
|        | 4.51 |    +8 |     4 | $1 \rightarrow 3 \rightarrow 5 \rightarrow 8 \rightarrow 10$ |
|        | 8.01 |   +15 |     3 | $1 \rightarrow 4 \rightarrow 7 \rightarrow 10$ |
|        |   11 |   +33 |     2 | $1 \rightarrow 6 \rightarrow 10$ |
|        |   14 |   +95 |     1 | $1 \rightarrow 10$ |

Here is a same chart that shows which EX values reduce the number of ticks required to get C1 to a count of 25, but only for W1 (and other worlds with a base cost of 3).  Note that this doesn't mean that building to 25 W1 is the best starting strategy; usually, C2 is a better path.

{: .right-table}

|   Base |   EX | Bonus | Ticks | Path |
| -----: | ---: | ----: | ----: | :--- |
| 3 (W1) |    1 |    +0 |     9 | $1 \rightarrow 2 \rightarrow 3 \rightarrow 5 \rightarrow 8 \rightarrow 10 \rightarrow 16 \rightarrow 20 \rightarrow 23 \rightarrow 26$ |
|        | 2.01 |    +3 |     8 | $1 \rightarrow 2 \rightarrow 4 \rightarrow 7 \rightarrow 10 \rightarrow 16 \rightarrow 20 \rightarrow 23 \rightarrow 26$ |
|        | 4.51 |    +8 |     7 | $1 \rightarrow 3 \rightarrow 6 \rightarrow 9 \rightarrow 12 \rightarrow 18 \rightarrow 22 \rightarrow 25$ |
|        | 8.01 |   +15 |     6 | $1 \rightarrow 4 \rightarrow 8 \rightarrow 12 \rightarrow 17 \rightarrow 22 \rightarrow 25$ |
|        | 10.5 |   +28 |     5 | $1 \rightarrow 6 \rightarrow 11 \rightarrow 17 \rightarrow 22 \rightarrow 25$ |
|        |   13 |   +68 |     4 | $1 \rightarrow 10 \rightarrow 18 \rightarrow 22 \rightarrow 26$ |
|        | 14.5 |  +112 |     3 | $1 \rightarrow 13 \rightarrow 20 \rightarrow 25$ |
|        | 17.5 |  +256 |     2 | $1 \rightarrow 18 \rightarrow 25$ |
|        |    ? |  +727 |     1 | $1 \rightarrow 25$ |

Here is a chart to 10 C1 for higher bases, but it only has the EX values that shorten the path in order to keep the table smaller.  For example, with no EX, it takes 10 ticks of buying all to get to 10 C1s.  At 1.05 EX, it drops to 9.  At 1.51 EX, it drops to 8, and so on, until at 15 EX, one tick is enough.

{: .right-table}

| Base | Initial Ticks | EX cutoffs |      |      |      |      |      |
| ---: | ------------: | ---------: | ---: | ---: | ---: | ---: | ---: |
|    6 |            10 |       1.05 | 1.51 | 2.51 | 3.51 | 5.51 | 9.01 |
|      |               |         11 | 12.5 |**15**|
|    7 |            11 |       1.05 | 1.51 | 2.51 | 3.51 | 5.51 | 8.01 |
|      |               |         10 |   12 |   13 |**15.5**|
|    8 |            12 |       1.05 | 2.01 | 2.51 | 4.01 | 4.51 | 7.01 |
|      |               |        9.5 | 10.5 |   12 | 13.5 |**16** |
|    9 |            13 |       1.05 | 1.51 | 2.51 | 3.51 | 4.51 | 6.01 |
|      |               |       8.51 |   10 |   11 | 12.5 |   14 |**16.5** |
|   10 |            15 |       1.05 | 1.05 | 2.01 | 2.01 | 3.01 | 5.01 |
|      |               |       5.51 | 7.51 |  9.5 | 10.5 | 11.5 |   13 |
|      |               |       14.5 |**17**|
|   12 |            17 |       1.05 | 1.51 | 2.01 | 2.51 | 3.01 | 4.01 |
|      |               |       5.01 | 6.51 | 8.51 |  9.5 | 10.5 | 11.5 |
|      |               |       12.5 | 13.5 |   15 |**17.5**|
|   18 |            25 |       1.05 | 1.05 | 1.51 | 2.01 | 2.01 | 2.51 |
|      |               |       3.01 | 3.51 | 4.01 | 4.51 | 5.51 | 6.51 |
|      |               |       8.01 | 9.01 |  9.5 | 10.5 |   11 | 11.5 |
|      |               |         12 |   13 |   14 |   15 | 16.5 |**19.5**|
|   20 |            28 |       1.05 | 1.05 | 1.51 | 1.51 | 2.01 | 2.01 |
|      |               |       2.51 | 3.01 | 3.51 | 4.01 | 4.51 | 5.51 |
|      |               |       6.01 | 7.01 | 8.01 | 9.01 |   10 |   10 |
|      |               |         11 | 11.5 |   12 | 12.5 | 13.5 |   14 |
|      |               |         15 |   17 |**20**|
