# TAS_Benchmark
Public set of problem instances for the evaluation of scheduling algorithms for TAS.


# Parameters
Each set consists of 40 instances per parameter configuration, all parameters are set to the respective default value except for one.
- Topology: Line, Ring, Star, Scale-free, RRG
- Nodes: 10, 20, 50, 100 Bridges
- Frames: 250, 500, 1000, 2000, 4000, 8000
- Periods: 500µs (industrial automation/isochronous), 1ms (industrial automation/isochronous, automotive, aerospace), 1ms+2ms (industrial automation/isochronous, automotive, aerospace), 20ms+50ms+100ms (automotive), 2ms+16ms+128ms (aerospace)
- Frame size: 84B, 813, 1542B, Random
- Latencies: 1x period, 0.5x, 0.25x
- Frames per stream: 1, 2, 4
- Listeners per stream: 1 (unicast), 2, 4, 8, 16


# Default Parameters
The folder /instances_final/default contains the problem instances with default parameter configuration. These are implicitely part of every parameter study and must be considered, but the files are not duplicated in the folders of other studies.
- Topology: Ring and RRG (20 per set each)
- Nodes: 20
- Frames: 1000
- Frame size: Uniformly sampled from [84,1542]
- Listeners per stream: 1 (unicast)
- Periods: 1ms+2ms
- Latency: Same as stream period
- Frames per period: 1

# Units and Encoding
- Times are stated in nanoseconds
- Data size is stated in byte
- Transmission rates are stated in byte/ns for numerical reasons
- Paths are orded lists of links from talker to listener. Multicast paths are given as a single link sequence in topological order from talker to listeners, i.e., every link is only contained once and all except one link have a predecessor with lower index in this list.
