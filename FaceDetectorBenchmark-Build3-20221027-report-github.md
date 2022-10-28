``` ini

BenchmarkDotNet=v0.13.2, OS=Windows 11 (10.0.22621.675)
11th Gen Intel Core i7-11800H 2.30GHz, 1 CPU, 16 logical and 8 physical cores
.NET SDK=6.0.402
  [Host] : .NET 6.0.10 (6.0.1022.47605), X64 RyuJIT AVX2 DEBUG  [AttachedDebugger]

Method=RunBenchmarkAsync  Job=InProcess  Toolchain=InProcessEmitToolchain  
InvocationCount=Default  IterationCount=Default  UnrollFactor=16  
WarmupCount=Default  

```
| Resolution | Benchmark | AcquisitionType | DetectSegments | FullFrontal | TokenFrontal | Mean [ms] | Error [ms] | StdDev [ms] | StdErr [ms] | Median [ms] | Min [ms] | Q1 [ms] | Q3 [ms] | Max [ms] |  Op/s | Allocated [KB] |
|----------- |---------- |---------------- |--------------- |------------ |------------- |----------:|-----------:|------------:|------------:|------------:|---------:|--------:|--------:|---------:|------:|---------------:|
|        UHD |    Detect |            N.A. |          False |        N.A. |         N.A. |     10.54 |      0.210 |       0.532 |       0.061 |       10.37 |    8.831 |   10.17 |   10.82 |    12.01 | 94.90 |           1.05 |
|            |           |                 |                |             |              |           |            |             |             |             |          |         |         |          |       |                |
|        UHD |    Detect |            N.A. |           True |        N.A. |         N.A. |     26.25 |      0.506 |       0.473 |       0.122 |       26.22 |   25.529 |   25.87 |   26.52 |    27.25 | 38.10 |           5.52 |
|            |           |                 |                |             |              |           |            |             |             |             |          |         |         |          |       |                |
|     FullHD |    Detect |            N.A. |          False |        N.A. |         N.A. |     10.12 |      0.134 |       0.159 |       0.035 |       10.05 |    9.912 |   10.01 |   10.23 |    10.47 | 98.81 |           1.05 |
|            |           |                 |                |             |              |           |            |             |             |             |          |         |         |          |       |                |
|     FullHD |    Detect |            N.A. |           True |        N.A. |         N.A. |     16.58 |      0.302 |       0.268 |       0.072 |       16.47 |   16.309 |   16.40 |   16.73 |    17.23 | 60.32 |           5.52 |
