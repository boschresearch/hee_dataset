HEE data set
===

## General information about the data set

This is the HEE (Highway Eagle Eye) data set.
It consists of ~12000 individual vehicle trajectories (~4h), recorded by drones over a highway section (length ~600m) with an entry lane. 

*Important note:* Keep in mind that this data set can be useful for studies like ours, but some aspects of it may be noisy, so it is only meant for such experimental purposes.
In particular, the measurements in the data set are partially noisy/distortet.
Furthermore, unfortunately the "map.kml" in parts, is somewhat inaccurate.


## Citation

This data set is published as part of a research paper.
Threfore, if you are using this data set, please give the following reference:

> Geiger, Philipp, and Christoph-Nikolas Straehle. "Learning Game-Theoretic Models of Multiagent Trajectories Using Implicit Layers." Proceedings of the AAAI Conference on Artificial Intelligence. Vol. 35. No. 6. 2021.

Bibtex Code:
<pre><code>
@inproceedings{geiger2021learning,
  title={Learning Game-Theoretic Models of Multiagent Trajectories Using Implicit Layers},
  author={Geiger, Philipp and Straehle, Christoph-Nikolas},
  booktitle={Proceedings of the AAAI Conference on Artificial Intelligence},
  volume={35},
  number={6},
  pages={4950--4958},
  year={2021}
}
</pre></code>

The paper can be found [here](https://arxiv.org/pdf/2008.07303.pdf).



## Dataset details


### Python code for loading and preprocessing the data

Here are some preliminary scripts for loading/preprocessing and working with the data.

- General loading and preprocessing functions in Python](https://github.com/boschresearch/trajectory_games_learning/tree/master/data/hee_loading_and_preprocessing)
- [Example to ilter some merge tracks](https://github.com/boschresearch/trajectory_games_learning/blob/master/data/hee_preprocess2.py)

Generally, code for the abovementioned paper is [available](https://github.com/boschresearch/trajectory_games_learning).

### Files

The file "objectposition.csv" contains vehicle trajectories. It is recorded by drones that flew over a highway section that includes an onramp/entry. It is a table where each row corresponds to one object (i.e., vehicle) measured at one time instance. 

The file "map.kml" contains some lane bounday information. 


### Structure of "objectposition.csv" with explanations

"objectposition.csv" is the main data file. For each vehicle (objectid) and each timepoint (frameid), the position (longitude/latitude in world coordinates) etc. is given as one row.


Columns of "objectposition.csv" with explanations:

- objectpositionid: primary key
- objectid: reference to object
- videoid: reference to video (the data comprises several recording runs)
- frameid: reference to frame
- speed: current speed
- acceltan: tangential acceleration
- accellat: longitudinal acceleration
- latitude: latitude of the current position (geographic coordinate)
- longitude: longitude of the current position (geographic coordinate)
- angle: angle of the bounding box


### Photos


Photos can be found [in Section D.2 of the abovementioned paper](https://arxiv.org/pdf/2008.07303.pdf).


## License



The data is released unter the [CC BY-SA 4.0 license](https://creativecommons.org/licenses/by-sa/4.0/legalcode.txt) as documented in the [LICENSE.txt](LICENSE.txt) file.