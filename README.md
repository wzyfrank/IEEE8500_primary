# IEEE8500_primary
optimal power flow IEEE 8500 node test feeder (primary only)

Edits from the original OpenDSS model:
(1) the reactor at the source is ignored (R and X set at very small values).
(2) loads models changed to 1, constant PQ.
(3) the Vminpu parameter of loads are modified from .88 to .80 p.u. to avoid the auto-conversion from constant PQ to constant impedance.
(4) the parameters (%imag, %Noloadloss, %loadloss and Xhl) are set at very small values to ingore the losses of load transformer.
(5) the length of secondary lines are set at very small values to ingore the losses of secondary lines.

Requires: (1) MATLAB, (2) YALMIP (3) SeDuMi or Mosek as the SDP solver.

Reference: Accurate Semidefinite Programming Models for Optimal Power Flow in Distribution Systems
https://arxiv.org/abs/1711.07853
