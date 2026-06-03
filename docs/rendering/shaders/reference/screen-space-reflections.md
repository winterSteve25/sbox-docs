---
title: "Screen-Space Reflections"
icon: "🪞"
created: 2025-07-28
updated: 2025-07-28
---

# Screen-Space Reflections

SSR is done in three steps

* Intersection
  * Uses the [G-Buffer](/rendering/shaders/classes/g-buffer.md) and [Screen Space Tracing](/rendering/shaders/classes/screen-space-tracing.md) right after we do the Depth Pre-Pass, uses the result from last frame reprojected with [Motion](/rendering/shaders/classes/motion.md)
  * ![](./images/screen-space-reflections-1.png)
* Denoising
  * Accumulates the result and makes it pretty taking off the rough edges
  * ![](./images/screen-space-reflections.png)
* Compositing
  * Sets the texture to be composited with [Dynamic Reflections](/rendering/shaders/classes/dynamic-reflections.md)
  * ![](./images/screen-space-reflections-2.png)
