# MULLET

### ML LTE Fingerprinter
### Brad Williams · Chris Limson
GMU CYSE 640 Wireless Network Security  
Fall 2024 · Moinul Hossain, PhD  

<img src="images/mullet_fingerprinter.jpg" width="200" height="300">

### System

On AWS Ubuntu nodes, Kubernetes platform orchestration, Docker containerization

These containers are interchangeable with base station hardware:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;MATLAB CLI script (.m) to generate LTE compliant modulated uplink waveform which will include RF fingerprint (RFF) then impairments, simulating device (UE) connection to Evolved Node Base (eNB base station)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Before demodulation, apply filters and OFDM to extract RFF

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;After demodulation eNB will also retrieve UE parameters (genuine, cloned or spoofed) like MAC

GNU Radio (Python) collect RFF Signal Metadata Format (sigMF)

MongoDB (Golang) to store RFF sigMF, and UE metadata

TensorFlow (C++) to apply RFF against Convolutional Neural Network, authenticating RFF, comparing to stored UE, classifying indications


### Experiment

Connect with a defined RFF to our UE

Not found, but RFF and UE stored anyway to contribute DL

Connect again with the following, evaluate results

| RFF       | UE        |
| --------- | --------- |
| different | different |
| different | same      |
| same      | different |
| same      | same      |

Also several trials, several RFFs


---

### Resources
Step-by-step instructions [https://chrimson.github.io/MULLET](https://chrimson.github.io/MULLET)

For download or online with GMU's Campus-Wide License, MATLAB and Simulink https://matlab.mathworks.com  

GNU Radio https://www.gnuradio.org  
On Ubuntu 24.04  
```
sudo apt install gnuradio

gnuradio-companion
```

### More References
[https://repository.library.neu.edu/files/neu:m044c531h/fulltext.pdf](https://repository.library.neu.edu/files/neu:m044c531h/fulltext.pdf)

[https://ece.northeastern.edu/fac-ece/ioannidis/static/pdf/2018/radio_identification.pdf](https://ece.northeastern.edu/fac-ece/ioannidis/static/pdf/2018/radio_identification.pdf)

Improving security of the Internet of Things via RF fingerprinting based device identification system [https://link.springer.com/article/10.1007/s00521-021-06115-2](https://link.springer.com/article/10.1007/s00521-021-06115-2)

https://www.mathworks.com/help/lte/ref/ltewaveformgenerator-app.html?searchHighlight=lte%20impairment&s_tid=srchtitle_support_results_2_lte%20impairment

https://www.mathworks.com/company/technical-articles/measuring-the-impact-of-rf-impairments-on-an-lte-system.html?s_tid=srchtitle_support_results_1_lte%20impairment

Performance Evaluation of LTE Radio Fingerprinting using Field Measurements [https://ieeexplore.ieee.org/document/7454387](https://ieeexplore.ieee.org/document/7454387)

LTE Device Identification Based on RF Fingerprint with Multi-Channel Convolutional Neural Network [https://ieeexplore.ieee.org/document/9685067](https://ieeexplore.ieee.org/document/9685067)

Performance evaluation of LTE radio fingerprint positioning with timing advancing [https://ieeexplore.ieee.org/abstract/document/7459984](https://ieeexplore.ieee.org/abstract/document/7459984)

Radio Frequency Fingerprints Extraction for LTE-V2X: A Channel Estimation Based Methodology [https://arxiv.org/pdf/2301.01446](https://arxiv.org/pdf/2301.01446)

RF fingerprinting for user locationing in LTE/WLAN networks [https://jyx.jyu.fi/handle/123456789/51204#](https://jyx.jyu.fi/handle/123456789/51204#)

Enhanced Device FingerPrinting in 4G LTE Communication Networks [http://drsr.daiict.ac.in/handle/123456789/1055](http://drsr.daiict.ac.in/handle/123456789/1055)

### Documentation
[CYSE640_BradChris_ProjectProposalPresentation.pdf](docs/CYSE640_BradChris_ProjectProposalPresentation.pdf)  
[CYSE640_BradChris_ProjectProposalReport.pdf](docs/CYSE640_BradChris_ProjectProposalReport.pdf)

(below are placeholders for now)  
[CYSE640_BradChris_ProjectFinalPresentation.pdf](docs/CYSE640_BradChris_ProjectFinalPresentation.pdf)  
[CYSE640_BradChris_ProjectFinalReport.pdf](docs/CYSE640_BradChris_ProjectFinalReport.pdf)  

### Notes
[Archive](archive.md)

### License
[MIT](LICENSE)
