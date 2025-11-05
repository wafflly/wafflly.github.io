---
layout: page
title: Course Scheduling
description: ILP Optimization System
img: assets/img/Course.png
importance: 1
category: work
related_publications: false
---


Collaborated in the design and implementation of an automatic course scheduling system for the Linguistics Department at the University of Washington, formulated as an integer linear programming (ILP) problem using the [PuLP optimization package](https://coin-or.github.io/pulp/). 

The system automates the complex stage of the department’s annual scheduling process—assigning optimal time slots for courses—by translating real-world constraints such as UW’s block scheduling policy, the 10% rule, course conflicts, and instructor preferences into formal mathematical constraints.

We developed a fully end-to-end pipeline that reads departmental input files, constructs and solves the ILP problem, and generates optimized schedules, instructor assignment summaries, and compliance heatmaps. The solution balances institutional requirements and instructor preferences, significantly reducing the manual effort and potential inconsistencies in departmental scheduling.