Big Data in Finance final exam, Part B2, calculating PI using CUDA Thrust
=========================================================================

The CUDA Thrust program has several bugs. These bugs can be in the C code,
the makefile, or the PBS job file. Your task is to find these bugs,
fix them, compile and run the program, then share your results.

In this file, write any thoughts or comments that might help
improve your grade.

And, remember, to use Git you must first load Git:

  module load git
  
Similarly, to use CUDA (and CUDA Thrust):

  module load cuda
  
These may also be useful commands:

  module list
  
  module avail
  
And a hint to help you on your way. Remember that every GPU program has
two parts: a CPU part and a GPU part. To run this example you will have
to engage, at a minimum, at least 1 CPU and at least 1 GPU.

Comments: 
makefile had the same issues as in part 1. I added identation and corrected the name of the file

pbs file: corrected 0 to for ncpus
removed # sign from the line "cd $PBS_O_WORKDIR"
at the bottom corrected ./cuda-thrust

cuda-thrust.cu:
corrected two commented lines on the top
multiple errors: changed **device** to __device__; 
corrected the if condition changed "? 1 : 1" tp "? 1 : 0"

