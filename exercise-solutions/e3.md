***Q: What are some ways which we can filter nonsensical bounding boxes?***

A: 

You may have come up with different answers. The SSD paper does 2 things:

1. Filters boxes based on IoU metric. For example, if a box has an IoU score
less than 0.5 on all ground truth boxes it's removed.

2. *Hard negative mining*. This is a fancy way of saying "search for negatives examples
the highest confidence". For example, a box that misclassifies a dog as a cat with 80% confidence.
The authors of the SSD paper limit the positive to hard negative ratio to 3:1 at most. The actual positive to negative ratio is typically much higher and the number of boxes are typically reduced substantially.