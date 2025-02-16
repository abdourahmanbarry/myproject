Notation: $I_{a,b}$ represents the current flowing into Bus b from the branch connecting Bus a and Bus b, $I_{G,a}$ the current from generator a, $I_{L,a}$ the current from load a, and $V_a$ the voltage at Bus a.

## Bus equations:
```math 
I_{G,1}+I_{2,1}+I_{3,1}+I_{L,1} = 0
```
```math
I_{L,2}+I_{1,2}+I_{3,2} = 0
```
```math 
I_{G,3}+I_{1,3}+I_{2,3} = 0
```

## Branch equations:

(branch connecting Bus 1 and Bus 2)
```math
\left[ \begin{array}{c}
        I_{2,1} \\
        I_{1,2}
    \end{array}\right] = 
    Y^{[1]}\left[ \begin{array}{c}
        V_1 \\
        V_2
\end{array}\right]
```

(branch connecting Bus 2 and Bus 3)
```math
\left[ \begin{array}{c}
        I_{3,2} \\
        I_{2,3}
    \end{array}\right] = 
    Y^{[2]}\left[ \begin{array}{c}
        V_2 \\
        V_3
    \end{array}\right]
```

(branch connecting Bus 1 and Bus 3)
```math
\left[ \begin{array}{c}
        I_{3,1} \\
        I_{1,3}
    \end{array}\right] = 
    Y^{[3]}\left[ \begin{array}{c}
        V_1 \\
        V_3
    \end{array}\right]
```

 ## Load equations:
```math
 I_{L,1} = \frac{V_1}{R_1} 
``` 
```math
    I_{L,2} = \frac{V_2}{R_2}
```

## Generator 1
Differential equations: <br>
$$\dot{\delta} = \omega \cdot \omega_0 $$ <br>
$$\dot{\omega} = \frac{1}{2H}\left( \frac{P_{mech} - D\omega}{1+\omega} - T_{elec}\right) $$ <br>
$$\dot{E_{qp}} = \frac{1}{T_{dop}}\left(  E_{fd} - \left( E_{qp} + X_{d1}\left( I_d + X_{d3}\left( E_{qp} - \psi_{dp} - X_{d2}I_d \right)  \right) + \psi_{dpp}\cdot k_{sat} \right) \right)$$ <br>
```math \dot{\psi}_{dp} = \frac{1}{T_{dopp}} \left( E_{qp} - \psi_{dp} - X_{d2} I_d \right) ``` <br>
$$\dot{\psi}_{qp} = \frac{1}{T_{qopp}} \left( E_{qp} - \psi_{dp} - X_{d2}I_d\right)$$ <br>
$$\dot{E}_{dp} = \frac{1}{T_{qop}}\left(-E_{dp} + X_{qd}\psi_{qpp} + X_{q1} \left(I_q - X_{q3} \left(E_{dp} + I_qX_{q2} - \psi_{qp}\right)\right)\right)$$

Algebraic equations:
```math
V_d = -\psi_{qpp}(\psi_{qp^{\prime}}E_{dp})(1+\omega)
```<br>
```math
V_q = -\psi_{dpp}(\psi_{dp^{\prime}}E_{qp})(1+\omega)
```
```math
I_d = I_r\sin\,\sin(\delta) - I_i\cos\,\cos(\delta)
```
```math
I_q = I_r\cos\,\cos(\delta) + I_i\sin(\delta)
```
```math
V_d = V_r\sin\,\sin(\delta) - V_i\cos\,\cos(\delta) - (I_d R_a  -I_q X_{qpp})
```
```math
V_q = V_r\cos\,\cos(\delta) + V_i\sin(\delta) + I_{d}X_{qpp} + I_{q}R_a
```


