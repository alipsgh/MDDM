# ICDE 2018 - McDiarmid Drift Detection Methods
This repository is prepared for reviewers of my paper submitted to ICDE 2018.

* The source codes of MDDMs and FHDDM are available in repository [codes_for_moa](https://github.com/alipsgh/codes_for_moa/tree/master/drift_detection).
  * The source codes should be added into the [MOA](https://github.com/Waikato/moa) framework, under folder **'moa/classifiers/core/driftdetection/'**.
  * You may need to install Eclipse (or a similar Java IDE), and then import MOA as a **Maven** project.
  * For further informaiton, please click [here](https://www.cs.waikato.ac.nz/~abifet/MOA/Manual.pdf) for the manual of MOA.
* The synthetic data streams are available in repository [data_streams](
https://github.com/alipsgh/data_streams/tree/master/synthetic), (you need to unzip the files).
* You also need to pass the path of **sizeofag.jar** as a virual machine (VM) argument for being able to measure memory size of objects.
  ```
  -javaagent:[enter directory path]/sizeofag.jar
  ```
  For Eclipse, you must pass it using tab ```Arguments``` in ```Run Configurations...``` under tab ```Run``` from the main menu.
