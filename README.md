<html>
  <head><h1># llm</h1></head>
<body>
<p>This is the sart of my llm projetcs ;currently there are 2 projects</p>

<br>
<p>1 ."chatbot_gguf" is a jupyter notebook run locally on my pc based off the codellama-7b-instruct.Q2_K.gguf model .Its supposed to generate python code for a text prompt provided .As shown in the results for it however , it was highly inaccurate due to the version used which brings me to my second project:-</p>
<p>Instructions to run the model are as follows :-
<br>
a.Download chatbot_gguf.ipynb jupyter notebook from the directory . It scontains the entire script of downloads except for the model which i will show how to download and change the code .
<br>
b.Download the model "codellama-7b-instruct.Q2_K.gguf "(or any gguf model you wish to download from hugging face or github.the link is https://huggingface.co/TheBloke/CodeLlama-7B-Instruct-GGUF/blob/main/codellama-7b-instruct.Q2_K.gguf
  ensure that your jupyter ntbk and this model are in same directory 
  additional download scripts <br>
  !pip install gradio<br>
!pip install ctransformers
<br>
c.while defining the model instead of<br>
  def load_model():<br>
    model = AutoModelForCausalLM.from_pretrained(<br>
        "codellama-7b-instruct.Q2_K.gguf",#//put the path to your model here<br> 
        model_type='llama',#//type here<br>
        max_new_tokens=64 #//the number of tokens you wish to train your model on , more tokens better chance to be accurate for longer prompts<br>
    )<br>
    return model<br>
d. You can run my model here on the cloud on google colab link : 
  <br>
e.It should look something like this : <br>
  ![image](https://github.com/aamod-wick/llm/assets/130042477/aa1020ee-bb03-4fa0-8f79-c5c112174399)

</p>
<br>

<p>2 ."finetune_llama2" is a colab project aiming to use a free T4 gpu to finetune llama , currently im in the process of finetuning it and have already prepared the dataset under the header of "finetune_llama_dataset" the conext taken is quite small to decrease my idle time ,and the dataset values have been filtered .</p>
</body>
</html>
