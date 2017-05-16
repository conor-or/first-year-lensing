# First Year Lensing Project

Welcome to the project! This is where I'll keep all the materials and I'll update it as we move along.
Please use the Slack for any queries!

Timetable of project (from dept. website)

* Week of Tuesday 9 May: First meeting with project supervisor (email discussions before this are encouraged)
* Weeks 2-7: Project work
* Week 8: Display preparation
* Thursday 22 June: 1pm-4.30pm Open Day (GCSE + departmental visitors)
* Friday 23 June: 1pm-4.30pm Open Day (A-Level + departmental visitors)
* Monday 26 June: Reports due at 4pm
___

##### A consequence of general relativity is that mass causes light to bend. Different mass deflects light in different ways and essentially, that's gravitational lensing.

<p align="center">
<img src="https://github.com/conor-or/lens-mcmc/blob/master/images/image1.png" width="400"><img src="https://github.com/conor-or/lens-mcmc/blob/master/images/image2.png" width="400">
<img src="https://github.com/conor-or/lens-mcmc/blob/master/images/image3.png" width="400"><img src="https://github.com/conor-or/lens-mcmc/blob/master/images/image4.png" width="400">
</p>

___

### Method in a Nutshell

The process of modelling a gravitational lens system can be broken into a few parts:
1. Defining some kind of source (background) object to be 'lensed' (this is the easy bit, first we'll make some sources using a Gaussian but we should be able to try real photos of people, places etc)
2. Defining a lens (foreground) object which has some mass distribution. This is where 99% of the computation actually is; different distributions of mass cause different deflections. The most typical of these distributions are very well studied and their deflection angles have analytic forms which should be easy to implement in NumPy.
3. Matching the deflected path of the light to a point in the background and producing the full image. This is a process called ray-tracing and is really only a coordinate transformation - very simple!

### Project Goals

By the end of the project we should aim to achieve most of the
following:

- Use NumPy and SciPy to construct a gravitational lens model and ray-trace an image
- Use maptlotlib to create high-resolution images and animations of lenses
- Lens your friends! Use PIL to import real photos for lensing
- Present your work as a good understanding of grav. lensing using attractive and interesting images

### Reading List

Some papers covering different aspects of lensing:

##### Lensing Theory
* [My MSc Dissertation](https://github.com/conor-or/first-year-lensing/raw/master/docs/dissertation.pdf) has all the lensing theory we'll need. Of use to us is the stuff in the first half of chapter two.
* [Narayan and Bartelmann, 1998](https://arxiv.org/abs/astro-ph/9606001) is another good introduction, chapter two covers all the point mass stuff quite well.

##### Simulating Lensing (Computations)
* [Kormann, 1994](http://adsabs.harvard.edu/abs/1994A%26A...284..285K) gives an analytic solution to a specific type of lens called the Single Isothermal Ellipsoid. This is a very good model for most early-type galaxies. This is likely all we'll use.
* [Tessore and Metcalf, 2015](https://arxiv.org/abs/1507.01819) provides an ultra-fast method for analytically calculating any elliptical gravitational lens. More general than Kormann but a bit trickier.

##### Real Lenses
* [The SLACS Project (Auger, Bolton et. al.)](http://www.physics.utah.edu/~bolton/slacs/Home.html) is the state of the art on lensing surveys, plenty of really nice images here.
* [Shu et. al., 2016](https://arxiv.org/abs/1608.08707) really has the best looking images of gravitational lenses out there (see pages 8-11), all taken with the Hubble Wide Field Camera. We can compare our results to some of the these images.
