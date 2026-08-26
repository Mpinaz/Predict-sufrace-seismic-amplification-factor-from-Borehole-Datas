# Prediction of sufrace seismic amplification factor from borehole datas

Work done by Matteo Pinato (pinato.2061665@studenti.uniroma1.it) and Sofia De Angelis (deangelis.2126369@studenti.uniroma1.it) for the exam: Earthquakes Physics for Machine Learing.

One of the key factors influencing seismic risk is the accurate assessment of local seismic response. Traditional empirical methods, often based on multiple linear regression models, exhibit significant limitations in capturing the complex nonlinear interactions between soil properties and seismic wave propagation.

This study proposes a Deep Neural Network based approach for predicting the seismic amplification factor, formulating the problem as a regression task aimed at quantifying site response in continuous rather than categorical terms. 

## Dataset

The dataset is composed of Kik-Net Datas retrieved and reogrinized in tabular datas:

- Zhu, Chuanbin; Weatherill, Graeme; Cotton, Fabrice; Pilz, Marco; Kwak, Dong Youp; Kawase, Hiroshi (2020): An Open-Source Site Database of Strong-Motion Stations in Japan: K-NET and KiK-net. V. 1.0.0. GFZ Data Services. https://doi.org/10.5880/GFZ.2.1.2020.006

- Loviknes, Karina; von Specht, Sebastian; Lilienkamp, Henning; Händel, Annabel; Cotton, Fabrice (2025): KiK-NET and K-NET flatfile with automatically processed ground motions. GFZ Data Services. https://doi.org/10.5880/GFZ.LKUT.2025.001

## Features

We used a set of 18 features taken from both datasets, more information on features are located in the [Paper](Paper.pdf) on chapter 2.2.

## Models

Since we are dealing with tabular datas models like Random Forest and XGBoost are expected to perform extremely well for our task, so we decided to confront them with an MLP in oredr to have a baseline to confirm the proper fit of out model.

The MLP is composed of 6 layers (18, 128, 256, 128, 64, 1) with an expanding and contracting hidden-layer structure (128 → 256 → 128), forming a symmetric bottleneck, this design is specifically created in order to seize the physical features hidden between the input datas.

## Results

