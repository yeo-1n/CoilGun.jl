# CoilGun.jl
This program models the behavior of a ferromagnetic projectile under the influence of magnetic induction. This device, known as a Gauss Cannon (or Coil Gun), uses a series of solenoids to accelerate a projectile by sequentially turning solenoids on and off. With the aid of Julia and its packages, all known phenomena involved with magnetizing and accelerating a ferromagnetic projectile can be be simulated.

The device itself can be used for a number of different applications. Some notable applications are: general nailing, clearing computer memory, material testing, scientific demonstrations, etc, etc. The goal of this project is to be able to accelerate the projectile to mach 1.


This code takes into consideration the following effects:

Markup: 
    -Friction

    -air resistance

    -time for switches and coils to reach a steady state value

-energy lost in circuit and in projectile

-Primary forces as well as secondary; Secondary forces are dependent upon a dynamic system. If a system is static, no secondary forces exist. An example would be an induced counter-current when a magnet is traveling towards or away from a solenoid.

Assumptions*:

-The magnetic field inside a wire loop is constant, and is calculated at the center. Also, all of the winding are treated as if they're in a single loop at the effective radius.

-projectiles geometry is a perfect cyliner

-The pinning factor (when calculating the magnetizaiton) is a constant i.e. energy loss due to domain rotation is negligible.

-The interaction between the coil and the projectile is like a wire loop to a magnetic dipole

-Each coil/loop is seperated by the actual length of the coil

-The current created by the capacitor and coupled coils is completely independent from the current induced by the accelerating projectile.

-The entire material's magnetizaiton can be assumed to be constant throughout the projectile, holding the magnetization value of the closest part of the projectile to the magnetic field. Also that the behavior of the magnetic domains can be accurately generalized and averaged.

-The friciton force between the projectile and the barrel is, once moving, independent upon velocity.


It's not taking into consideration:

-quantum effects (besides the domain magnetic dipoles) into consideration

-frictional force of rifling into consideration or the effects that it would have on the projectile

-Navier-Stokes drag (using Newtonian)

-Magnetostriction, other stress/strain relations to magnetizm or their effect on permeability.

-Earths magnetic field  

-How the barrel affects the generated magentic fields.

-How the voltage produced from the capacitor changes in time.
 

*All assumptions made will gradually be made to fit closer with reality. The complexity of the system will increase until either the simulation provieds accurate resutls and matches reality (error < 1%), or until computation time is unreasonably long (like taking 10 minutes to complete the simulation).


```math
\scrL
```

Sources Used:

Jiles, D. C., & Atherton, D. L. (1986). Theory of ferromagnetic hysteresis. Journal of magnetism and magnetic materials, 61(1-2), 48-60.
    This paper was used to understand the magnetization process. This describes the derivation of some of the equations used. Some of the equations used were the:
    ```math \scrL 
    ```