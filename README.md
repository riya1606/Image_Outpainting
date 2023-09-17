# Image Outpainting Project
## Objective
This computer vision project addresses the challenge of extending images beyond their original boundaries, creating a realistic and visually coherent expansion.
## Methodology
<p>
While common inpainting methods employ Generative Adversarial Networks (GANs) and Convolutional Neural Networks (CNNs), this project focuses on outpainting, which extrapolates beyond image boundaries. It involves a completion network and two auxiliary context discriminators, used exclusively for training and not during testing.
</p>
<p>
Network Components: The architecture includes:
- Completion Network: Responsible for extending images beyond their boundaries.
- Global Discriminator Network: Evaluates full images to determine if they are real or completed.
- Local Discriminator Network: Focuses on small regions around the finished area to assess realism.
</p>

## Training
Both discriminator networks are trained to distinguish real images from those completed by the network, while the completion network is trained to deceive both discriminators. This comprehensive training enables the completion network to produce visually plausible extensions.
**Architecture Efficacy:** The project relies on sophisticated convolutional neural networks for image extension, utilizing a single completion network. However, to ensure appropriate image completion, two additional networks—global and local setting discriminator networks—are used in tandem. This strategic combination enables the completion network to generate realistic extensions. 


## Dataset

**Source**: The dataset employed in this project is the renowned Places365 dataset, meticulously curated by MIT. Originally intended for CNNs to facilitate scene feature recognition, it aligns well with the project's requirements.
**Data Selection**: From the Places365 dataset, we specifically extracted a substantial number of beach images. These beach images served as the primary dataset for our model. A total of 3500 beach images were used for training over 25 epochs.

## Experimental Results

**DCGAN Implementation:** We successfully implemented a Deep Convolutional Generative Adversarial Network (DCGAN) architecture, enabling the generation of images up to a resolution of 256 x 256 pixels.

**Image Resizing:** To handle various input image sizes, we extensively utilized the OpenCV library in Python for image resizing, ensuring compatibility with our model.

**Framework:** The project's architecture was predominantly developed using Keras, providing flexibility for incorporating multiple convolution layers within the network and working with larger image sizes.

**Outcome:** The outcomes of our experiments yielded impressive results, demonstrating the effectiveness of our DCGAN-based image generation approach.

## Results
<img width="496" alt="image" src="https://github.com/riya1606/Image_Outpainting/assets/62128029/19b16231-1197-4367-8d3b-0e1f270d93b8">

## Conclusion
In conclusion, we have successfully developed a comprehensive end-to-end Generative Adversarial Network (GAN) capable of addressing image outpainting challenges. Our deep neural network implementation extends images up to 256 × 256 pixels, producing high-quality results. By introducing a local discriminator in addition to the global discriminator, we achieved near-ideal image outputs. Future work could involve expanding the project's capabilities to accept larger input image sizes and enhancing image resolution, contingent on increased computational resources.
