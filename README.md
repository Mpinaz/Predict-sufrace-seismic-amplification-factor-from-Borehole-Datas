# Prediction of Surface Seismic Amplification Factor from Borehole Data

Work done by **Matteo Pinato** (pinato.2061665@studenti.uniroma1.it) and **Sofia De Angelis** (deangelis.2126369@studenti.uniroma1.it) for the exam *Earthquake Physics for Machine Learning*.

## Overview

One of the key factors influencing seismic risk is the accurate assessment of local seismic response. Traditional empirical methods, often based on multiple linear regression models, show significant limitations in capturing the complex nonlinear interactions between soil properties and seismic wave propagation.

This project proposes a Deep Neural Network approach for predicting the seismic amplification factor, formulating the problem as a **regression task** that quantifies site response in continuous rather than categorical terms.

## Table of Contents

- [Dataset](#dataset)
- [Features](#features)
- [Models](#models)
- [Results](#results)
- [Installation & Usage](#installation--usage)
- [References](#references)

## Dataset

The dataset is built from **KiK-net** records, retrieved and reorganized into tabular form. Sources:

- Zhu, Chuanbin; Weatherill, Graeme; Cotton, Fabrice; Pilz, Marco; Kwak, Dong Youp; Kawase, Hiroshi (2020): *An Open-Source Site Database of Strong-Motion Stations in Japan: K-NET and KiK-net*. V. 1.0.0. GFZ Data Services. https://doi.org/10.5880/GFZ.2.1.2020.006
- Loviknes, Karina; von Specht, Sebastian; Lilienkamp, Henning; Händel, Annabel; Cotton, Fabrice (2025): *KiK-net and K-NET flatfile with automatically processed ground motions*. GFZ Data Services. https://doi.org/10.5880/GFZ.LKUT.2025.001

## Features

We used a set of **18 features** taken from both datasets. Details are provided in the [paper](Paper.pdf), Section 2.2.

## Models

Since the task involves tabular data, tree-based models such as **Random Forest** and **XGBoost** are expected to perform strongly. We compare them against a **Multi-Layer Perceptron (MLP)**, which serves as a baseline to confirm the proper fit of our approach.

The MLP has 6 layers with sizes `18 → 128 → 256 → 128 → 64 → 1`. The expanding-then-contracting hidden structure (128 → 256 → 128) forms a symmetric bottleneck, designed to capture the physical relationships hidden within the input data.

## Results

_WIP_

## Installation & Usage

_WIP_

## References

See the [paper](Paper.pdf) for the full methodology and bibliography.
