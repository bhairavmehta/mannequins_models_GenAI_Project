Converting Mannequins into models:

Description:
This project was to converting mannequins into real life models. To lower the cost of seller as they pay for the photoshoot with models.
https://colab.research.google.com/drive/1VU0sQ99VHOj2j0vXMHkXwr0O-AAc7v6h?usp=sharing

Models for detection and segmentation:-
We will be using grounding dino(https://github.com/IDEA-Research/GroundingDINO) and segment anything model( https://github.com/facebookresearch/segment-anything) for generating masks for the inpainting. 
Grounded-segment-anytging(https://github.com/IDEA-Research/Grounded-Segment-Anything) will be used for creating the mask of mannequin body and head.
Now , we will use cloth segmentation model based on u2net for the segmentation of cloth(https://github.com/wildoctopus/huggingface-cloth-segmentation).

Mask creation:-
Mask creation, (head mask + person mask) - cloth_segmentation.
Head mask will be created with head detection and converting detection box into the mask. Person mask is created with the persondetection and  segmentation.
Last cloth segmentation will be created with u2net pretrained model by wildoctopis.

Image generation using diffusion :-
Now, we will pass the image and mask created with the stable diffusion models juggernautxl(finetuned version of sdxl which gives photorealistic image)
https://huggingface.co/stablediffusionapi/juggernaut-xl
https://civitai.com/models/133005/juggernaut-xl
 and realisticvision6(finetuned version of sd1.5) 
https://huggingface.co/SG161222/Realistic_Vision_V6.0_B1_noVAE
https://civitai.com/models/4201/realistic-vision-v60-b1
.then, we will use the fooocus api(https://github.com/konieshadow/Fooocus-API) with these models which has lora and ip adapters which makes the generarion more perfect.
Fooocus api is a docker image of the image generarion software Fooocus(https://github.com/lllyasviel/Fooocus).
Here are the resulting images:-


