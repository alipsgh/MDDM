# McDiarmid Drift Detection Methods
This repository is prepared for McDiarmid Drift Detection Methods.

* The source codes of MDDMs and FHDDM are available in repository [codes_for_moa](https://github.com/alipsgh/codes_for_moa/tree/master/drift_detection).
  * The source codes should be added into the [MOA](https://github.com/Waikato/moa) framework, under folder **'moa/classifiers/core/driftdetection/'**.
  * You may need to install Eclipse (or a similar Java IDE), and then import MOA as a **Maven** project.
  * For further informaiton, please click [here](https://www.cs.waikato.ac.nz/~abifet/MOA/Manual.pdf) for the manual of MOA.
* The synthetic data streams are available in the [data_streams](
https://github.com/alipsgh/data_streams/tree/master/synthetic) repository, (you need to unzip the files).
* You also need to pass the path of **sizeofag.jar** as a virual machine (VM) argument for being able to measure memory size of objects.
  ```
  -javaagent:[enter directory path]/sizeofag.jar
  ```
  For Eclipse, you must pass the path using tab ```Arguments``` in ```Run Configurations...``` under tab ```Run``` from the main menu.
* I have already built a **moa.jar** file and shared it in this repository. You should run it in a terminal (or in a command prompt in Windows). You may use a command similar to the one below for an experiment:
  ```
  java -cp moa.jar -javaagent:sizeofag.jar moa.DoTask alipsgh.EvaluatePrequential -l \(drift.alipsgh.DriftDetectionMethodClassifierSyntheticData -l trees.HoeffdingTree -d MDDM_G -m 20000 -n 4 -a 250\) -s \(ArffFileStream -f /home/ali/moa/data_streams/arff/sine1_w_50_n_0.1/sine1_w_50_n_0.1_101.arff\) -e BasicClassificationPerformanceEvaluator -i -1 -f 1000 -q 1000
  ```
  The results would be similar to:
  ```
  Delay, TP, FP, FN, Runtime, Memory, Classification Accuracy
  39.25,4,0,0,49,1344,87.05
  ```
  
Please contact me for any problem.
  
  <br/>
  <br/>
  
<sub>Ali Pesaranghader © 2017</sub>
