# SN Ia uncertainties workshop

Workshops for the Tonale Winter School on Cosmology (https://indico.physi.uni-heidelberg.de/event/1349/)

All of the proposed workshops are code-based. For each session the useful files are detailed here, but the full list and where to download them is available at `data_requirements.txt`, along with a list of useful packages at `package_requirements.txt`. I put very basic notebooks for each session (mostly to show how to load the data), but feel free to explore if you have ideas!
Papers are there for later references rather than mandatory reading before the sessions.

### Session 1: Hubble diagram & selection effects

Get the Pantheon+ data ([Brout+22](arxiv.org/abs/2202.04077)). 
Fit the Hubble diagram and get cosmological parameters. Coming from you own experience/field, do you have an idea on how to extract unbiased cosmological parameters from the uncorrected data?
The data release also includes Hubble residuals corrected by the BBC method.
Explore how external priors impact cosmological parameter recovery.

*Extra:* Pantheon+ is not the most recent SN Ia sample, but it is often used as all the SNe are spectroscopically confirmed. As an example, DES5Y ([DES collaboration+25](arxiv.org/pdf/2401.02929)), which uses very similar methods, have some photometric SN Ias. Think about ways to account for that in w inference.

*Required data:* Pantheon+ data

### Session 2: SN Ia standardisation

Get the ZTF SN Ia DR2 data ([Rigault+25](arxiv.org/abs/2409.04346)). Design a standardisation fitting algorithm, then compare to [Ginolin+25] (arxiv.org/abs/2405.20965) values or `standax` (look at `standax/notebooks` for an example on how to reproduce the paper results). 

*Extra:* 
- Test the different fitting strategies (for example $\alpha$ and $\beta$ first, then the step). 
- Change the cuts on the data (reshift, subtypes, colour and stretch cuts…) and see what changes

*Required data:* ZTF SN Ia DR2 data

### Session 3: Simulating SNe

Simulate a simple SN Ia model with the default `skysurvey` ([Rigault+26](arxiv.org/abs/2605.25840)) model. Documentation is available at https://skysurvey.readthedocs.io/.
Then explore more complex Ia modelling based on what we saw in the lectures, You can modify the parameters of the distributions, change the distribution shapes, add extra dependencies, change the standardisation…
Use the ZTF logs to simulate a realistic sample, or « noisify » the SALT parameters directly. Think about how you could select the SNe to reproduce the sample.

*Extra:* 
- Fit the light curves with sncosmo
- Apply your standardisation fitting code to your simulated samples

*Required data:* ZTF SN Ia DR2 data

### Session 4: Simulating a realistic LSST forecast

This aims at applying everything you've done in the past three sessions. Use the LSST logs to simulate a LSST-like sample with skysurvey. Apply selection to this sample, to see how many SNe are observed. Then try to fit your previous codes (standardisation, Hubble diagram, to see if you recover the truth).

*Required data:* LSST Opsim
