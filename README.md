# GA-Reader
Tensorflow implementation of [Gated Attention Reader for Text Comprehension](https://arxiv.org/abs/1606.01549). The original code can be found [here](https://github.com/bdhingra/ga-reader)

## Prerequisites
- Python 3.5
- TensorFlow 1.0

## Preprocessed Data
You can get the preprocessed data files from [here](https://drive.google.com/drive/folders/0B7aCzQIaRTDUZS1EWlRKMmt3OXM?usp=sharing). Extract the tar files to the `data/` directory. Ensure that the symbolic links point to folders with `training/`, `validation/` and `test/` directories for each dataset.

You can also get the pretrained Glove vectors from the above link. Place this file in the `data/` directory as well.

## To run
```
usage: main.py [-h] [--resume] [--use_feat] [--train_emb]
               [--data_dir DATA_DIR] [--log_dir LOG_DIR] [--save_dir SAVE_DIR]
               [--embed_file EMBED_FILE] [--gru_size GRU_SIZE]
               [--n_layers N_LAYERS] [--batch_size BATCH_SIZE]
               [--n_epoch N_EPOCH] [--save_every SAVE_EVERY]
               [--print_every PRINT_EVERY] [--grad_clip GRAD_CLIP]
               [--init_learning_rate INIT_LEARNING_RATE] [--seed SEED]
               [--char_dim CHAR_DIM] [--gating_fn GATING_FN]
               [--drop_out DROP_OUT]

Gated Attention Reader for Text Comprehension Using TensorFlow

optional arguments:
  -h, --help            show this help message and exit
  --resume              whether to keep training from previous model
  --use_feat            whether to use extra features
  --train_emb           whether to train embed
  --data_dir DATA_DIR   data directory containing input
  --log_dir LOG_DIR     directory containing tensorboard logs
  --save_dir SAVE_DIR   directory to store checkpointed models
  --embed_file EMBED_FILE
                        word embedding initialization file
  --gru_size GRU_SIZE   size of word GRU hidden state
  --n_layers N_LAYERS   number of layers of the model
  --batch_size BATCH_SIZE
                        mini-batch size
  --n_epoch N_EPOCH     number of epochs
  --save_every SAVE_EVERY
                        save frequency
  --print_every PRINT_EVERY
                        print frequency
  --grad_clip GRAD_CLIP
                        clip gradients at this value
  --init_learning_rate INIT_LEARNING_RATE
                        initial learning rate
  --seed SEED           random seed for tensorflow
  --char_dim CHAR_DIM   size of character GRU hidden state
  --gating_fn GATING_FN
                        gating function
  --drop_out DROP_OUT   dropout rate
```