# Supercomputing 2019 Architecture Testbed BoF
_Approximate Attendees: ~50_
[SC19 BoF webpage](https://sc19.supercomputing.org/proceedings/bof/bof_pages/bof227.html)

These notes represent some subset of the discussion and questions for the BoF held in Denver, Colorado during SC 2019. 

**Panelists**: Alice Koniges (AK), Jiajia Li (JJL), Mark (MK), Jeff Vetter (JV), Jim Laros (JLS), Jeff Young  (JY)

## Introductions 
* CSCS and ORNL working on giving users lots of access (e.g. something close to root) via bare-metal instances
     * Brings up issues of security and reproducibility 
* JLS - "On a testbed, you never say no”. That is, they are places to try implementations and configurations that might be tough elsewhere.

## Audience Questions

1) Is 8 nodes enough to address scalability? 
* JLS - No, not the point of a testbed 
* JV - A couple nodes is plenty to address the node architecture, many evaluations aren’t concerned with transferring data between nodes. 2 or 3 is good though as it is just as easy to manage as 1
* JJL - Sounds like they may rely on network performance models for testbeds 
* AK - some times you can identify problems with vendor MPI implementations (such as compilation issues) with only a few nodes 

2) How do you trade off adding something to a testbed vs. using AWS
* JV - Time to setup is important - FPGAs are complicated and available online. GPUs are easy, so set-up yourself
* JLS - It is important to build vendor relationships with vendors so that you can have an option to influence industry. Can’t build these relationships when using cloud
* AK - The detailed performance information is not available through the cloud 

3) Do vendors support you?
* Sometimes - more if you are a large organization
* AK - hackathon model worked well to get engagement

4) What’s the most exciting emerging technology?
* JLS - ARM, ARM GPUs, Dataflow computing, HBM (further integration). 
* JV - Dark silicon  - “almost certain”; Versal and coarse grained reconfigurable devices are also interesting along with silicon photonics 
* Alice - More portable programming models from vendors 
* Young - ML accelerators like the Cerebras Wafer Scale Engine

5) How do we do testbeds for truly new chips, e.g. TrueNorth? How do you decide whether or not to include them?
* JY - It would be best if those systems have some support from the vendor, and if you have people locally that could become an expert 
* MK - What goes into the testbed must first have interest from their engineers
* AK - Decision to include will be dependent on how well it is expected to work for their apps of interest 

6) How do you test new interconnects?
* JLS - They install high speed interconnects, and you do what you can
* JY - At GT, we try to get a single high performance link so you can test drivers, MPI libraries, etc. 
* MK - Try to do Ethernet and Infiniband on each node

7) How do we handle data sharing?
* JV - NDAs are too restrictive. Would be nice if two groups under the same NDA could share info. 
* JLS - Multi-party NDAs are hard, but they have found workarounds for new systems.
