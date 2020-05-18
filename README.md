[Project contains large files e.g. pretrained model weights, so it cannot be uploaded directly to Github, unless GIT LFS (Large File Storage) is used]

For the full project go to this link - https://dev.azure.com/russelalfeche/_git/TF-Image-Recog_UiPathAIFab-vs-Local

# UiPath AI Fabric vs Local Hosted Model - TF Image Recognition
Comparison of execution speed of a locally inferenced TF image recognition model against the same model but deployed in AI fabric

# Getting Started
This section will show the prerequisites on how to setup the local environment and AI fabric environment before running the workflow

## Prerequisites

### Locally Hosted Model Execution
 - [x] [Python 3.x Install](https://www.python.org/downloads/) or [Anaconda 3.x Install](https://www.anaconda.com/products/individual)
 - [x] Python 3.6 **Environment** (virtual env or conda env)
 - [x] Python Package Dependencies 
 - tensorflow==1.14.0
- numpy==1.16.4
- six==1.12.0
- future

### AI Fabric Hosted Model Execution
 - [x] Upload packaged model in '.\ai_fab_ready_pkg' folder into AI fabric instance then [create an ML skill](https://docs.uipath.com/orchestrator/docs/about-ml-skills)
 - [x] Make sure to connect your robot machine/s (that will consume the ML skill) into the Orchestrator with the AI fabric instance where you deployed the ML skill
 - [x] Check the ML skill activity in the workflow and make sure it calls the deployed ML skill

## How To

### Running the workflow

1. Open **Main.xaml** via studio and hit Run.

2. The workflow will prompt a dialog to select model host 


![enter image description here](https://lh3.googleusercontent.com/QhqpGEfiYOaAQvp5BJUX_sY37yG5eH9GAyN9D61QZtoRXGZkBv0OeRJik3wvUnGD5-XTC5kUxnFMO4CQFO1WiCM4M1Ym9e7jmSMpCg7fo9Ux7YG8KwzJlYJTunamUziVU1RLUvOaOjJQbHI7EX24q3kCmOsWEgNdpASouqslKGlwaF6MIYHITyyEuCX6pfW2Ph_nsR5cbnV4DhI6USY-PaeYxsz9xD0q1qcqJ52NSBtt-kGhKmk0RNOn5GvtWcpi0i1BEW1m2KGSgkcSl0gqMVQGH6tWn6VT265p0gkZqc_fTW4sX4C6trqkkE1wxGTd3s1T5UNlsU889GBbupDuvhOQQ692xs_DT58-E98eHS0mYTAvdMB1kbcj4Cl9gMrzqAd_WUpQ1VOeeM5_JIkx9FvrgYUx8ocm1KOtHYRlkvPYF34iFsuAyz4OZXGzs5stWzi8_rH6GRo9DpOc_rZshmHuyDJcktp803i7eyglnf_lCcce-40VIDpy3DKlTrVkVGctTE-0tqqQBhc84fuPzD3seljgNOiLRpasT_dY0FSv_9UDDbKedpWdOBZFlTJLCaaNAdpehJ5ZyM64fLTVD6wku63ePz0ZVSZXOGc4K3xt1Igr57QJdmfr9DX7cVRKCzk_RotAcfJtmZcARh2uwPCo9NVJP_tCngqZ9klkUYRmrYqUiKBJrgDzy0ML)


3. Select **'Local'** and check **studio output tab** to see the runtime speed of locally hosted model.


![enter image description here](https://lh3.googleusercontent.com/pw/ACtC-3fndKfjnHlMBm0MYKmZzFbHWV1k2rGPLyMtayQLOHX_gMtB2KSvfOWDM3XtidBw2rsx55mLG8Tko1Ca1H9dsdjGn3MneagX3RYqzfrjuyRC4j-NwPyFIS-r62K5ZIcbnQ28BzZlhBFUNqjIWqyAvTC8)


4. Select **'AI fabric'** and check **studio output tab** to see the runtime speed of locally hosted model.


![enter image description here](https://lh3.googleusercontent.com/r2sD1UpcwEbrGk-6ZRfFk6Y76A3gOVZcMVqiPa2Sg11ZkSf1rFMHgbeMRELocCgIm8mKIC4Ea6_X1e_FzpEOgMFlo8-sDhMtkMY27J7hB7HQjJeTxM7KaACWYtLb-9FCLC5al9fwMrgA4Vi7G4rIi_8O3ZT7ocu1GW92O9mI0wbvqq3ngRQqix8LGcJ0rdFpyNtjvnBlcA8K8eIhOLqrrSHwOAmnENDdGI3YGVGPYIHvO6Yestkq57-STfqgKWJ8Lv-8Fw28LuXA0eVnSoWWhFBMqplxi-NjaUAIC5VXpO5oN1zNNbpKbJVOqfqZ71oZqFBFk5CvpnuCSCplTchY3GV5H9nQtGEIUjZxWKIspfU-d15nlo3xuBysegDDdNQdWOBrk0h00DPnZZrn6G_L6n1daYwIiC9AwiDf3YBo2SAo5Jj44TdxTGeHwKopMH-i_7yU1LAQq51skCqW96pTFt-ij91bNCbfjVl-Z0juIeLB_RveXc99rAfG03T_IrLpf-oc0meC1ky_sy9dB63f31usMEcXb_2v37R8U8QfIkTBs5Gb8QuX-Rqmf357PGvwlZbF7Z_tRiQ5VJNolOHzwrjYt0dzcedR-WdVgu6H2Co2nEkbfe5qMLiClGrYqMadzP61uDzF8YeGKZIRnsHsUhjie0EcSRbHku_U_JTpwalCqQHB93atUPTq2kdb)


6. Check project output - Recognized and processed images will go to the 'Processed' folder where the images are renamed to their corresponding labels.


7. Check project output - Runtime speed logs it output on a text file in the project folder

# License
Copyright (c) Russel Alfeche. All rights reserved.

This project is licensed under the MIT License - see the [LICENSE.MD](LICENSE.md) file for details
