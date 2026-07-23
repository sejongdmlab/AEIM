# An Error-Adaptive Framework to Support Optimization in Intelligent Manufacturing Systems

This article provides executables of frameworks and datasets used in our research, "An Error-Adaptive Framework to Support Optimization in Intelligent Manufacturing Systems", for readers interested in our research.

The frameworks used in our experiments include 

The executables include the frameworks, such as AEIM, EPAS, DWEL*, and LUEID* and the datasets which are used in our experiment: QPMP, SIEC, Cosmetics, DataCo, and T10I4D200K—T10I4D1000K.

All executables were compiled to run on 64-bit architectures.

Please refer to the following guide:

1. Note that the name of the executable for each algorithm is as follows:

| Original Name   | AEIM | EPAS | DWEL* | LUEID* |
| --------------- | ---- | ---- | ----- | ------ |
| Executable Name | AEIM | EPAS | DWEL  | LUEID  |

2. The parameters of the executables are as follows:

 for AEIM and EPAS
```bash
[0]          [1]            [2]                     [3]                        [4]                      [5]
[Executable] [MGT Ratio(%)] [Approximate Factor(%)] [Erasable Data Path(.dat)] [Original Data Ratio(%)] [Total Number of Original and Stream Data]
```

for DWEL* and LUEID*
```bash
[0]          [1]            [2]                        [3]                      [4]
[Executable] [MGT Ratio(%)] [Erasable Data Path(.dat)] [Original Data Ratio(%)] [Total Number of Original and Stream Data]
```

3. Next, the file name and the parameters of each dataset are as follows:

|  Dataset  | Database Size     | Number of Items | Average Transaction Length |
| --------- | ----------------- | --------------- | -------------------------- |
| QPMP      | 737,453           | 206             | 23.0                       |
| SIEC      | 35,039            | 68              | 8.0                        |
| Cosmetics | 114,635           | 68,604          | 12.8                       |
| DataCo    | 172,933           | 4,441           | 18.0                       |
| T10I4DxK  | 200,000—1,000,000 | 1,000           | 10                         |

4. For example
```bash
AEIM.exe 0.5 0.3 ..\Data\QPMP.dat 80 5
```
will run AEIM on QPMP, with the threshold set at MGTRatio : 0.5% and ApproximateFactor : 0.3%
```bash
LUEID.exe 9 ..\data\SIEC.dat 80 5
```
will run LUEID* on SIEC, with the threshold set at MGTRatio : 9%

