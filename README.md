<html>
  <head><h1># llm</h1></head>
<body>
<p>This is the sart of my llm projetcs ;currently there are 3 projects</p>

<br><br>
<p>1 ."chatbot_gguf" is a jupyter notebook run locally on my pc based off the codellama-7b-instruct.Q2_K.gguf model .Its supposed to generate python code for a text prompt provided .As shown in the results for it however , it was highly inaccurate due to the version used which brings me to my second project:-</p>
<p>Instructions to run the model are as follows :-
<br>
a.Download chatbot_gguf.ipynb jupyter notebook from the directory . It scontains the entire script of downloads except for the model which i will show how to download and change the code .
<br><br>
b.Download the model "codellama-7b-instruct.Q2_K.gguf "(or any gguf model you wish to download from hugging face or github.the link is https://huggingface.co/TheBloke/CodeLlama-7B-Instruct-GGUF/blob/main/codellama-7b-instruct.Q2_K.gguf<br><br>
  ensure that your jupyter ntbk and this model are in same directory 
  additional download scripts <br>
  !pip install gradio<br>
!pip install ctransformers
<br><br>
c.while defining the model instead of<br>
  def load_model():<br>
    model = AutoModelForCausalLM.from_pretrained(<br>
        "codellama-7b-instruct.Q2_K.gguf",#//put the path to your model here<br> 
        model_type='llama',#//type here<br>
        max_new_tokens=64 #//the number of tokens you wish to train your model on , more tokens better chance to be accurate for longer prompts<br>
    )<br>
    return model<br>
  <br><br>
d.It should look something like this : <br>
  ![image](https://github.com/aamod-wick/llm/assets/130042477/aa1020ee-bb03-4fa0-8f79-c5c112174399)


<br><br>
e.This is best run for cpu only pcs . I f you have a gpu i recommend using gptq to inference on your personal machine <br><br>
</p>
<p>2 ."finetune_llama2" is a colab project aiming to use a free T4 gpu to finetune llama , currently im in the process of finetuning it and have already prepared the dataset under the header of "finetune_llama_dataset" the conext taken is quite small to decrease my idle time ,and the dataset values have been filtered .</p>
<p>3.Gemma_2b_finetune.ipynb is a colab project aiming to use a free T4 gpu to fine tune googles gemma 2b model and using LoRA and PEFT to quantise the llm to run on the free hardware provided by colab .The data set taken is a famous hugging face dataset "data bricks dolby" .<br><br>
The model has been trained on the a  modified version of the dataset and the training parameters are shown in this colab notebook along with the entire model code in this colab notebook here https://colab.research.google.com/drive/1nHGjj5adCYu_NYO0afh15IQc5ZjVslph?usp=sharing.<br><br>
To execute it on your local machine you would need basic packages and the model installed to load it in unless you could do it through hugging face login itself .The hugging face login credentials in the colab code are my own , please remember to change the username and token when you try to use or run the project yourself on your own notebook if you so desire .
colab link https://colab.research.google.com/drive/1nHGjj5adCYu_NYO0afh15IQc5ZjVslph?usp=sharing<br><br>
training/loss graph ![image](https://github.com/aamod-wick/llm/assets/130042477/ae9c8524-f99d-48ea-a2e0-79e268fcb56c)

  
</p>
</body>
</html>
