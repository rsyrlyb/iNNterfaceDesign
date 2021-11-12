# iNNterfaceDesign
This package provides a framework for one-sided design of protein-protein interfaces based on features of protein receptor. This novel method is based on pipeline of neural networks processing features of the protein surface and producing the relevant binders and motifs for the target. The method is extremely quick and does not imply scanning of libraries with native PPI. The figure below demonstrate performance of the method on SARS-CoV-2 receptor binding domain. Crystal structures of all generated binders for the rarget can be found in folder "output_examples" for mor clar overview of capabilities of the method. If someone is interested in these designs from practical point of view, they can contact with us for collaborative work.

|     :---:      |     :---:      |
|![capture](gif/1l6x_pepseq.gif)|![capture](gif/1l6x_bb.gif)|

The framework includes the following main neural network models:
1) PepBB generating 6-residue backbones of binders;
2) BepBBE elongating initial backbones;
3) PepSeP1/PepSep6 designing amino acid sequences for the backbones.

All these methods can be used separately.

The outputs include designed backbone in docked pose and designed amino acid sequence for it. Mapping of amino acid sequence to the backbone and subsequent relaxation have to be done in other specialized software, like Rosetta. Normal job should include filteing as well, since some produced binders are of poor quality.

## First time setup ##

The following software and python packages have to be installed  in order to run PepBB:
1. python v3.7 or higher;
2. PyRosetta;
3. Tensorflow.

Setup consists in a mere downloading of folder “PepBB” and unzipping of an archive “Models” in “PepBB/Modules” directory into the same destination.
