``` ini

BenchmarkDotNet=v0.13.2, OS=Windows 11 (10.0.22621.755)
11th Gen Intel Core i7-11800H 2.30GHz, 1 CPU, 16 logical and 8 physical cores
.NET SDK=6.0.402
  [Host] : .NET 6.0.10 (6.0.1022.47605), X64 RyuJIT AVX2 DEBUG  [AttachedDebugger]

Method=RunBenchmarkAsync  Job=InProcess  Toolchain=InProcessEmitToolchain  
InvocationCount=Default  IterationCount=Default  UnrollFactor=16  
WarmupCount=Default  

```
| Resolution | Benchmark | AcquisitionType | DetectSegments | FullFrontal | TokenFrontal | Mean [ms] | Error [ms] | StdDev [ms] | StdErr [ms] | Min [ms] | Q1 [ms] | Median [ms] | Q3 [ms] | Max [ms] |   Op/s | Allocated [KB] |
|----------- |---------- |---------------- |--------------- |------------ |------------- |----------:|-----------:|------------:|------------:|---------:|--------:|------------:|--------:|---------:|-------:|---------------:|
|        UHD |    Detect |            N.A. |          False |        N.A. |         N.A. |     7.891 |     0.0381 |      0.0318 |      0.0088 |    7.841 |   7.874 |       7.893 |   7.902 |    7.965 | 126.73 |           1.05 |
|            |           |                 |                |             |              |           |            |             |             |          |         |             |         |          |        |                |
|        UHD |    Detect |            N.A. |           True |        N.A. |         N.A. |    25.857 |     0.5161 |      0.5522 |      0.1302 |   24.974 |  25.454 |      25.789 |  26.181 |   27.204 |  38.67 |           5.52 |
|            |           |                 |                |             |              |           |            |             |             |          |         |             |         |          |        |                |
|     FullHD |    Detect |            N.A. |          False |        N.A. |         N.A. |     7.655 |     0.0998 |      0.0779 |      0.0225 |    7.530 |   7.599 |       7.654 |   7.696 |    7.809 | 130.63 |           1.05 |
|            |           |                 |                |             |              |           |            |             |             |          |         |             |         |          |        |                |
|     FullHD |    Detect |            N.A. |           True |        N.A. |         N.A. |    14.452 |     0.2448 |      0.4415 |      0.0689 |   13.812 |  14.140 |      14.353 |  14.658 |   15.528 |  69.20 |           5.51 |
