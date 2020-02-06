---
layout: default
---

## Interpreting Video Features: a Comparison of 3D Convolutional Networks and Convolutional LSTM Networks
A number of techniques for interpretability have been presented for deep learning in computer vision, typically with the goal of understanding what the networks have actually learned underneath a given classification decision. However, interpretability for deep video architectures is still in its infancy and we do not yet have a clear concept of how to decode spatiotemporal features. In this paper, we present a study comparing how 3D convolutional networks and convolutional LSTM networks learn features across temporally dependent frames. This is the first comparison of two video models that both convolve to learn spatial features but that have principally different methods of modeling time. Additionally, we extend the concept of meaningful perturbation introduced by <a href="http://openaccess.thecvf.com/content_ICCV_2017/papers/Fong_Interpretable_Explanations_of_ICCV_2017_paper.pdf">Fong et al.</a> to the temporal dimension to search for the most meaningful part of a sequence for a classification decision.

## Results samples from main article


Class | Scores I3D | I3D | CLSTM | Scores CLSTM
---- | ---- | ----
Moving something and something away from each other | OS: 0.994<br /> FS: 0.083 <br />RS: 0.856 | ![img](../gifs/resultclips/36/43627/i3d/i3d.gif) | ![img](../gifs/resultclips/36/43627/clstm/clstm.gif) | 0.312<br /> 0.186 <br />0.125
Moving something and something closer to each other | OS: 0.547<br /> FS: 0.028 <br />RS: 0.053 <br /> P: 38 | ![img](../gifs/resultclips/37/180193/i3d/i3d.gif) | ![img](../gifs/resultclips/37/180193/clstm/clstm.gif) | 0.257<br /> 0.079 <br />0.122<br/> P: 135
Moving something and something so they pass each other | OS: 0.999<br /> FS: 0.002 <br />RS: 0.414 | ![img](../gifs/resultclips/39/28170/i3d/i3d.gif) | ![img](../gifs/resultclips/39/28170/clstm/clstm.gif) | 0.788<br /> 0.392 <br />0.537
Moving something up | OS: 0.804<br /> FS: 0.016 <br />RS: 0.667 | ![img](../gifs/resultclips/45/125857/i3d/i3d.gif) | ![img](../gifs/resultclips/45/125857/clstm/clstm.gif) | 0.546<br /> 0.121 <br />0.764
Moving something up | OS: 0.685<br /> FS: 0.003 <br />RS: 0.048 <br/> CS: 0.001 <br/>P: 146 | ![img](../gifs/resultclips/45/81536/i3d/i3d.gif) | ![img](../gifs/resultclips/45/81536/clstm/clstm.gif) | 0.221<br /> 0.182 <br />0.350 <br/> CS: 0.005 <br/> P: 100
Pretending to take something from somewhere | OS: 0.284<br /> FS: 0.003 <br />RS: 0.006 | ![img](../gifs/resultclips/81/46708/i3d/i3d.gif) | ![img](../gifs/resultclips/81/46708/clstm/clstm.gif) | 0.600<br /> 0.167 <br />0.088 <br/> CS: 0.004 <br/> P: 27
Turning the camera downwards while filming something | OS: 1.000<br /> FS: 0.001 <br />RS: 0.011 | ![img](../gifs/resultclips/165/197549/i3d/i3d.gif) | ![img](../gifs/resultclips/165/197549/clstm/clstm.gif) | 0.158<br /> 0.063 <br />0.093 
Turning the camera upwards while filming something | OS: 0.990<br /> FS: 0.001 <br />RS: 0.000 | ![img](../gifs/resultclips/168/215115/i3d/i3d.gif) | ![img](../gifs/resultclips/168/215115/clstm/clstm.gif) | 0.806<br /> 0.177 <br />0.181


## Further Examples of Spatio-temporal Features:

