Study 1: Skeleton code for video classification using Swin3D.

Study 2: Studied the video manipulation function form Study 1, deconstructed it to legible blocks and tried on a single video.

Study 3.1: Skeleton Study 1 works good, so trying another model x3d.

Study 3.2: Skeleton Study 1 works good, so trying another model pyslowfast.

Study 4: Skeleton is good, now taking out the manual data processing block and replacing with PyTorchVideo DataLoader. Using model Slow-R50, this combination is a native PyTorchVideo approach.

Study 5: Using PyTorchVideo DataLoader and Swin3D model combined.

Conclusion on my small dataset:

Manually processed data + Swin3D , CONFIDENCE: 57.16%

Manually processed data + x3d , CONFIDENCE: 80.39%

Manually processed data + pyslowfast , CONFIDENCE: 90.40%

PyTorchVideo DataLoader + Slow-R50 , CONFIDENCE: 96.66% (100%native'PyTorchVideo'way)

PyTorchVideo DataLoader + Swin3D , CONFIDENCE: 100.00%

.


