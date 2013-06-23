SimpleScalar sim-outorder simulator with PLRU policy cache
===

We implement the 
**Alpha 21264 tournament branch predictor** 
 as illustrated in ![Figure 1][alpha-bp]
in the _SimpleScalar_(http://www.simplescalar.com/) sim-outorder simulator.

- The current Simplscalar uses 2-bit up-down saturating
counter arrays for all counter tables, we modify one of the tables (the local PHT) to
employ 3-bit up-down saturating counters. 

- The local predictor, global predictor, and meta (or choice) predictor 
in the original Simplescalar used some PC bits to index , we modify the code to use the global history.


## Configuration ##

Please further refer to a complete example configuration file _hybrid-3.2bc.cfg_.

## Compilation ##

```bash
make config-alpha
make clean
make sim-outorder
```

[alpha-bp]: alpha-bp.png 
