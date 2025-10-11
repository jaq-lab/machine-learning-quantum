# Plan for the world model  quantum project

Timeline


1. October (2 weeks)
   - Ising model evolution, time-trace of the OBSERVABLES (N different terms: mz(t), N^2 second order terms: mz1mz2(t), 6 numbers, 12)
   - Connect LSTM to predict time-series of the observables
   - Train LSTM on the Ising model evolution, 
   - Add noise to evolution *optional* (OU noise, white noise, correlated noise)
   - Train LSTM on states instead of time-series of the observables *optional* (64 variables, 16 for two qubits)


2. November (3 weeks) 
   - Decide on geometry: 2D, 1D, random - spin glass. 1D = J_ij = J_{i,i+1}, random: J = np.random(NxN) 
   - Decide on ferro/para, sign of the couplings
   - Autoencoder to compress and to reconstruct the state to a latent space (no evolution) STATES (SMALL 2-3 qubits 8x8 density matrix)
   - Sequential training, autoencoder and LSTM (indepedent) 
   - Joint training, autoencoder and LSTM (dependent)

3. December (3 weeks)
   - Reality direction: replace DM by shadow tomography (parallelization of the shadow tomography)
   - Machine learning direction: scale up LSTM, add attention mechanism, Gen RL
   - Physics direction: add noise to the evolution, OU noise, white noise, correlated noise
   - If noisy -> Consider diffusion model (score models) https://arxiv.org/pdf/2011.13456

4. January (3 weeks)
 - fallbacks, issue solving...
 - put it cluster, JAX tricks
 - try to generalize, learn on N qubits, infer/deploy on N+1
 - start write down thesis
 - first plots -results
  
5. February (3 weeks)
- Polishing, repository
- Training in background
- Theory, effective models, 

6. March (4 week)
- writing up.

