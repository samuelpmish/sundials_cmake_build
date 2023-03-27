## Building and Running examples

1. Get the sources:

```
$ git clone https://github.com/samuelpmish/sundials_cmake_build.git
```

2. Configure CMake (this will fetch sundials and integrate it into the CMake build):

```
$ cd sundials_cmake_build
sundials_cmake_build$ cmake . -Bbuild
```

3. Build

```
sundials_cmake_build$ cd build && make -j
```

4. Run Examples

```
sundials_cmake_build/build$ ./kinsol_ex
nni = 8
Jac nni = 8

   Index                     J DQ                   J true      absolute difference      relative difference
------------------------------------------------------------------------------------------------------------
       0    3.000000000000000e+00    3.000000000000000e+00    0.000000000000000e+00    0.000000000000000e+00
       1    9.962893873453140e-01    9.962893692575923e-01    1.808772176481455e-08    1.815508859468512e-08
       2    2.204735279083252e-01    2.204735027468027e-01    2.516152244891323e-08    1.141249271927672e-07
       3   -5.571749806404114e-02   -5.571756320875725e-02    6.514471611457351e-08   -1.169195355340568e-06
       4    1.613615968823433e+01    1.613615515450222e+01    4.533732113287670e-06    2.809673103584837e-07
       5   -5.502227544784546e-01   -5.502227423498225e-01    1.212863209865134e-08   -2.204313119965542e-08
       6   -2.103064954280853e-02   -2.103065042929854e-02    8.864900029326162e-10   -4.215228653592263e-08
       7    8.634001463651657e-01    8.633999867018508e-01    1.596633149025806e-07    1.849239255984787e-07
       8    2.000000000000000e+01    2.000000000000000e+01    0.000000000000000e+00    0.000000000000000e+00
       
sundials_cmake_build/build$ ./cvodes_ex

Particle traveling on the unit circle example
---------------------------------------------
alpha      = 1.0000e+00
num orbits = 100
---------------------------------------------
rtol       = 0.0001
atol       = 1e-09
proj sol   = 1
proj err   = 0
nout       = 0
tstop      = 0
---------------------------------------------

     t            x              y             err x          err y       err constr
0.0000e+00   1.000000e+00   0.000000e+00   0.000000e+00   0.000000e+00   0.000000e+00
6.2832e+02   9.979545e-01   6.392827e-02  -2.045504e-03   6.392827e-02   0.000000e+00

Integration Statistics:
Number of steps taken = 4131  
Number of function evaluations = 6030  
Number of linear solver setups = 862   
Number of Jacobian evaluations = 115   
Number of nonlinear solver iterations = 6027  
Number of convergence failures = 52    
Number of error test failures = 343 
```