Class | Mask Losses I3D | I3D | CLSTM | Mask Losses CLSTM
---- | ---- | ----
Turning the camera downwards while filming something |.000<br /> 0.000 <br />0.000 | ![img](../gifs/appendixclips/165/12462/i3d/i3d.gif) | ![img](../gifs/appendixclips/165/12462/clstm/clstm.gif) | 0.000<br /> 0.000 <br />0.000
Turning the camera downwards while filming something |.000<br /> 0.000 <br />0.000 | ![img](../gifs/appendixclips/165/213899/i3d/i3d.gif) | ![img](../gifs/appendixclips/165/213899/clstm/clstm.gif) | 0.000<br /> 0.000 <br />0.000
Turning the camera left while filming something |.000<br /> 0.000 <br />0.000 | ![img](../gifs/appendixclips/45/85790/i3d/i3d.gif) | ![img](../gifs/appendixclips/45/85790/clstm/clstm.gif) | 0.000<br /> 0.000 <br />0.000
Turning the camera left while filming something |.000<br /> 0.000 <br />0.000 | ![img](../gifs/appendixclips/45/85790/i3d/i3d.gif) | ![img](../gifs/appendixclips/45/85790/clstm/clstm.gif) | 0.000<br /> 0.000 <br />0.000
Turning the camera right while filming something |.000<br /> 0.000 <br />0.000 | ![img](../gifs/appendixclips/45/85790/i3d/i3d.gif) | ![img](../gifs/appendixclips/45/85790/clstm/clstm.gif) | 0.000<br /> 0.000 <br />0.000
Turning the camera right while filming something |.000<br /> 0.000 <br />0.000 | ![img](../gifs/appendixclips/45/85790/i3d/i3d.gif) | ![img](../gifs/appendixclips/45/85790/clstm/clstm.gif) | 0.000<br /> 0.000 <br />0.000
Turning the camera upwards while filming something |.000<br /> 0.000 <br />0.000 | ![img](../gifs/appendixclips/45/85790/i3d/i3d.gif) | ![img](../gifs/appendixclips/45/85790/clstm/clstm.gif) | 0.000<br /> 0.000 <br />0.000
Turning the camera upwards while filming something |.000<br /> 0.000 <br />0.000 | ![img](../gifs/appendixclips/45/85790/i3d/i3d.gif) | ![img](../gifs/appendixclips/45/85790/clstm/clstm.gif) | 0.000<br /> 0.000 <br />0.000
Moving something and something away from each other |.000<br /> 0.000 <br />0.000 | ![img](../gifs/appendixclips/45/85790/i3d/i3d.gif) | ![img](../gifs/appendixclips/45/85790/clstm/clstm.gif) | 0.000<br /> 0.000 <br />0.000
Moving something and something away from each other |.000<br /> 0.000 <br />0.000 | ![img](../gifs/appendixclips/45/85790/i3d/i3d.gif) | ![img](../gifs/appendixclips/45/85790/clstm/clstm.gif) | 0.000<br /> 0.000 <br />0.000
Moving something and something closer to each other |.000<br /> 0.000 <br />0.000 | ![img](../gifs/appendixclips/45/85790/i3d/i3d.gif) | ![img](../gifs/appendixclips/45/85790/clstm/clstm.gif) | 0.000<br /> 0.000 <br />0.000
Moving something and something closer to each other |.000<br /> 0.000 <br />0.000 | ![img](../gifs/appendixclips/45/85790/i3d/i3d.gif) | ![img](../gifs/appendixclips/45/85790/clstm/clstm.gif) | 0.000<br /> 0.000 <br />0.000
Moving something and something so they collide with each other |.000<br /> 0.000 <br />0.000 | ![img](../gifs/appendixclips/45/85790/i3d/i3d.gif) | ![img](../gifs/appendixclips/45/85790/clstm/clstm.gif) | 0.000<br /> 0.000 <br />0.000
Moving something and something so they collide with each other |.000<br /> 0.000 <br />0.000 | ![img](../gifs/appendixclips/45/85790/i3d/i3d.gif) | ![img](../gifs/appendixclips/45/85790/clstm/clstm.gif) | 0.000<br /> 0.000 <br />0.000
Moving something and something so they so they pass each other |.000<br /> 0.000 <br />0.000 | ![img](../gifs/appendixclips/45/85790/i3d/i3d.gif) | ![img](../gifs/appendixclips/45/85790/clstm/clstm.gif) | 0.000<br /> 0.000 <br />0.000
Moving something and something so they so they pass each other |.000<br /> 0.000 <br />0.000 | ![img](../gifs/appendixclips/45/85790/i3d/i3d.gif) | ![img](../gifs/appendixclips/45/85790/clstm/clstm.gif) | 0.000<br /> 0.000 <br />0.000
Burying something in something |.000<br /> 0.000 <br />0.000 | ![img](../gifs/appendixclips/45/85790/i3d/i3d.gif) | ![img](../gifs/appendixclips/45/85790/clstm/clstm.gif) | 0.000<br /> 0.000 <br />0.000
Burying something in something |.000<br /> 0.000 <br />0.000 | ![img](../gifs/appendixclips/45/85790/i3d/i3d.gif) | ![img](../gifs/appendixclips/45/85790/clstm/clstm.gif) | 0.000<br /> 0.000 <br />0.000
Moving something up | .000<br /> 0.000 <br />0.000 | ![img](../gifs/appendixclips/45/85790/i3d/i3d.gif) | ![img](../gifs/appendixclips/45/85790/clstm/clstm.gif) | 0.000<br /> 0.000 <br />0.000
Moving something up | .000<br /> 0.000 <br />0.000 | ![img](../gifs/appendixclips/45/96257/i3d/i3d.gif) | ![img](../gifs/appendixclips/45/96257/clstm/clstm.gif) | 0.000<br /> 0.000 <br />0.000
Pretending to take something from somewhere| .000<br /> 0.000 <br />0.000 | ![img](../gifs/appendixclips/45/85790/i3d/i3d.gif) | ![img](../gifs/appendixclips/45/85790/clstm/clstm.gif) | 0.000<br /> 0.000 <br />0.000
Pretending to take something from somewhere| .000<br /> 0.000 <br />0.000 | ![img](../gifs/appendixclips/45/96257/i3d/i3d.gif) | ![img](../gifs/appendixclips/45/96257/clstm/clstm.gif) | 0.000<br /> 0.000 <br />0.000

