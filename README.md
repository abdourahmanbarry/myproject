Notation: $I_{a,b}$ represents the current flowing into Bus b from the branch connecting Bus a and Bus b, $I_{G,a}$ the current from generator a, $I_{L,a}$ the current from load a, and $V_a$ the voltage at Bus a.

Bus equations:
$$I_{G,1}+I_{2,1}+I_{3,1}+L_{L,1} = 0$$
$$I_{L,2}+I_{1,2}+I_{3,2} = 0$$
$$I_{G,3}+I_{1,3}+I_{2,3} = 0$$

Branch equations:
(branch connecting Bus 1 and Bus 2)
$\left[ \begin{array}{c}
        I_{2,1} \\
        I_{1,2}
    \end{array}\right] = 
    Y^{[1]}\left[ \begin{array}{c}
        V_1 \\
        V_2
\end{array}\right]$

(branch connecting Bus 2 and Bus 3)
$$\left[ \begin{array}{c}
        I_{3,2} \\
        I_{2,3}
    \end{array}\right] = 
    Y^{[1]}\left[ \begin{array}{c}
        V_2 \\
        V_3
    \end{array}\right]$$

(branch connecting Bus 1 and Bus 3)
$$\left[ \begin{array}{c}
        I_{3,1} \\
        I_{1,3}
    \end{array}\right] = 
    Y^{[1]}\left[ \begin{array}{c}
        V_1 \\
        V_3
    \end{array}\right]$$

    Load equations:
    $$L_{L,1} = \frac{V_1}{R_1} \quad \text{and} \quad I_{L,2} = \frac{V_2}{R_2}$$
