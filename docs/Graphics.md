---
layout: default
title: VR & Computer Graphics
parent: Basic Questions
nav_order: 1
---

# VR & Computer Graphics
{: .no_toc }

Useful Link:

- [Learn OpenGL](https://learnopengl.com/)


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

**Objects in a 3D scene are typically described using triangles**, which in turn are defined by their vertices.

A vertex shader is a graphics processing function which calculate the x, y, z position value of each vertex.

---

## Fragment Shader

Fragment Shader is a function which calculate the color of each pixel.

---

## Depth Map

Depth maps contain information about **the distance of objects from a specific perspective or reference point (like a camera lens)**. It's a 2D image, each pixel is assigned a value to represent the distance of that pixel from the reference point.

There are camera depth map and light depth map which save the distance from each vertex to the camera or light source.

---

## Light Map & Normal Map

Light Map include the surface with ambient, diffuse and specular lighting (Phong lighting model).

Light Map with 2D texture is flat, most real-life surface aren't flat however and exhibit a lot of (bumpy) details.

We can slightly deviate the normal vector based on a surface's little details; this gives the illusion the surface is a lot more complex. By using per-fragment normals we can trick the lighting into believing a surface consists of tiny little planes (perpendicular to the normal vectors) giving the surface an enormous boost in detail. This technique to use per-fragment normals compared to per-surface normals is called normal mapping or bump mapping. Applied to the brick plane it looks a bit like this:

![](../../assets/images/normal_mapping_compare.png)

Extra 2D normal map image needed:

![](../../assets/images/normal_mapping_normal_map.png)


## mipmap

Since mipmaps, by definition, are pre-allocated, additional storage space is required to take advantage of them. They are also related to wavelet compression. Mipmap textures are used in 3D scenes to decrease the time required to render a scene. They also improve image quality by reducing **aliasing and Moiré patterns** that occur at large viewing distances, at the cost of 33% more memory per texture.

## Shadow mapping

[Shadow mapping](https://github.com/Weiwei-Wan/OpenGL-shadow-mapping)
