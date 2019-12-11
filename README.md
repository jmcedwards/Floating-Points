# Floating Points Website

Website for the musician Floating points that uses WebGL shader for mixed grid-particle fluid simulation.

## Simulation 

<img style="width:100%" src="example.png"/>

This simulation solves the <a href="https://en.wikipedia.org/wiki/Navier%E2%80%93Stokes_equations" target="_blank">Navier-Stokes equations</a> for incompressible fluids in a GPU fragment shader.
I implemented <a href="https://en.wikipedia.org/wiki/No-slip_condition" target="_blank">no-slip boundary conditions</a> at the borders to keep the fluid contained within the bounds of the screen.
To increase performance, I solved for the velocity vector field of the fluid at a lower resolution than I used to compute the visualization of fluid flow; I used bilinear interpolation to smooth out artifacts caused by this speedup.
There is the option to add <a href="https://en.wikipedia.org/wiki/Lagrangian_particle_tracking" target="_blank">Lagrangian particles</a> on top of the simulation -
these particles are rendered using <a href="https://threejs.org/" target="_blank">threejs</a>, but their positions are computed on the GPU.

<img style="width:100%" src="example2.png"/>

## Instrutctions

Move the mouse over the webpage to apply a force to the fluid. Over time, the colored material in the fluid will dissipate.

## Maths

To learn more about the maths involved, check out the following sources:<br/>

1. <a href="https://pdfs.semanticscholar.org/84b8/c7b7eecf90ebd9d54a51544ca0f8ff93c137.pdf" target="_blank">Real-time ink simulation using a grid-particle method</a> - mixing Eulerian and Lagrangian techniques for fluids<br/>
2. <a href="http://developer.download.nvidia.com/books/HTML/gpugems/gpugems_ch38.html" target="_blank">Fast Fluid Dynamics Simulation on the GPU</a> - a very well written tutorial about programming the Navier-Stokes equations on a GPU.
Though not WebGL specific, it was still very useful.<br/>
3. <a href="http://jamie-wong.com/2016/08/05/webgl-fluid-simulation/" target="_blank">Fluid Simulation (with WebGL demo)</a> - this article has some nice, interactive graphics that helped me debug my code.<br/>
4. <a href="http://www.dgp.toronto.edu/people/stam/reality/Research/pdf/ns.pdf" target="_blank">Stable Fluids</a> - a paper about stable numerical methods for evaluating Navier-Stokes on a discrete grid.

## Credits

Fluid simulation framework by <a href="http://www.amandaghassaei.com/" target="_blank">Amanda Ghassaei</a>, code on <a href="https://github.com/amandaghassaei/FluidSimulation" target="_blank">Github</a>.
          
Website design by Jamie Edwards, jmcedwards@live.co.uk.      

## Issues

The left button works and when clicked brings up the information about that album, bellow is the html code for the button and page it brings up (in the file index.html).

<img style="width:100%" src="left_button_html.png"/>

The css for the left button is shown bellow (in the file main.css).

<img style="width:100%" src="left_button_css.png"/>

However the right button doesn't work. I am unsure how to link the button to bring up the page in the same way as with the left button. I recon the issue is with the href line (line 463) as shown bellow along with the page it's supposed to bring up.

<img style="width:100%" src="right_button_html.png"/>

The css for the right button is shown bellow (in the file main.css).

<img style="width:100%" src="right_button_css.png"/>
