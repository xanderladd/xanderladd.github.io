---
layout: base
title:  "Review 23: Neuropixels 2.0: A miniaturized high-density probe for stable, long-term
brain recordings"
date:   2022-4-16 5:16:13 -0700
author: xander
categories: reviews
---


[Neuropixels 2.0: A miniaturized high-density probe for stable, long-term
brain recordings](https://www.biorxiv.org/content/10.1101/2020.10.27.358291v1.full.pdf) by [Nick Steinmetz](http://www.nicksteinmetz.com/#:~:text=Nick%20Steinmetz,and%20cognition%20across%20the%20brain.).


- Paper notes for Neuropixels 2.0
    - Notably, this is a pretty big collaboration. The following labs participated:
        - O'Keefe Lab at UCL
        - Moser Lab at NTNU
        - Lee Lab at Janelia Research
        - Dudman lab at Janelia Research
        - Hausser Lab at UCL
        - Steinmetz Lab at UW
        - Svoboda Lab at Janelia
        - Carandini/ Harris Lab
        - Hantman Lab
        - Haesler Lab

    - Neuropixels new probe :
        - has over 5000 sites, features 
        - has 2 probes and a head stage
        - records at 786 sites at once
        - weighs over 1 gram
        - enables recording from over > 10000 recording sites during free behavior in mice
    - Stably recording neurons over days / weeks during long terms processes like learning and memory is challenging, but important for understanding neural coding.
    - Many attempts to record from devices that are flexible and less than $\mu$m in size.
        - Paper states that downside to these approaches are: make insertion difficult and do not scale at large numbers of recording sites per shank.
        - I don't understand how small flexible devices could make insertion more difficult.
    - More rigid and larger devices (Utah array, wire tetrodes, silicon probes) record high-quality signals for 8 weeks. However, no consistent recordings of individual neurons over the scale of months.
    - Neuropixels: dense coverage along a line, another array: across a plane.
    - algorithm stabilizes device to brain motion post hoc.
    - two recording channels be simultaneously recorded in the same channel with noise penalty in snr.
        - At this point, I realized that there is a lot of past literature about these recording probes that I am missing. This feels like watching avengers before watching all the prequel movies.
    - Results
        - 4 shanks, 1280 sites per shank, 5120 total sites.
        - single wide band 14-bit data stream.
        - Hardware switches can swap recording streams enabling recording from thousands of streams/experiment.
        - can cover a plan of 750 x 720 $\mu$m during recording.
        - Fig. 1
            - Neuropixels 2.0 is much less wide than the previous version.
            - Shows LFP recording and spike waveform recording (overlapping channels).
            - Probe rasters and reproduced raster of dorsal striatum firing pattern across ten trials.
        - 7 / 8  probes recovered in working condition.
        - max time recording from implant: 309 days.
        - Fig 2.
            - the proportion of spikes has a decaying distribution over the # of days after implant. A similar trend is shown in C. and D.
            -  hippocampus has a high proportion of firing neurons.
            - comparison of spike recording stats between labs that used the device.
                - I think this plot is hard to interpret because I know there are different conditions for each lab so plot does not necessarily show apples to apples.
        - Paper claims brain motion leads to progressively less spikes during the duration of a recording.
        - But they have an unsupervised learning algorithm to adjust for motion post hoc and re-detect spikes. This method increases recording stability (3E).
        - Fig 3.
            - The results from this stabilization procedure a visually very convincing.
        - Now they expand the timescale alignment to long intervals.
            - successful tracking across days, and weeks (figure 4). 83% tracking accuracy after 9 weeks. 
            - wonder what that accuracy is across more than three months? But tracking 83% of neurons seems really good.
        - Average signals from two sites along a recording line and then decompose them.
        - Fig 4
            - bank 1 and bank 2 separated to two sets of neurons and the switch helps record mapping between banks using mismatch.
            - when both banks are recording noise is lower.
            - 3 configurations: both banks on, bank 1 on, bank 2 on.
