---
layout: default
title: Basics
nav_order: 2
---

# Basic Terminologies
{: .no_toc }
Below are some of the basic terminologies which can help you further:
1. Face Detection API: Used to detect one or more human faces along with attributes such as: age, emotion, pose, smile, and facial hair, including 27 landmarks for each face in the image. It also detect perceived facial expressions such as anger, contempt, disgust, fear, happiness, neutral, sadness, and surprise. It is important to note that facial expressions alone do not represent the internal states of people.
  ![Face detection api image demo](../../assets/images/face-detect.PNG)
2. Face Verification: Checks the likelihood that two faces belong to the same person and receive a confidence score.
3. Face Similarity: Check if the face given (could be either an image or person) is similar to given face list, large face list, person list, large person list, face Ids passed. If only one face id or image is passed then it'll check for similar faces for all face lists or large face lists available. If you passed many images then you can be able to identify if they are similar to all the persons available. 
4. Face List: You can store list of faces directly into face list
5. Large Face List: Works same as face list but here you can store more than a million of faces.
6. Person Group: Group of known persons, each person can be attributed via name and user data (description).
7. Large Person Group: Works same as Person Group but here more than a billion persons can be stored.
8. Train: You can train person groups, face lists and large face lists to let them find similar photos.
8. Persistent faces: Be default faces will not be percieved for a long time, to make sure the faces will be saved, you need to add them to face list or large face list, person group or large person group which will then save it as persistent face.
{: .fs-6 .fw-300 }

## Limitations
 
1. Image Size: Minimum of 36x36 pixels and maximum of 1920x1080 pixel image.
2. Allowed Image format: JPEG, PNG, GIF (the first frame), and BMP are supported. 
3. Allowed Image sizes: Ranging from 1KB to 6MB.
4. Max Faces: Upto 100 faces can be detected.
5. Our methodology uses recognition_03 model due to its high accuracy.

## API Zones
The API key is been generated according to API Zone pervasive all across the globe. The API key or Ocp Apim Subscription Key related to one zone won't work on another zone, if you're creating app then try to use the API key as an environment variable which would allow you to get the zone specific key and would integrate it easily
- Australia East - australiaeast.api.cognitive.microsoft.com
- Brazil South - brazilsouth.api.cognitive.microsoft.com
- Canada Central - canadacentral.api.cognitive.microsoft.com
- Central India - centralindia.api.cognitive.microsoft.com
- Central US - centralus.api.cognitive.microsoft.com
- East Asia - eastasia.api.cognitive.microsoft.com
- East US - eastus.api.cognitive.microsoft.com
- East US 2 - eastus2.api.cognitive.microsoft.com
- France Central - francecentral.api.cognitive.microsoft.com
- Japan East - japaneast.api.cognitive.microsoft.com
- Japan West - japanwest.api.cognitive.microsoft.com
- Korea Central - koreacentral.api.cognitive.microsoft.com
- North Central US - northcentralus.api.cognitive.microsoft.com
- North Europe - northeurope.api.cognitive.microsoft.com
- South Africa North - southafricanorth.api.cognitive.microsoft.com
- South Central US - southcentralus.api.cognitive.microsoft.com
- Southeast Asia - southeastasia.api.cognitive.microsoft.com
- UK South - uksouth.api.cognitive.microsoft.com
- West Central US - westcentralus.api.cognitive.microsoft.com
- West Europe - westeurope.api.cognitive.microsoft.com
- West US - westus.api.cognitive.microsoft.com
- West US 2 - westus2.api.cognitive.microsoft.com
- UAE North - uaenorth.api.cognitive.microsoft.com


## Face API options
Be default we would provide all the informations listed below, optionally incase you want some of these information then you could send us any of the following options true.
1. Location
Location of the face inside the image mentioned by the name of faceRectangle and the response looks like this:
```json
"faceRectangle": {
  "top": 72,
  "left": 261,
  "width": 130,
  "height": 130
}
```
2. Landmarks
Face landmarks are a set of easy-to-find points on a face, such as the pupils or the tip of the nose. By default, there are 27 predefined landmark points. 27 Points of Universally identified Face landmarks:

![Face Landmarks](../../assets/images/landmarks_what.jpg)

3. Features
Face features can be optionally be detected by the Face - Detect API and contains following:
- Glasses: To tell weather the given face has eyeglasses. Possible values are NoGlasses, ReadingGlasses, Sunglasses, and Swimming Goggles.
- Hair: The hair type of the face. This attribute shows whether the hair is visible, whether baldness is detected, and what hair colors are detected.
- Head pose: The face's orientation in 3D space. This attribute is described by the pitch, roll, and yaw angles in degrees. The value ranges are -90 degrees to 90 degrees, -90 degrees to 90 degrees, and -90 degrees to 90 degrees, respectively. See the following diagram for angle mappings:
```A head with the pitch, roll, and yaw axes labeled```
- Makeup: Whether the face has makeup. This attribute returns a Boolean value for eyeMakeup and lipMakeup.
- Accessories: To tell if the person in the photo have wore any accessories and if yes then what can be they.
- Facial hairs: The estimated facial hair presence and the length for the given face.

4. Emotions
It contains different emotions of the personas we can observe inside the photo and it contains following:
 - Smile: Encounters the probability of person in the picture to smile. This value is between zero for no smile and one for a clear smile.
 - Emotions: Encounters the probability of mixture of emotions we can observe inside the picture. A list of emotions with their detection confidence for the given face. Confidence scores are normalized, and the scores across all emotions add up to one. The emotions returned are happiness, sadness, neutral, anger, contempt, disgust, surprise, and fear.

5. Characterstics:
 - Age: The estimated age in years of a particular face.
 - Gender: The estimated gender of the given face. Possible values are male, female, and genderless.

6. Noises:
 - Blur: The blurriness of the face in the image. This attribute returns a value between zero and one and an informal rating of low, medium, or high.
 - Exposure: The exposure of the face in the image. This attribute returns a value between zero and one and an informal rating of underExposure, goodExposure, or overExposure.
 - Noise: The visual noise detected in the face image. This attribute returns a value between zero and one and an informal rating of low, medium, or high.
- Occlusion: Whether there are objects blocking parts of the face. This attribute returns a Boolean value for eyeOccluded, foreheadOccluded, and mouthOccluded.

---

View the [original documentation at Microsoft Website](https://github.com/pmarsceill/just-the-docs/tree/master/_config.yml).