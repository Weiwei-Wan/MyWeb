---
layout: default
title: VR & Computer Graphics
parent: Basic Questions
nav_order: 1
---

# VR & Computer Graphics
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## What's XR, AR, VR, and MR?

| Abbreviation | Full Name         | Description                                            |
|:-------------|:------------------|:-------------------------------------------------------|
| XR           | Extended Reality  | Add digital element to real world (AR, MR, VR include) |
| AR           | Augment Reality   | Digital layer over physical elements                   |
| MR           | Mixed Reality     | Digital elements interact with physical elements       |
| VR           | Virtual Realit    | Fully immersive (headset)                              |

In MR experiences the user can interact with both digital and physical elements. 
In AR digital and physical elements don’t interact.
In VR the physical or real world is completely blocked out.

![](../../assets/images/ar_vr_mr.jpg)
"Christian Briggs and the Interaction Design Foundation, CC BY-SA 4.0"

---

## Difference between quaternion and euler angle

You have to make three rotations and multiply them together when rotating by Euler angles, whereas a Quaternion is only one rotation and as it already encodes the sin and cos, the conversion from quaternion to matrix is quite efficient.

{: .note }
Eule angle would cause `dead lock`, if two axes overlap (y rotate 90° and overlap with x), we would lost one dimension.

---

## Vertex Shader

What is a vertex?
A vertex is the corner of the triangle where two edges meet, and thus every triangle is composed of three vertices.

Objects in a 3D scene are typically described using triangles, which in turn are defined by their vertices.

A vertex shader is a graphics processing function used to add special effects to objects in a 3D environment by performing mathematical operations on the objects' vertex data. Each vertex can be defined by many different variables. For instance, a vertex is always defined by its location in a 3D environment using the x-, y-, and z- coordinates. Vertices may also be defined by
colors, coordinates. Vertices may also be defined by colors, textures, and lighting characteristics. Vertex Shaders don't actually change the type of data; they simply change the values of the data, so that a vertex emerges with a different color, different textures, or a different position in space.

---
