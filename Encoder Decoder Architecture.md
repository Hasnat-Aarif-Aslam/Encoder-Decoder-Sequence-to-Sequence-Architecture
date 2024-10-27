# **in the encoder part, we can either use LSTM or GRU not RNNS because they cause VANISHING GRADIENT PROBLEM**
![{C7777BE8-FCC8-4D7A-8C29-6CA98F235E9C}](https://github.com/user-attachments/assets/d3cd8289-6285-4c90-91e6-aa93e2053887)


# **This image shows the encoder section, let's say we had 1 lstm cell in encoder when we UNFOLD IT THROUGH TIME, we got something like that for the sentence we use 'NICE TO MEET YOU'**

# **FOR EACH TIME STEP WE GOT THIS STRUCTURE, the hidden state and cell state of each cell becomes the input to the next cell**

# **and at the end what we got is the `CONTEXT VECTOR`**
![{205581FC-58CF-48B6-AE25-1DE61182F8C5}](https://github.com/user-attachments/assets/ba1c69b7-1a49-4e39-8afb-7284cf42c8fe)



# **DECODER SECTION**

# **We provide that context vector to the decoder, and provide it a special symbol < START >, as the decoder encounters it, it starts to produce the sequences**

# **THE FIRST SEQUENCE IT HAS PRODUCED WILL BE GIVEN AS AN INPUT TO THE NEXT CELL, AND THE OUTPUT SEQUENCE THAT CELL WILL PRODUCE WILL BE GIVEN AS AN INPUT TO THE NEXT CELL AND SO ON...**

# **at the end, when it encoutners < END >, it stops producing the sequences**
![{9C9F73D4-B249-4E12-9580-D3B7B16E3CE5}](https://github.com/user-attachments/assets/1b856820-0164-4718-8d35-beef43677278)



# **TRAINING ENCODER DECODER**

# **keep this in front of you when training it, THEY ARE TRAINED SIDE BY SIDE (NOT ENCODER FIRST AND DECODER LATER)**
![{659CF670-B62E-49B3-A7F1-44BBA55D20E8}](https://github.com/user-attachments/assets/65747cee-06dd-4821-8048-4db5b8c3d3be)

# **LETS SAY WE HAVE THE DATASET OF ENG TO HINDI SENTENCES, WE WILL FIRST CONVERT IT TO NUMBERS, HERE WE USED OHE**
![{7E7C36E3-2AA6-4BF9-87AE-919557BB78F6}](https://github.com/user-attachments/assets/461b83b7-658c-4b2a-83dd-9196fb56d342)


# **FORWARD PROP**

# **Here At time-step 1: our model has output wrong prediction, so RATHER THAN GIVING THIS OUTPUT AS AN INPUT TO THE NEXT TIME STEP, WE USE THE ACTUAL OUTPUT & GIVE THAT TO THE NEXT TIME STEP**

# **this is called `TEACHER FORCING`**

# **IF WE GIVE OUR MODEL THE WRONG PREDICTIONS, IT WILL leads to problems like slow convergence, model instability, and poor skilL**
![{7D18D66F-5368-4D6F-8A87-305DE5F80078}](https://github.com/user-attachments/assets/a14773c5-335b-4ac4-81fa-da705f0ce6bf)



# **CALCULATING LOSS**
# **HERE WE HAVE CALCULATED LOSS**
![{CB185105-20EA-4C60-A6EB-F1B7EB8EE571}](https://github.com/user-attachments/assets/99d7537a-a1f9-4807-be8e-1e65e6e52434)


# **BACK PROP**
![{C1DE82A7-5850-4726-9DE6-8F59C8684899}](https://github.com/user-attachments/assets/cef5ae70-4728-425d-b73b-e61e7fc3116e)


# **PREDICTION**
# **during prediction, we will use the output of the cell at time step 0 as an input to the next cell, WE CAN'T DO TEACHER FORCING HERE BECAUSE WE DONT HAVE THE CORRECT OUTPUTS**

# **teacher forcing is only in TRAINING**
![{47F44CE8-7D5A-4F60-B728-723B8510D493}](https://github.com/user-attachments/assets/5be42f16-44c6-436b-8e0d-7d15c832f9d3) ![{3BBE05E8-785D-422D-877E-9FB3B5A5D36C}](https://github.com/user-attachments/assets/0f2d7b08-d8a5-4b86-be42-16573bdfb6c4)


# **EMBEDDINGS**

# **IT'S ALWAYS BETTER TO USE EMBEDDINGS**

# **THINK ABOUT IT, WILL PASS THROUGH EMBEDDING LAYER AND THEN TO THE ENCODER, similarly in decoder, < start > will pass through embedding and then through decoder, similarly for other time steps**
![{0853270D-A5D8-4A9F-960C-ACD4C526DCE3}](https://github.com/user-attachments/assets/614503f3-d707-4052-9fbc-c86bb394ebcf)

![{0222F31A-E00B-4B4B-872E-A22915CF693C}](https://github.com/user-attachments/assets/bde03aa4-d539-4466-beb4-1f7c927286ca)


# **DEEP LSTSM OR GRUS**

# **CAN HANDLE LONG TERM DEPENDENCIES: it means they can handle long sentences, paragraphs etc**

# **LAYERS REPRESENTATION: the lower layers will understand words, meanings, grammar etc (things at lower lvl), upper layers will handle sentences, upper layers will handle paragraphs etc**
![{78CFB21A-AE62-47DC-BA88-8FA0BDC4A7EE}](https://github.com/user-attachments/assets/ae2c378e-ac60-4b09-a88e-38d455e50b62)










