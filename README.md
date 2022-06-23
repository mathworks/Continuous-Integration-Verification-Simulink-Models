<h1>Continuous Integration for Verification of Simulink® Models</h1>

This project is used in the explanation of the Technical Article ['Continuous Integration for Verification of Simulink® Models'](https://www.mathworks.com/company/newsletters/articles/continuous-integration-for-verification-of-simulink-models.html) to describe a simple end-to-end example showing Model Based Design integration into Jenkins® and GitLab® where Jenkins is used as CI system and GitLab as version control system. Upon following the steps in the Technical Article, one can setup a running Continuous Integration pipeline performing verify, build, and test stages to generate corresponding artifacts.



Quick Start guide
==================
1. Fork the repository to your own GitHub® account.
2. Configure MATLAB, GitLab and Jenkins, as outlined in the Technical Article.
3. Create a new CI job using your forked repository.

Please refer the Technical Article ['Continuous Integration for Verification of Simulink® Models'](https://www.mathworks.com/company/newsletters/articles/continuous-integration-for-verification-of-simulink-models.html) for detailed instructions on how to setup and run the continuous integration pipeline.



Folder Structure
================


    .
    ├── Data                                           # Data required to run the models and test cases
    │   ├── ACC_01_ISO_TargetDiscriminationTest.mat
    │   ├── ACC_02_ISO_AutoRetargetTest.mat
    │   ├── ACC_03_ISO_CurveTest.mat
    │   ├── ACC_04_ISO_StopnGo.mat
    │   ├── LFACC_01_DoubleCurve_DecelTarget.mat
    │   ├── LFACC_02_DoubleCurve_AutoRetarget.mat
    │   ├── LFACC_03_DoubleCurve_StopnGo.mat
    │   ├── LFACC_04_Curve_CutInOut.mat
    │   ├── LFACC_05_Curve_CutInOut_TooClose.mat
    ├── Models                                        # Simulink models used to model lane change logic
    │   ├── LaneFollowingTestBenchExample.slx
    │   ├── LFRefMdl.slx
    ├── Requirements                                  # Requirements for the lane change controller
    │   ├── LaneFollowingTestRequirements.slreqx
    ├── resources                                     # Simulink project related files
    ├── Scripts                                       # Scripts used to setup models, tests, and visualizations
    │   ├── createLaneFollowingController.m           # Helper script to design MPC Controller for lane following application
    │   ├── createLaneSensorBuses.m                   # Defines Lane Sensor Buses
    │   ├── getDiscreteModelForAdaptiveMPC.m          # Helper to get discrete state-space model for adaptive MPC
    │   ├── helperLFSetUp.m                           # Initializes lane following example model
    │   ├── helperSessionToScenario.m                 # Helper to convert scenario to drivingScenario object
    │   ├── LaneFollowingExecControllerBuild.m        # Builds controller
    │   ├── LaneFollowingExecModelAdvisor.m           # Performs Model Advisor analysis
    │   ├── plotLFResults.m                           # Helper to plot results of lane following example
    ├── Tests                                         # Test cases we will execute as part of our CI pipeline
    │   ├── LaneFollowingTestScenarios.mldatx         
    │   ├── LaneFollowingTestScenarios.slmx           
    ├── SltestLaneFollowingExample.prj                # Can run this file in MATLAB® to setup the Simulink project
    ├── LICENSE
    ├── SECURITY.md
    └── README.md



Products/Toolboxes Required
===========================
- [MATLAB®](https://www.mathworks.com/products/matlab.html)
- [Simulink®](https://www.mathworks.com/products/simulink.html)
- [Automated Driving Toolbox™](https://www.mathworks.com/products/automated-driving.html)
- [Computer Vision Toolbox™](https://www.mathworks.com/products/computer-vision.html)
- [Control System Toolbox™](https://www.mathworks.com/products/control.html)
- [Embedded Coder®](https://www.mathworks.com/products/embedded-coder.html)
- [Image Processing Toolbox™](https://www.mathworks.com/products/image.html)
- [MATLAB® Coder™](https://www.mathworks.com/products/matlab-coder.html)
- [Model Predictive Control Toolbox™](https://www.mathworks.com/products/model-predictive-control.html)
- [Requirements Toolbox™](https://www.mathworks.com/products/requirements-toolbox.html)
- [Simulink® Check™](https://www.mathworks.com/products/simulink-check.html)
- [Simulink® Coder™](https://www.mathworks.com/products/simulink-coder.html)
- [Simulink® Control Design™](https://www.mathworks.com/products/simcontrol.html)
- [Simulink® Coverage™](https://www.mathworks.com/products/simulink-coverage.html)
- [Simulink® Test™](https://www.mathworks.com/products/simulink-test.html)



License
=======
The license for Continuous Integration for Verification of Simulink Models is available in the [License.txt](License.txt) file in this repository.



Community Support
=================
[MATLAB Central](https://www.mathworks.com/matlabcentral/)


Copyright 2022 The MathWorks, Inc.
