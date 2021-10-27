# AzureKinectBodyTracking  
## Install sdk  
 - Azure Kinect sensor sdk  
https://github.com/microsoft/Azure-Kinect-Sensor-SDK/blob/develop/docs/usage.md  
 - Body-sdk  
https://docs.microsoft.com/bs-latn-ba/azure/Kinect-dk/body-sdk-download  
 - Nvidia Cuda  
https://developer.nvidia.com/cuda-gpus 
  
## Import libraries  
See tutorial from  
 - https://github.com/microsoft/Azure-Kinect-Samples/tree/master/body-tracking-samples/sample_unity_bodytracking  
 - https://channel9.msdn.com/Shows/Mixed-Reality/Azure-Kinect-Body-Tracking-Unity-Integration
  
## Modify SkeletalTrackingProvider.cs  
1. Open SkeletalTrackingProvider.cs
2. Modify line 46, If you are already install Nvidia Cuda, you can change TrackerProcessingMode to Cuda.
  ```
  using (Tracker tracker = Tracker.Create(deviceCalibration, new TrackerConfiguration() { ProcessingMode = TrackerProcessingMode.Gpu, SensorOrientation = SensorOrientation.Default   }))
  ```  
  Change `TrackerProcessingMode.Gpu` to `TrackerProcessingMode.Cuda` or `TrackerProcessingMode.Cpu`  
    
3. Scenes/Kinect4AzureSampleScene press play.  
  
## Reference  
 - AzureKinect-BodyTracking tutorial  
https://channel9.msdn.com/Shows/Mixed-Reality/Azure-Kinect-Body-Tracking-Unity-Integration  
 - AzureKinectで"sample_unity_bodytracking"を動かすまでのお話  
https://qiita.com/Tuyoshi/items/343ce116d11e0cc9b797
  
  
