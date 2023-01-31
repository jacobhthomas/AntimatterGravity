# Antimatter Gravity -- Developing an Antimatter Gravity Interferometer

In order to determine the effect of gravity on antimatter, an experiment has been proposed to use a muonium beam, which is produced by passing antimuon particles through superfluid helium, SFHe, then reflecting it through a modified Mach-Zehnder interferometer, to diffract through two gratings in order to make the measurement of the change in height, as a result of gravitational effects, easier, if not possible – the reason for this will be further discussed later, as I update this README.md.

Muonium, an exotic atom composed of an antimuon and electron, has been chosen for the experimental simulation because of its feasibility — when compared to antihydrogen and positronium — and theoretical interest in this experiment. Since the antimuon component of muonium acts as the nucleus, the particle behaves as antimatter in a gravitational field. When looking closer at using positronium, it is noticed that the half-life is too short to allow for measurable effects of gravity on the beam, if gravity does affect antimatter differently. It is to be noted that this half-life changes when a positronium beam enters an excited state, which can be caused by lasers, but in comparison to muonium, seems to be an unnecessary step to take. With regard to antihydrogen, it does not have the issue of too short of a half-life but instead poses its own problems. Most notably, the effect of the strong force in antihydrogen is very apparent and requires extensive calculations, unnecessary when using a particle unaffected by the strong force. Because of the composition of muonium, which is one electron and one muon, two leptons, the strong force is not a present source of variation.

The simulation uses a Gaussian-Schell model to represent the beam, as was the model used in Ben McMorran’s simulation for *Electron Diffraction and Interferometry Using Nanostructures*. This model, which is a wave field,  is used because of its ability to accurately characterize beams of both high coherence and near incoherence, lending itself to deeper insights into the beam. To simulate the grating structure, the code uses a Fourier series, which allows for the calculation of the beam intensity. Three unique grating structures, or functions, are used to describe the beam at its three distinctive stages, described as GP0, GP1, and GP2. Each of these represents the beam before passing through a grating, after passing through the first grating, and after passing through the second grating, respectively.

For the grating functions, since periodicity must be implemented, multiple gratings of varying widths will be simulated in a single period to allow for periodicity to be preserved during size variation. However, the aperiodicity of the grating structure reduces the effectiveness of the Fourier series, since not every grating can be modeled through the periodic Fourier expansion. Nonetheless, the use of the Fourier series in the experimental simulation will remain because of the speed at which it can be processed by the code. Additionally, the code allows for independence between GP0, GP1, and GP2, allowing for the intensity distribution to be generated – computed – at any point along the z-axis. This independence also allows for the grating function to be generated without the need for the preceding grating stage.

The importance of measuring the effect of gravity on antimatter, muonium in this experiment, can be seen by the lack of direct experimental confirmation that matter and antimatter behave the same in a gravitational field. While the equivalence principle is commonly assumed to hold true for this interaction, it is becoming of greater interest in the physics community to see asymmetry between antimatter and matter’s behavior in gravity. This is because of its potential to give deeper insight or provide alternatives to topics such as CP violation, dark matter, dark energy, and cosmic inflation to some of the most enigmatic questions of modern physics.
