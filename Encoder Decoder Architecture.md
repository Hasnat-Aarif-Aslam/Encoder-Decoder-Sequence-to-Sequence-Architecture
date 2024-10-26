# **in the encoder part, we can either use LSTM or GRU not RNNS because they cause VANISHING GRADIENT PROBLEM**
![{C7777BE8-FCC8-4D7A-8C29-6CA98F235E9C}](https://github.com/user-attachments/assets/d3cd8289-6285-4c90-91e6-aa93e2053887)


# **This image shows the encoder section, let's say we had 1 lstm cell in encoder when we UNFOLD IT THROUGH TIME, we got something like that for the sentence we use 'NICE TO MEET YOU'**

# **FOR EACH TIME STEP WE GOT THIS STRUCTURE, the hidden state and cell state of each cell becomes the input to the next cell**

# **and at the end what we got is the `CONTEXT VECTOR`**
![{205581FC-58CF-48B6-AE25-1DE61182F8C5}](https://github.com/user-attachments/assets/ba1c69b7-1a49-4e39-8afb-7284cf42c8fe)



# **DECODER SECTION**

# **We provide that context vector to the decoder, and provide it a special symbol < START > , as the decoder encounters it, it starts to produce the sequences**

# **THE FIRST SEQUENCE IT HAS PRODUCED WILL BE GIVEN AS AN INPUT TO THE NEXT CELL, AND THE OUTPUT SEQUENCE THAT CELL WILL PRODUCE WILL BE GIVEN AS AN INPUT TO THE NEXT CELL AND SO ON...**

# **at the end, when it encoutners < END >, it stops producing the sequences**
![{9C9F73D4-B249-4E12-9580-D3B7B16E3CE5}](https://github.com/user-attachments/assets/1b856820-0164-4718-8d35-beef43677278)
