---
layout: default
---

## Interpreting Video Features: a Comparison of 3D Convolutional Networks and Convolutional LSTM Networks
Joonatan Mänttäri\*, Sofia Broomé\*, John Folkesson, Hedvig Kjellström. \*Joint authorship

*ACCV 2020, 15th Asian Conference on Computer Vision, to appear.*

This website contains animated figures both from the main article and the supplementary material of our [paper](https://arxiv.org/abs/2002.00367). The hyperparameters used in the work can be found at the bottom of the page.

`@InProceedings{ManttariBroome_2020_Interpreting_Video_Features,                                                                                                               
    title={Interpreting Video Features: a Comparison of 3D Convolutional Networks and Convolutional LSTM Networks},
    author={Joonatan M\"antt\"ari* and Sofia Broom\'e* and John Folkesson and Hedvig Kjellstr\"om},
    year={2020},
    booktitle={Computer Vision - ACCV 2020, 15th Asian Conference on Computer Vision, to appear. (*Joint first authors)},
    month = {December}
}`


If you find the article useful for your research, please cite it.

<iframe width="420" height="315" src="https://www.youtube.com/embed/UScJpd4_B_0" frameborder="0" allowfullscreen></iframe>


**Abstract:** A number of techniques for interpretability have been presented for deep learning in computer vision, typically with the goal of understanding what the networks have actually learned underneath a given classification decision. However, interpretability for deep video architectures is still in its infancy and we do not yet have a clear concept of how to decode spatiotemporal features. In this paper, we present a study comparing how 3D convolutional networks and convolutional LSTM networks learn features across temporally dependent frames. This is the first comparison of two video models that both convolve to learn spatial features but that have principally different methods of modeling time. Additionally, we extend the concept of meaningful perturbation introduced by <a href="http://openaccess.thecvf.com/content_ICCV_2017/papers/Fong_Interpretable_Explanations_of_ICCV_2017_paper.pdf">Fong et al.</a> to the temporal dimension to search for the most meaningful part of a sequence for a classification decision.

## Results samples from main article


Class | Scores I3D | I3D | CLSTM | Scores CLSTM
---- | ---- | ----
Moving something and something away from each other | OS: 0.994<br /> FS: 0.083 <br />RS: 0.856 | ![img](../gifs/resultclips/36/43627/i3d/i3d.gif) | ![img](../gifs/resultclips/36/43627/clstm/clstm.gif) | 0.312<br /> 0.186 <br />0.125
Moving something and something closer to each other  <br/><br/> *Predicted:* <br/> 38: Moving something and something so they collide with each other <br/> 135: Something falling like a rock | OS: 0.547<br /> FS: 0.028 <br />RS: 0.053 <br /> P: 38 | ![img](../gifs/resultclips/37/180193/i3d/i3d.gif) | ![img](../gifs/resultclips/37/180193/clstm/clstm.gif) | 0.257<br /> 0.079 <br />0.122<br/> P: 135
Moving something and something so they pass each other | OS: 0.999<br /> FS: 0.002 <br />RS: 0.414 | ![img](../gifs/resultclips/39/28170/i3d/i3d.gif) | ![img](../gifs/resultclips/39/28170/clstm/clstm.gif) | 0.788<br /> 0.392 <br />0.537
Moving something up | OS: 0.804<br /> FS: 0.016 <br />RS: 0.667 | ![img](../gifs/resultclips/45/125857/i3d/i3d.gif) | ![img](../gifs/resultclips/45/125857/clstm/clstm.gif) | 0.546<br /> 0.121 <br />0.764
Moving something up  <br/><br/> *Predicted:* <br/> 146: Taking one of many similar things on the table <br/> 100: Pushing something so that it slightly moves | OS: 0.685<br /> FS: 0.003 <br />RS: 0.048 <br/> CS: 0.001 <br/>P: 146 | ![img](../gifs/resultclips/45/81536/i3d/i3d.gif) | ![img](../gifs/resultclips/45/81536/clstm/clstm.gif) | 0.221<br /> 0.182 <br />0.350 <br/> CS: 0.005 <br/> P: 100
Pretending to take something from somewhere  <br/><br/> *Predicted:* <br/> 27: Lifting something up completely without letting it drop down | OS: 0.284<br /> FS: 0.003 <br />RS: 0.006 | ![img](../gifs/resultclips/81/46708/i3d/i3d.gif) | ![img](../gifs/resultclips/81/46708/clstm/clstm.gif) | 0.600<br /> 0.167 <br />0.088 <br/> CS: 0.004 <br/> P: 27
Turning the camera downwards while filming something | OS: 1.000<br /> FS: 0.001 <br />RS: 0.011 | ![img](../gifs/resultclips/165/197549/i3d/i3d.gif) | ![img](../gifs/resultclips/165/197549/clstm/clstm.gif) | 0.158<br /> 0.063 <br />0.093 
Turning the camera upwards while filming something | OS: 0.990<br /> FS: 0.001 <br />RS: 0.000 | ![img](../gifs/resultclips/168/215115/i3d/i3d.gif) | ![img](../gifs/resultclips/168/215115/clstm/clstm.gif) | 0.806<br /> 0.177 <br />0.181


## Further Examples of Spatio-temporal Features:

Below, we present results for 22 additional randomly selected sequences (two from each class) from
the Something-something dataset. As mentioned in the main article, we selected eleven classes
where the two models had comparable performance, both poor and strong. The four classes not appearing above are (I3D
F1-score/C-LSTM F1 score): moving something and something so they collide with each other
(0.16/0.03), burying something in something (0.1/0.06), turning the camera left while filming something
(0.94/0.79) and turning the camera right while filming something (0.91/0.8).

Class | Mask Losses I3D | I3D | CLSTM | Mask Losses CLSTM
--- | --- | ---- | ---- | ----
Turning the camera downwards while filming something |OS: 1.000<br/> FS: 0.015<br/> RS: 0.003<br/> | ![img](../gifs/appendixclips/165/12462/i3d/i3d.gif) | ![img](../gifs/appendixclips/165/12462/clstm/clstm.gif) | 0.373<br /> 0.547 <br />0.224

Turning the camera downwards while filming something |OS: 0.999<br/> FS: 0.000<br/> RS: 0.000<br/> | ![img](../gifs/appendixclips/165/213899/i3d/i3d.gif) | ![img](../gifs/appendixclips/165/213899/clstm/clstm.gif) | 0.921<br /> 0.238 <br />0.460

Turning the camera left while filming something |OS: 0.997<br /> FS: 0.012 <br />RS: 0.014 | ![img](../gifs/appendixclips/166/147868/i3d/i3d.gif) | ![img](../gifs/appendixclips/166/147868/clstm/clstm.gif) | 0.988<br /> 0.183 <br />0.105

Turning the camera left while filming something |OS: 0.999<br /> FS: 0.001 <br />RS: 0.451 | ![img](../gifs/appendixclips/166/183031/i3d/i3d.gif) | ![img](../gifs/appendixclips/166/183031/clstm/clstm.gif) | OS: 0.985<br /> FS: 0.229 <br />RS: 0.094

Turning the camera right while filming something <br/><br/> *Predicted:* <br/> 157: Tilting something with something on it until it falls off | OS: .940<br /> FS: 0.106 <br /> RS: 0.017 | ![img](../gifs/appendixclips/167/72679/i3d/i3d.gif) | ![img](../gifs/appendixclips/167/72679/clstm/clstm.gif) | OS: 0.192<br /> FS: 0.261 <br />RS: 0.140 <br/> CS: 0.103 <br/> P: 157

Turning the camera right while filming something | OS: .947<br /> FS: 0.005 <br /> RS: 0.188 | ![img](../gifs/appendixclips/167/130060/i3d/i3d.gif) | ![img](../gifs/appendixclips/167/130060/clstm/clstm.gif) | OS: 0.708<br /> FS: 0.093 <br />RS: 0.119

Turning the camera upwards while filming something | OS: 0.999 <br /> FS: 0.001 <br /> RS: 0.002 | ![img](../gifs/appendixclips/168/191690/i3d/i3d.gif) | ![img](../gifs/appendixclips/168/191690/clstm/clstm.gif) | OS: 0.687<br /> FS: 0.205 <br /> RS: 0.149

Turning the camera upwards while filming something | OS: 0.997<br /> FS: 0.002 <br /> RS: 0.064 | ![img](../gifs/appendixclips/168/40456/i3d/i3d.gif) | ![img](../gifs/appendixclips/168/40456/clstm/clstm.gif) | OS: 0.689<br /> FS: 0.108 <br />RS: 0.129

Moving something and something away from each other <br/><br/> *Predicted:* <br/> 121: Removing something, revealing something behind | OS: 0.917<br /> FS: 0.058 <br />RS: 0.071 | ![img](../gifs/appendixclips/36/192470/i3d/i3d.gif) | ![img](../gifs/appendixclips/36/192470/clstm/clstm.gif) | OS: 0.297<br /> FS: 0.155 <br />RS: 0.294 <br/> CS: 0.085 <br/> P:121

Moving something and something away from each other <br/><br/> *Predicted:* <br/> 130: Showing that something is inside something | OS: 0.991 <br /> FS: 0.022 <br />RS: 0.956 | ![img](../gifs/appendixclips/36/60360/i3d/i3d.gif) | ![img](../gifs/appendixclips/36/60360/clstm/clstm.gif) | OS: 0.259<br /> FS: 0.081 <br />RS: 0.146 <br/> CS: 0.008 <br/> P: 130
Moving something and something closer to each other <br/><br/> *Predicted:* <br/> 173: Wiping something off of something <br/> 100: Pushing something so that it slightly moves |OS: 0.273<br /> FS: 0.004 <br />RS: 0.245 <br/> CS: 0.001 <br/> P:173 | ![img](../gifs/appendixclips/37/134107/i3d/i3d.gif) | ![img](../gifs/appendixclips/37/134107/clstm/clstm.gif) | OS: 0.1230<br /> FS: 0.375 <br />RS: 0.200 <br/> CS: 0.012 <br/> P: 100
Moving something and something closer to each other |OS: 0.932<br /> FS: 0.002 <br />RS: 0.007 | ![img](../gifs/appendixclips/37/94171/i3d/i3d.gif) | ![img](../gifs/appendixclips/37/94171/clstm/clstm.gif) | OS: 0.453<br /> FS: 0.063 <br />RS: 0.198
Moving something and something so they collide with each other |OS: 0.686<br /> FS: 0.003 <br />RS: 0.000 | ![img](../gifs/appendixclips/38/126217/i3d/i3d.gif) | ![img](../gifs/appendixclips/38/126217/clstm/clstm.gif) | OS: 0.620<br /> FS: 0.145 <br />RS: 0.129
Moving something and something so they collide with each other <br/><br/> *Predicted:* <br/> 37: Moving something and something closer to each other| OS: 0.810<br /> FS: 0.055 <br />RS: 0.419 | ![img](../gifs/appendixclips/38/67970/i3d/i3d.gif) | ![img](../gifs/appendixclips/38/67970/clstm/clstm.gif) | OS: 0.333<br /> FS: 0.119 <br /> RS: 0.276 <br/> CS: 0.030 <br/> P:37
Moving something and something so they so they pass each other | OS: 0.997<br /> FS: 0.007 <br /> RS: 0.974 | ![img](../gifs/appendixclips/39/113944/i3d/i3d.gif) | ![img](../gifs/appendixclips/39/113944/clstm/clstm.gif) | OS: 0.737<br /> FS: 0.490 <br /> RS: 0.140
Moving something and something so they so they pass each other  <br/><br/> *Predicted:* <br/> 37: Moving something and something closer to each other| OS: 0.694<br /> FS: 0.010 <br /> RS: 0.003 <br/> CS: 0.273 <br/> P: 37 | ![img](../gifs/appendixclips/39/91016/i3d/i3d.gif) | ![img](../gifs/appendixclips/39/91016/clstm/clstm.gif) | OS: 0.813<br /> FS: 0.227 <br />RS: 0.830 <br/> CS: 0.142 <br/> P: 37
Burying something in something <br/><br/> *Predicted:* <br/> 145: Taking one of many similar things on the table <br/> 157: Tilting something with something on it until it falls off | OS: 0.619<br /> FS: 0.010 <br /> RS: 0.216 <br/> CS: 0.020 <br/> P: 145| ![img](../gifs/appendixclips/4/30133/i3d/i3d.gif) | ![img](../gifs/appendixclips/4/30133/clstm/clstm.gif) | OS: 0.013<br /> FS: 0.079 <br /> RS: 0.262<br/> CS: 0.001 <br/> P: 157
Burying something in something <br/><br/> *Predicted:* <br/> 106: Putting something into something <br/> 5: Closing something |OS: 0.177<br /> FS: 0.007 <br /> RS: 0.130 <br/> CS: 0.027 <br/> P: 106| ![img](../gifs/appendixclips/4/58874/i3d/i3d.gif) | ![img](../gifs/appendixclips/4/58874/clstm/clstm.gif) | OS: 0.112<br /> FS: 0.147 <br />0.327<br/> CS: 0.002 <br/> P: 5
Moving something up  <br/><br/> *Predicted:* <br/> 27: Lifting something up completely without letting it drop down <br/> 100: Pushing something so that it slightly moves| OS: 0.848<br /> FS: 0.065 <br /> RS: 0.380 <br/> CS: 0.003 <br/> P: 27| ![img](../gifs/appendixclips/45/85790/i3d/i3d.gif) | ![img](../gifs/appendixclips/45/85790/clstm/clstm.gif) | OS: 0.229 <br /> FS: 0.102 <br /> RS: 0.269<br/> CS: 0.003 <br/> P: 100
Moving something up <br/><br/> *Predicted:* <br/> 100: Pushing something so that it slightly moves| OS: 0.755<br /> FS: 0.012 <br /> RS: 0.032 | ![img](../gifs/appendixclips/45/96257/i3d/i3d.gif) | ![img](../gifs/appendixclips/45/96257/clstm/clstm.gif) | OS: 0.230<br /> FS: 0.146 <br />RS: 0.200<br/> CS: 0.003 <br/> P: 100
Pretending to take something from somewhere <br/><br/> *Predicted:* <br/> 160: Touching (without moving) part of something | OS: 0.810<br /> FS: 0.019 <br /> RS: 0.682 <br/> CS: 0.000 <br/> P: 160| ![img](../gifs/appendixclips/81/18593/i3d/i3d.gif) | ![img](../gifs/appendixclips/81/18593/clstm/clstm.gif) | OS: 0.179<br /> FS: 0.073 <br /> RS: 0.162<br/> CS: 0.004 <br/> P: 160
Pretending to take something from somewhere <br/><br/> *Predicted:* <br/> 145: Stuffing something into something <br/> 160: Touching (without moving) part of something | OS: 0.325<br /> FS: 0.012 <br /> RS: 0.126<br/> CS: 0.047 <br/> P: 145 | ![img](../gifs/appendixclips/81/7435/i3d/i3d.gif) | ![img](../gifs/appendixclips/81/7435/clstm/clstm.gif) | OS: 0.418<br /> FS: 0.062 <br /> RS: 0.266<br /> CS: 0.011 <br /> P: 160

## Hyperparameters For Experiments

Model (dataset) | Dropout Rate | Weight Decay | Optimizer | Epochs | Momentum 
 ---- | ---- | ---- | ---- | ---- | ---- 
I3D (smth-smth) | 0.5 | 0 | ADAM | 13 | -
I3D (KTH) | 0.7 | 5E-5 | ADAM | 30 | - 
C-LSTM (smth-smth) | 0 | 0 | SGD | 105 | 0.2 
C-LSTM (KTH) | 0.5 | 1E-4 | SGD | 21 | 0.2 

## Hyperparameters For Temporal Mask Inference

Dataset | Lambda1 | Lambda2 | Beta | Optmizer | Iterations | Learning Rate 
 ---- | ---- | ---- | ---- | ---- | ---- 
Smth-Smth | 0.01 | 0.02 | 3 | ADAM | 300 | 0.001 
KTH | 0.02 | 0.04 | 3 | ADAM | 300 | 0.001 


