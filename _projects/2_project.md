---
layout: page
title: Improving Chinese CLIP
description: Input manipulation to improve CLIP
img: assets/img/CN_CLIP/CN_CLIP_Background.png
importance: 1
category: Text
related_publications: false
---

## Introduction
Contrastive language-image pre-training (CLIP) is an efficient method that learns the association between the components in an image and their text from mapping captions to the images. The objective of our project is to enhance the accuracy of Chinese CLIP (CN-CLIP) in image classification tasks through three types of input manipulation methods.

<div class="row justify-content-center">
  <div class="col-md-10 col-sm-8 mt-3 mt-md-0 text-center">
    {% include figure.liquid 
        loading="eager" 
        path="assets/img/CN_CLIP/sys_overview.png" 
        title="system overview" 
        class="img-fluid rounded z-depth-1 mx-auto d-block" 
    %}
  </div>
</div>

<div class="caption text-center mt-2">
  An overview of the three methods.
</div>

---

## Methods

**1. GPT-generated prompt engineering**

Repace the original label with GPT-generated description of that label.
For instance, "飞机(an airplane)" is replaced with "飞机是一种大型的空中交通工具...（an airplane is a large aerial vehicle used for transportation...）"

**2. Multi-language input-embedding emsemble**

Average out the BERT embedding of Chinese description and English description for text encoder.

**3. Context optimized prompt learning**

Introduce learnable context vectors shared across all classes, added to Chinese class names, to fine-tune prompts and improve classification accuracy.

---

## Results

**GPT-generated prompt engineering** can significantly improve CN-CLIP’s accuracy on zero-shot image classification task; method 1 achieved the best performance - see below:

<div class="row justify-content-center">
  <div class="col-md-7 col-sm-8 mt-3 mt-md-0 text-center">
    {% include figure.liquid 
        loading="eager" 
        path="assets/img/CN_CLIP/results_method1.png" 
        title="results of method 1" 
        class="img-fluid rounded z-depth-1 mx-auto d-block" 
    %}
  </div>
</div>

<div class="caption text-center mt-2">
  Performance of GPT generated prompts (Method 1) on ImageNet
</div>