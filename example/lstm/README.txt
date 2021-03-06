## GOAL ##
LSTM example using Platoon.


## CONTENT ##
- README.txt
- lstm_controller.py
- lstm_worker.py
- imdb.py


## HOW TO USE ##
# USING THE LAUNCHER
1) Assuming you are in the lstm folder.
   `cd platoon/example/lstm/`

1) Launch the experiment on 2 GPUs using the platoon-launcher script.
   `platoon-launcher lstm -D cuda0 cuda2`

To see all controller parameters do: `python lstm_controller.py -h`
To pass them via the platoon-launcher script: `platoon-launcher lstm -D cuda0 cuda2 -c=...`

To see all worker parameters do: `python lstm_worker.py -h`
To pass them via the platoon-launcher script: `platoon-launcher lstm -D cuda0 cuda2 -w=...`

# MANUALLY
1) Assuming you are in the lstm folder.
   `cd platoon/example/lstm/`

2) Start the controller.
   `THEANO_FLAGS='device=cpu' python -u lstm_controller.py`

3) Start the worker. Repeat as needed changing the GPU id.
   `THEANO_FLAGS='device=gpu0' python -u lstm_worker.py`


## NOTE ##
If you use the MANUAL way, you may want to run them in different windows of screen or tmux.
They all expect to be in the foreground.
