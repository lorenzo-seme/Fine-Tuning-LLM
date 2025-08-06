Python pipeline to finetune a LLM with some input output examples.
Input and outputs must be a JSON file with the following structure:

[
  {
    "input": "What are some reliable starter houseplants for beginners?",
    "output": "Easy-care plants like ZZ Plant, Pothos, Spider Plant, and Snake Plant are ideal for beginners—they tolerate low light and occasional neglect." 
  },
  {
    "input": "How can busy people maintain healthy houseplants?",
    "output": "Choose low-maintenance species and water only when the soil is dry. Succulents or hardy foliage plants can thrive with minimal effort." 
  },
  {
    "input": "How do you know when to water indoor plants?",
    "output": "Tap the pot side—if it sounds hollow, soil is likely dry. Avoid watering on a schedule; check moisture manually instead." 
  }
]

Finetuning is done using LoRA technique. You can set the name of the model you want to finetune, for example:

model_name = "unsloth/SmolLM-135M"

At the end of the pipeline you get the finetuned model and the finetuned and quantized model.
