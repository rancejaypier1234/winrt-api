---
-api-id: P:Windows.AI.MachineLearning.Preview.LearningModelPreview.Description
-api-type: winrt property
---

<!-- Property syntax.
public ILearningModelDescriptionPreview Description { get; }
-->

# Windows.AI.MachineLearning.Preview.LearningModelPreview.Description

## -description
Gets the descriptive metadata for the trained machine learning model.

## -property-value
The descriptive metadata for the machine learning model.

## -remarks

## -see-also

## -examples
public async Task LoadModel()
{
    var modelFile = await Windows.ApplicationModel.Package.Current.InstalledLocation.GetFileAsync("model.pb");
    LearningModelPreview model = await LearningModelPreview.LoadModelFromStorageFileAsync(modelFile);
 
    // Confirm the version of the model is 1
    if (model.Description.Version != 1)
    {
        throw new Exception("Invalid model version");
    }
}
