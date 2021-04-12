---
title: Representación de superficies simples
description: La biblioteca GLU incluye un conjunto de funciones para dibujar varias superficies simples (esferas, cilindros, discos y partes de discos) en una variedad de estilos y orientaciones. Estas funciones se describen en detalle en el manual de referencia de OpenGL.
ms.assetid: 403bdf8d-de4c-49e2-87d0-11109061b4c2
keywords:
- Utilidad OpenGL (GLU), superficies simples
- GLU (utilidad OpenGL), superficies simples
- superficies simples OpenGL
- Utilidad OpenGL (GLU), esferas
- GLU (utilidad OpenGL), esferas
- esferas OpenGL
- Utilidad OpenGL (GLU), cilindros
- GLU (utilidad OpenGL), cilindros
- cilindros de OpenGL
- Utilidad OpenGL (GLU), discos
- GLU (utilidad OpenGL), discos
- discos OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab766c661f89cbdec30b3295dfef8dc85b59f7fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419177"
---
# <a name="rendering-simple-surfaces"></a><span data-ttu-id="0acb6-116">Representación de superficies simples</span><span class="sxs-lookup"><span data-stu-id="0acb6-116">Rendering Simple Surfaces</span></span>

<span data-ttu-id="0acb6-117">La biblioteca GLU incluye un conjunto de funciones para dibujar varias superficies simples (esferas, cilindros, discos y partes de discos) en una variedad de estilos y orientaciones.</span><span class="sxs-lookup"><span data-stu-id="0acb6-117">The GLU library includes a set of functions for drawing various simple surfaces (spheres, cylinders, disks, and parts of disks) in a variety of styles and orientations.</span></span> <span data-ttu-id="0acb6-118">Estas funciones se describen en detalle en el *manual de referencia de OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="0acb6-118">These functions are described in detail in the *OpenGL Reference Manual*.</span></span>

<span data-ttu-id="0acb6-119">**Para representar superficies simples**</span><span class="sxs-lookup"><span data-stu-id="0acb6-119">**To render simple surfaces**</span></span>

1.  <span data-ttu-id="0acb6-120">Cree un objeto quadric con [**gluNewQuadric**](glunewquadric.md).</span><span class="sxs-lookup"><span data-stu-id="0acb6-120">Create a quadric object with [**gluNewQuadric**](glunewquadric.md).</span></span>

    <span data-ttu-id="0acb6-121">Para destruir este objeto cuando haya terminado, use [**gluDeleteQuadric**](gludeletequadric.md).</span><span class="sxs-lookup"><span data-stu-id="0acb6-121">To destroy this object when you're finished with it, use [**gluDeleteQuadric**](gludeletequadric.md).</span></span>

2.  <span data-ttu-id="0acb6-122">Especifique el estilo de representación que desee, como se muestra a continuación, con la función adecuada (a menos que esté satisfecho con los valores predeterminados):</span><span class="sxs-lookup"><span data-stu-id="0acb6-122">Specify the desired rendering style, as listed below, with the appropriate function (unless you're satisfied with the default values):</span></span>
    -   <span data-ttu-id="0acb6-123">Si se deben generar normales de superficie y, en caso afirmativo, si debe haber una normal por vértice o una normal por cara: [ **gluQuadricNormals**](gluquadricnormals.md)</span><span class="sxs-lookup"><span data-stu-id="0acb6-123">Whether surface normals should be generated, and if so, whether there should be one normal per vertex or one normal per face: [**gluQuadricNormals**](gluquadricnormals.md)</span></span>
    -   <span data-ttu-id="0acb6-124">Indica si se deben generar coordenadas de textura: [ **gluQuadricTexture**](gluquadrictexture.md)</span><span class="sxs-lookup"><span data-stu-id="0acb6-124">Whether texture coordinates should be generated: [**gluQuadricTexture**](gluquadrictexture.md)</span></span>
    -   <span data-ttu-id="0acb6-125">Qué lado del quadric se debe considerar fuera y en el interior: [ **gluQuadricOrientation**](gluquadricorientation.md)</span><span class="sxs-lookup"><span data-stu-id="0acb6-125">Which side of the quadric should be considered the outside and which the inside: [**gluQuadricOrientation**](gluquadricorientation.md)</span></span>
    -   <span data-ttu-id="0acb6-126">Si quadric se debe dibujar como un conjunto de polígonos, líneas o puntos: [ **gluQuadricDrawStyle**](gluquadricdrawstyle.md)</span><span class="sxs-lookup"><span data-stu-id="0acb6-126">Whether the quadric should be drawn as a set of polygons, lines, or points: [**gluQuadricDrawStyle**](gluquadricdrawstyle.md)</span></span>
3.  <span data-ttu-id="0acb6-127">Después de especificar el estilo de representación, invoque la función de representación para el tipo deseado del objeto quadric: [**gluSphere**](glusphere.md), [**gluCylinder**](glucylinder.md), [**gluDisk**](gludisk.md)o [**gluPartialDisk**](glupartialdisk.md).</span><span class="sxs-lookup"><span data-stu-id="0acb6-127">After specifying the rendering style, invoke the rendering function for the desired type of quadric object: [**gluSphere**](glusphere.md), [**gluCylinder**](glucylinder.md), [**gluDisk**](gludisk.md), or [**gluPartialDisk**](glupartialdisk.md).</span></span>

    <span data-ttu-id="0acb6-128">Si se produce un error durante la representación, se invoca la función de control de errores que ha especificado con [*gluQuadricCallBack*](gluquadric.md) .</span><span class="sxs-lookup"><span data-stu-id="0acb6-128">If an error occurs during rendering, the error-handling function you've specified with [*gluQuadricCallBack*](gluquadric.md) is invoked.</span></span>

<span data-ttu-id="0acb6-129">Use el *\* radio*, el *alto* y argumentos similares, en lugar de la función [**glScale**](glscale.md) , para escalar el Quadrics, de modo que no tenga que volver a normalizar las normales de longitud de unidad que se generan.</span><span class="sxs-lookup"><span data-stu-id="0acb6-129">Use the *\*Radius*, *height*, and similar arguments, rather than the [**glScale**](glscale.md) function, to scale the quadrics, so that you don't have to renormalize any unit-length normals that are generated.</span></span> <span data-ttu-id="0acb6-130">Para forzar cálculos de iluminación con una granularidad más fina, especialmente si la especulación del material es alta, establezca los argumentos *bucles* y *pilas* en valores distintos de 1.</span><span class="sxs-lookup"><span data-stu-id="0acb6-130">To force lighting calculations at a finer granularity, especially if the material specularity is high, set the *loops* and *stacks* arguments to values other than 1.</span></span>

 

 




