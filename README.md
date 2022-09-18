EM_particle code

An electromagnetic particle code is utilized for solar and magnetospheric space physics. Both electric and magnetic fields at low frequencies are solved by a slightly backward time decentering technique. Magnetic reconnection and solar wind-earth magnetic field coupling are quite suitable for applying this code.

One uses here the time decentered scheme \aimpl=0.6, while the time centered scheme in the explicit code (\aimpl=0.5) is used in the other directory of molecular dynamics simulations. It is noted that finite errors in the divergence term accumulate which must be corrected if the finite difference coordinates are utilized. Four physical units are, i) time: 1/wpe (c/wpe: electron inertia length), ii) length: c/wpe, iii) mass: electron mass, and iv) charge: electron charge. The program is written in Fortran 2003 and MPI version 3 for parallelization.

By the implicit scheme it is free from the Courant condition, that is, Dx(length)/Dt(time step) >< c, the speed of light. For the backward differential scheme \aimpl > 0.5, a time step may be dt~1.2/wpe to dump out plasma oscillations, while 2 \pi/dt \wce > 1 for the kinetic ions and electrons. A large time step of 2 \pi/dt \wce >> 1 is a good target of the drift-kinetic simulation code, where a typical time step may be dt= 10/\wpe. References to read this implicit particle code are recommended.

References:

1. M. Tanaka, A simulation of low-frequency electromagnetic phenomena in kinetic plasmas of three dimensions, J.Comput. Phys., 107, 124-145 (1993).

2. M. Tanaka, Macro-EM particle simulation method and a study of collisionless magnetic reconnection, Comput.Phys.Commun., 87, 117-138 (1995).

3. M. Tanaka, Macro-particle simulations of collisionless magnetic reconnection, Phys.Plasmas, 2, 2920-2930 (1995).
 
4. H. Shimazu, M. Tanaka, and S. Machida, The behavior of heavy ions in collisionless parallel shocks generated by the solar wind and planetary plasma interactions, J.Geophys.Res., 101, 27565-27571 (1996).

