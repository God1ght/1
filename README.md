- [> 简介](#-简介)
- [> 线性化模型](#-线性化模型)
- [> 故障类型](#-故障类型)
- [> 结果展示](#-结果展示)
- [> My blog](#-my-blog)
- [> 参考文献](#-参考文献)
- [> Paper](#-paper)

## > 简介

​	> 仿真软件版本信息: Matlab R2020b

​	A three-tank system, as sketched in Fig. 1, has typical characteristics of tanks, pipelines and pumps used in chemical industry and thus often serves as a benchmark process in laboratories for process control. The model and the parameters of the three-tank system introduced here are from the laboratory setup DTS200.

<div align=center>
<img src="https://github.com/zhuofupan/Three-Tank-System/blob/main/TTS.jpg?raw=true" alt="Fig.1：TTS" style="zoom:30%;" />
</div>

Applying the incoming and outgoing mass flows under consideration of Torricelli’s law, the dynamics of DTS200 is modeled by




<div align=center>

$$ {}
\begin{equation}
    \begin{split}
        &\mathcal A\dot{h_1}=Q_1-Q_{13},\mathcal A\dot{h_2}=Q_2+Q_{32}-Q_{20},\mathcal A\dot{h_3}=Q_{13}-Q_{32}\\
        &Q_{13}=a_1s_{13}sign(h_1-h_3)\sqrt{2g|h_1-h_3|}  \\
        &Q_{32}=a_3s_{23}sign(h_3-h_2)\sqrt{2g|h_3-h_2|},Q_{20}=a_2s_0\sqrt{2gh_2}  \\
    \end{split}
\end{equation}
$$

</div>

## > 线性化模型



## > 故障类型

<div align=center>

$$ {}
\begin{equation}
    \begin{split}
        &\mathcal{A} \dot{h}_1 = Q_1 + f_1 + f_2 -  Q_{13} - f_7 \check Q_{10} + \omega_1\\
        &\mathcal{A} \dot{h}_2 = Q_2 + f_1 + f_3 + Q_{32} - f_8 (f_{11}+1) \check Q_{20} + \omega_2 \\
        &\mathcal{A} \dot{h}_3 = Q_{13} -  Q_{32} - f_9 \check Q_{30} + \omega_3\\ 
        &Q_{13} =  a_1 s_{13} (f_{10}+1) sign(h_1-h_3) \sqrt{2g \left| h_1 - h_3 \right| } \\
        &Q_{32} =  a_3 s_{23} (f_{12}+1) sign(h_3-h_2) \sqrt{2g \left| h_3 - h_2 \right| } \\
        &\check Q_{i0} =  a_i s_{0} \sqrt{2g h_i }, i = 1,2,3
    \end{split}
\end{equation}
$$
  
</div>

<div align=center>

| Fault ID |                         Description                          | Location |
| :------: | :----------------------------------------------------------: | :------: |
|    1     |             $f_1(t) =  6 \sin\frac{t-200}{6\pi}$             | Actuator |
|    2     |                   $f_2(t) =  0.02(t-200)$                    | Actuator |
|    3     | $f_3(t) = 0.005(t-200) + (-1)^{ \left\lfloor \frac{t}{48} \right\rfloor - \left\lfloor \frac{t}{60} \right\rfloor }$ | Actuator |
|    4     |                   $f_4(t) = -0.005(t-200)$                   |  Sensor  |
|    5     |                   $f_5(t) = 0.005(t-200)$                    |  Sensor  |
|    6     |                   $f_6(t) = 0.008(t-200)$                    |  Sensor  |
|  7,8,9   |          $f_7(t) =f_8(t) =f_9(t) = 0.00005 (t-200)$          | Process  |
|    10    |                 $f_{10}(t) =-0.0002(t-200)$                  | Process  |
|    11    |                 $f_{11}(t) =-0.0003(t-200)$                  | Process  |
|    12    |                 $f_{12}(t) =-0.0005(t-200)$                  | Process  |

</div>


## > 结果展示



## > My blog

[ResearchGate](https://www.researchgate.net/profile/Zhuofu-Pan), [知乎](https://www.zhihu.com/people/fu-zi-36-41/posts), [CSDN](https://blog.csdn.net/fuzimango/article/list/)

QQ群：640571839

## > 参考文献



## > Paper

希望大家多支持支持我们的工作，欢迎交流探讨~
