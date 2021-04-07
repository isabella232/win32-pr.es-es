---
title: Operación básica de OpenGL
description: Operación básica de OpenGL
ms.assetid: ad4c9321-a9e3-40c5-af80-0ad6a8b9f380
keywords:
- OpenGL, operaciones básicas
- OpenGL, procesamiento de datos
- OpenGL, fases de procesamiento
- OpenGL, mostrar listas
- Mostrar listas OpenGL
- OpenGL, evaluadores
- los evaluadores OpenGL
- OpenGL, operaciones por vértice
- operaciones por vértices OpenGL
- OpenGL, ensamblado primitivo
- ensamblado primitivo OpenGL
- OpenGL, rasterización
- rasterización OpenGL
- OpenGL, operaciones por fragmento
- operaciones por fragmento OpenGL
- framebuffers, operaciones básicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f6b9fb8c8ca4efb05d9050e0de3da807b213e7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104003286"
---
# <a name="basic-opengl-operation"></a><span data-ttu-id="6728b-119">Operación básica de OpenGL</span><span class="sxs-lookup"><span data-stu-id="6728b-119">Basic OpenGL Operation</span></span>

<span data-ttu-id="6728b-120">En el diagrama siguiente se ilustra el modo en que OpenGL procesa los datos.</span><span class="sxs-lookup"><span data-stu-id="6728b-120">The following diagram illustrates how OpenGL processes data.</span></span> <span data-ttu-id="6728b-121">Como se muestra, los comandos se escriben desde la izquierda y continúan a través de una canalización de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="6728b-121">As shown, commands enter from the left and proceed through a processing pipeline.</span></span> <span data-ttu-id="6728b-122">Algunos comandos especifican los objetos geométricos que se van a dibujar y otros controlan cómo se administran los objetos durante varias fases de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="6728b-122">Some commands specify geometric objects to be drawn, and others control how the objects are handled during various processing stages.</span></span>

![Diagrama que muestra las fases de canalización de procesamiento de datos de OpenGL.](images/basic01.png)

<span data-ttu-id="6728b-124">Las fases de procesamiento de la operación básica de OpenGL son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="6728b-124">The processing stages in basic OpenGL operation are as follows:</span></span>

-   <span data-ttu-id="6728b-125">**Mostrar lista** En lugar de que todos los comandos continúen inmediatamente a través de la canalización, puede optar por acumular algunos en una lista de visualización para procesarlos más adelante.</span><span class="sxs-lookup"><span data-stu-id="6728b-125">**Display list** Rather than having all commands proceed immediately through the pipeline, you can choose to accumulate some of them in a display list for processing later.</span></span>
-   <span data-ttu-id="6728b-126">**Evaluador** La fase Evaluadora del procesamiento proporciona una manera eficaz de aproximar la geometría de curva y de superficie mediante la evaluación de los comandos polinómicos de valores de entrada.</span><span class="sxs-lookup"><span data-stu-id="6728b-126">**Evaluator** The evaluator stage of processing provides an efficient way to approximate curve and surface geometry by evaluating polynomial commands of input values.</span></span>
-   <span data-ttu-id="6728b-127">**Operaciones por vértice y ensamblado primitivo** OpenGL procesa primitivespoints, segmentos de línea y polygonsall geométricos que se describen en los vértices.</span><span class="sxs-lookup"><span data-stu-id="6728b-127">**Per-vertex operations and primitive assembly** OpenGL processes geometric primitivespoints, line segments, and polygonsall of which are described by vertices.</span></span> <span data-ttu-id="6728b-128">Los vértices se transforman y se iluminan, y los primitivos se recortan a la ventanilla como preparación para la rasterización.</span><span class="sxs-lookup"><span data-stu-id="6728b-128">Vertices are transformed and lit, and primitives are clipped to the viewport in preparation for rasterization.</span></span>
-   <span data-ttu-id="6728b-129">**Rasterización** La fase de rasterización genera una serie de direcciones de búfer de fotogramas y valores asociados mediante una descripción bidimensional de un punto, segmento de línea o polígono.</span><span class="sxs-lookup"><span data-stu-id="6728b-129">**Rasterization** The rasterization stage produces a series of frame-buffer addresses and associated values using a two-dimensional description of a point, line segment, or polygon.</span></span> <span data-ttu-id="6728b-130">Cada fragmento generado se introduce en la última fase, en las operaciones por fragmento.</span><span class="sxs-lookup"><span data-stu-id="6728b-130">Each fragment so produced is fed into the last stage, per-fragment operations.</span></span>
-   <span data-ttu-id="6728b-131">**Operaciones por fragmento** Estas son las operaciones finales realizadas en los datos antes de que se almacenen como píxeles en el fotogramas.</span><span class="sxs-lookup"><span data-stu-id="6728b-131">**Per-fragment operations** These are the final operations performed on the data before it is stored as pixels in the framebuffer.</span></span>

    <span data-ttu-id="6728b-132">Las operaciones por fragmento incluyen actualizaciones condicionales para fotogramas basadas en valores z entrantes y almacenados previamente (para el almacenamiento en búfer z) y la combinación de colores de píxeles entrantes con colores almacenados, así como enmascaramiento y otras operaciones lógicas en valores de píxeles.</span><span class="sxs-lookup"><span data-stu-id="6728b-132">Per-fragment operations include conditional updates to the framebuffer based on incoming and previously stored z values (for z buffering) and blending of incoming pixel colors with stored colors, as well as masking and other logical operations on pixel values.</span></span>

<span data-ttu-id="6728b-133">Los datos se pueden escribir en forma de píxeles en lugar de vértices.</span><span class="sxs-lookup"><span data-stu-id="6728b-133">Data can be input in the form of pixels rather than vertices.</span></span> <span data-ttu-id="6728b-134">Los datos en forma de píxeles, como puede describir una imagen para su uso en la asignación de texturas, omiten la primera fase del procesamiento descrito anteriormente y, en su lugar, se procesan como píxeles, en la fase de operaciones de píxeles.</span><span class="sxs-lookup"><span data-stu-id="6728b-134">Data in the form of pixels, such as might describe an image for use in texture mapping, skips the first stage of processing described above and instead is processed as pixels, in the pixel operations stage.</span></span> <span data-ttu-id="6728b-135">En las siguientes operaciones de píxeles, los datos de píxeles son:</span><span class="sxs-lookup"><span data-stu-id="6728b-135">Following pixel operations, the pixel data is either:</span></span>

-   <span data-ttu-id="6728b-136">Se almacena como memoria de textura, para su uso en la fase de rasterización.</span><span class="sxs-lookup"><span data-stu-id="6728b-136">Stored as texture memory, for use in the rasterization stage.</span></span>
-   <span data-ttu-id="6728b-137">Rasterizado, con los fragmentos resultantes combinados en el fotogramas como si se hubieran generado a partir de datos geométricos.</span><span class="sxs-lookup"><span data-stu-id="6728b-137">Rasterized, with the resulting fragments merged into the framebuffer just as if they were generated from geometric data.</span></span>

 

 




