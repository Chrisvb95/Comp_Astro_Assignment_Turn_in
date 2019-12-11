# Computational Astrophysics final project
Directory containing the files that were turned in for the final project.

The write-up is found in the PDF named 'Computational_Astrophysics_Final_Project.pdf'. The text file containing the code for the final simulation is found in 'cloud_cluster_with_full_sph.py'. For each of the experiments that we ran we also made separate directories containing the code (addapted to the experiment), the results and a video of the simulation. 



---- Update on Dec 11 by Yuan Chen ----

When looking through the textbook I realized that there was a mistake in our code when dealing with the 'stopping condition': it missed the judgement of 'while density_limit_detection.is_set() == True:' before going into the 'resolve_sinks()' function, and there should have been another 'sph.evolve_model(t)'. This mistake caused the evolution to be trunked when a real stopping condtion was met, and consequently resulted in the 'discontinuity' before and after star-forming events were triggered in some of our videos. I fixed the problem in the newly updated version of our code, and I'm very sorry about it.