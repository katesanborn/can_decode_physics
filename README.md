# Physics-Based CAN Signal Decoding using Bayesian Optimization

This repository contains the code used for the multi-stage CAN signal decoding pipeline.

Specifically, this example demonstrates decoding the side radar data on a Nissan vehicle. All data used must be added to the data folder. It is not stored on GitHub.

The data in ```left_distance_381.csv``` contains a set of measurements and recorded CAN messages. The measurements represent how far a person was standing from the back car radar. While the person was standing there, the distance was measured, and the message was recorded. The values are matched temporally. It is assumed to be known that the radar messages are present in message ID 381.

The ```2025-08-27-16-11-56_JN8AT3CB9MW240939_CAN_Messages.csv``` file contains all the CAN messages recorded from the entire experiment. This includes driving to the parking lot, taking measurements, and then driving back. These messages are used to calculate the number of bit flips.

The ```can_decoding_pipeline.ipynb``` file demonstrates the full pipeline process. The ideal start, length, scale, and offset values are displayed. The notebook also plots the Bayesian Optimization convergence and the final linear regression results.