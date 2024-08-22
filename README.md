# Video Language Planning
## [<a href="https://video-language-planning.github.io/" target="_blank">Project Page</a>]

[//]: # (### Abstract)

We are interested in enabling visual planning for complex long-horizon tasks in the space of generated videos and language, leveraging recent advances in large generative models pretrained on Internet-scale data. To this end, we present video language planning (VLP), an algorithm that consists of a tree search procedure, where we train (i) vision-language models to serve as both policies and value functions, and (ii) text-to-video models as dynamics models. VLP takes as input a long-horizon task instruction and current image observation, and outputs a long video plan that provides detailed multimodal (video and language) specifications that describe how to complete the final task. VLP scales with increasing computation budget where more computation time results in improved video plans, and is able to synthesize long-horizon video plans across different robotics domains – from multi-object rearrangement, to multi-camera bi-arm dexterous manipulation. Generated video plans can be translated into real robot actions via goal-conditioned policies, conditioned on each intermediate frame of the generated video. Experiments show that VLP substantially improves long-horizon task success rates compared to prior methods on both simulated and real robots (across 3 hardware platforms).

For more info see the [project webpage](https://video-language-planning.github.io/).

## Code

Most of the code in the paper was run using Google infrastructure -- we have attached an [illustrative colab notebook](https://github.com/video-language-planning/vlp_code/blob/master/example.ipynb) to illustrate the code for VLP. Please see this [codebase](https://github.com/UMass-Foundation-Model/COMBO/) for open source implementation of VLP which include code for training video and VLM models as well for tree search.

## Data

The long horizon dataset used in the paper can be found at the GS bucket: gs://gresearch/robotics/language_table/captions/

Each loaded sample will consist of:
long_horizon_instructions
start_times
captions
frames
end_times


