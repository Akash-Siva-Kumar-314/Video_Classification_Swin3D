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

I decided to work more with the 'PyTorchVideo DataLoader + Swin3D' model.

Study05.1.1_PyTorchVideoDataLoader_Swin3D_ToSaveTrainedModel.ipynb  
Saved the Trained Model.

Study05.1.2_PyTorchVideoDataLoader_Swin3D_CallingAndUsingTrainedModel.ipynb  
Called the saved model, to do a single Inference.

Study05.1.3_PyTorchVideoDataLoader_Swin3D_CallingAndUsingTrainedModel_SortingAllVideos.ipynb  
This reads a bunch of videos and then sorts it according to predicted into respective folders.

Now the problem was, it sorts any video into running or walking. What if the video is neither scenario?  
So created a miscellaneous class as well, that catches miscellaneous videos.  
All Study05.1 was modified to account for this, and named Study05.2.

Study05.2.1_PyTorchVideoDataLoader_Swin3D_ToSaveTrainedModel_MiscIncluded
Study05.2.2_PyTorchVideoDataLoader_Swin3D_CallingAndUsingTrainedModel_MiscIncluded
Study05.2.3_PyTorchVideoDataLoader_Swin3D_CallingAndUsingTrainedModel_SortingAllVideos_MiscIncluded

I tried this Swin3D code to do actual work, but it is super slow.  
Did some study,  
Swin3D is a Video Transformer so it takes time to train while,  
Slow-R50 and x3d are 3D CNN so more lightweight.  

In order of speed: x3d, Slow-R50, Swin3D.


