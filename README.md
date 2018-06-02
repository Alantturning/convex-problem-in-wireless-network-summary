# convex-problem-in-wireless-network-summary
A review after graduate design about the scenario and particular solution where convex method is called for communication system
  
  在无线网络的通信系统中，无线网络的功耗管理与最大最小数据速率管理都会归结为一种范数约束问题。 
  
  这些范数的目标问题往往具备直接或者间接的凸性，而依据目前的研究现状来看，由于凸问题的求解工具与算法发展已经比较成熟，现有的解决办法往往是通过将问题的模型直接表示成凸问题的形式或者是将问题间接地转化成凸问题，比如说1.通过将问题直接解耦，使得问题分解为两个子的凸问题进而便于问题的求解2.或者利用凸松弛的方法，将原始问题松弛到一个凸的问题而且保证问题的最优解不变（这种方法往往将问题的约束变形成为范数的平方，作为罚函数作为目标函数的余项）。
  
  现有的凸优化求解工具包已经发展相对成熟，SDPT3，SeDuMi都是基于内点法的凸优化求解工具包，针对规模有限的问题能够方便的求得解析解，Mosek是一种商业的工具包，相比于前两种工具包具备更快的求解性能(但是)，SCS( (alternative direction method of multipler)ADMM，一种交替方向的乘子分裂法的求解器)这种算法牺牲了问题求解的精度，但是大大加速了针对大规模问题求解的速度，这对于未来网络的密集型结构的资源管理具备很好的适用性。
