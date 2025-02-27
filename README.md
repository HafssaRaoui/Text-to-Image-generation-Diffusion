# 🎨 Text-to-Image Generation with Diffusers
## 🤔 What's all this project is about ? 
This project explores diffusion models for **text-to-image** generation using the ```diffusers``` library. 
We experiment with different models, parameters,
and prompts to understand how diffusion models reconstruct images from noise. 

## ⚡ Installation
Make sure to install the following dependencies :
```
pip install diffusers transformers accelerate torch matplotlib 
```

## 🧠 How Do Diffusion Models Work?
* First of all Diffusion models are **generative ML models** , just like GANs , and VAEs (actually
  it is composed of a VAE )
  * The **interesting** thing about diffusion models is that they can generate an image from scratch
  * One more important fund to keep in mind : The model uses ```Markov chain``` to remove ```noise``` and reconstruct the
    original one

  ### 🌀 But here we go what does all that actually mean ?

  Diffusion models work by replicating the diifusion process which conists on :
  - taking an image as an input
  - adding noise to this image
  - and then learnign how to reverse this noise process


  So naturally we will find ourselves transiting from a state to another , that's why we say that the noise
  is applied following the Markov chain  (browse the equation , not very scary 😎)

  ### 💪 Training the model

  when we jump from a state to another , aka from less noiser image to another we apply the gradient descent optimization,
  the goal is to optimize the difference between previous step (image before noise) and the added noise image

  ![image](https://github.com/user-attachments/assets/d3811926-a883-4b93-83a1-a02e0cab7752)


  
  ### ↩️ What about inference ?
the idea consists on reconstructing an image from  the  Gaussian noise  which meeans reconstructing an image from the previously reconstructed data.
![image](https://github.com/user-attachments/assets/c8a84164-7b4a-44e6-a110-557fef989e50)
  https://colab.research.google.com/github/huggingface/notebooks/blob/main/diffusers/diffusers_intro.ipynb


  ### 👀 Want to see it in action? [Open the Jupyter notebook](https://github.com/HafssaRaoui/Text--to-Image-generation-Diffusion/blob/master/Text_to_Image_generation_with_LLM_hugging_face.ipynb) 📓 to dive into text-to-image generation and experiment with pipeline parameters! 🎨🖌️💡


  
