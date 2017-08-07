***Q: Why does SSD use several differently sized feature maps to predict detections?***

A: 

Differently sized feature maps allow for the network to learn to detect objects at different
resolutions. This is illustrated in the figure with the 8x8 and 4x4 feature maps. This may remind you
of skip connections in fully convolutional networks.