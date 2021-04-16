---
title: Biblioteca de Sphere GL de IRIS
description: OpenGL no es compatible con la biblioteca de esfera GL de IRIS. Puede reemplazar las llamadas de la biblioteca de esferas por las rutinas de Quadrics de la biblioteca de GLU. Para obtener más información acerca de la biblioteca GLU, vea la guía de programación de Open GL y la biblioteca de utilidades OpenGL.
ms.assetid: 2b7e6a3d-d2d0-4b54-8dff-8c4d6b113007
keywords:
- Migración de la contabilidad de IRIS, biblioteca de esferas
- portabilidad de IRIS GL, biblioteca de esferas
- trasladar a OpenGL desde IRIS GL, biblioteca de esferas
- Exportación de OpenGL desde IRIS GL, biblioteca de esferas
- funciones de dibujo, biblioteca Sphere
- Biblioteca de esferas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586974c5874aee73121e536cbadca4564a18c250
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357263"
---
# <a name="the-iris-gl-sphere-library"></a><span data-ttu-id="b6773-111">Biblioteca de Sphere GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="b6773-111">The IRIS GL Sphere Library</span></span>

<span data-ttu-id="b6773-112">OpenGL no es compatible con la biblioteca de esfera GL de IRIS.</span><span class="sxs-lookup"><span data-stu-id="b6773-112">OpenGL does not support the IRIS GL sphere library.</span></span> <span data-ttu-id="b6773-113">Puede reemplazar las llamadas de la biblioteca de esferas por las rutinas de Quadrics de la biblioteca de GLU.</span><span class="sxs-lookup"><span data-stu-id="b6773-113">You can replace your sphere library calls with quadrics routines from the GLU library.</span></span> <span data-ttu-id="b6773-114">Para obtener más información acerca de la biblioteca GLU, vea la *Guía de programación de Open GL* y la [biblioteca de utilidades OpenGL](opengl-utility-library.md).</span><span class="sxs-lookup"><span data-stu-id="b6773-114">For more information about the GLU library, see the *Open GL Programming Guide* and [OpenGL Utility Library](opengl-utility-library.md).</span></span>

<span data-ttu-id="b6773-115">En la tabla siguiente se enumeran las funciones de Quadrics de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="b6773-115">The following table lists the OpenGL quadrics functions.</span></span>



| <span data-ttu-id="b6773-116">Función OpenGL</span><span class="sxs-lookup"><span data-stu-id="b6773-116">OpenGL function</span></span>                                        | <span data-ttu-id="b6773-117">Significado</span><span class="sxs-lookup"><span data-stu-id="b6773-117">Meaning</span></span>                                                          |
|--------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="b6773-118">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="b6773-118">**gluNewQuadric**</span></span>](glunewquadric.md)                 | <span data-ttu-id="b6773-119">Crea un nuevo objeto quadric.</span><span class="sxs-lookup"><span data-stu-id="b6773-119">Creates a new quadric object.</span></span>                                    |
| [<span data-ttu-id="b6773-120">**gluDeleteQuadric**</span><span class="sxs-lookup"><span data-stu-id="b6773-120">**gluDeleteQuadric**</span></span>](gludeletequadric.md)           | <span data-ttu-id="b6773-121">Elimina un objeto quadric.</span><span class="sxs-lookup"><span data-stu-id="b6773-121">Deletes a quadric object.</span></span>                                        |
| [<span data-ttu-id="b6773-122">*gluQuadricCallback*</span><span class="sxs-lookup"><span data-stu-id="b6773-122">*gluQuadricCallback*</span></span>](gluquadric.md)                 | <span data-ttu-id="b6773-123">Asocia una devolución de llamada a un objeto quadric para el control de errores.</span><span class="sxs-lookup"><span data-stu-id="b6773-123">Associates a callback with a quadric object, for error handling.</span></span> |
| [<span data-ttu-id="b6773-124">**gluQuadricNormals**</span><span class="sxs-lookup"><span data-stu-id="b6773-124">**gluQuadricNormals**</span></span>](gluquadricnormals.md)         | <span data-ttu-id="b6773-125">Especifica las normales: no hay normal, una por cara o una por vértice.</span><span class="sxs-lookup"><span data-stu-id="b6773-125">Specifies normals: no normals, one per face, or one per vertex.</span></span>  |
| [<span data-ttu-id="b6773-126">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="b6773-126">**gluQuadricOrientation**</span></span>](gluquadricorientation.md) | <span data-ttu-id="b6773-127">Especifica la dirección de las normales: hacia fuera o hacia adentro.</span><span class="sxs-lookup"><span data-stu-id="b6773-127">Specifies direction of normals: outward or inward.</span></span>               |
| [<span data-ttu-id="b6773-128">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="b6773-128">**gluQuadricTexture**</span></span>](gluquadrictexture.md)         | <span data-ttu-id="b6773-129">Activa o desactiva la generación de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="b6773-129">Turns texture-coordinate generation on or off.</span></span>                   |
| [<span data-ttu-id="b6773-130">**gluQuadricDrawstyle**</span><span class="sxs-lookup"><span data-stu-id="b6773-130">**gluQuadricDrawstyle**</span></span>](gluquadricdrawstyle.md)     | <span data-ttu-id="b6773-131">Especifica el estilo de dibujo: polígonos, líneas, puntos, etc.</span><span class="sxs-lookup"><span data-stu-id="b6773-131">Specifies drawing style: polygons, lines, points, and so on.</span></span>     |
| [<span data-ttu-id="b6773-132">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="b6773-132">**gluSphere**</span></span>](glusphere.md)                         | <span data-ttu-id="b6773-133">Dibuja una esfera.</span><span class="sxs-lookup"><span data-stu-id="b6773-133">Draws a sphere.</span></span>                                                  |
| [<span data-ttu-id="b6773-134">**gluCylinder**</span><span class="sxs-lookup"><span data-stu-id="b6773-134">**gluCylinder**</span></span>](glucylinder.md)                     | <span data-ttu-id="b6773-135">Dibuja un cilindro o un cono.</span><span class="sxs-lookup"><span data-stu-id="b6773-135">Draws a cylinder or cone.</span></span>                                        |
| [<span data-ttu-id="b6773-136">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="b6773-136">**gluPartialDisk**</span></span>](glupartialdisk.md)               | <span data-ttu-id="b6773-137">Dibuja un arco.</span><span class="sxs-lookup"><span data-stu-id="b6773-137">Draws an arc.</span></span>                                                    |
| [<span data-ttu-id="b6773-138">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="b6773-138">**gluDisk**</span></span>](gludisk.md)                             | <span data-ttu-id="b6773-139">Dibuja un círculo o un disco.</span><span class="sxs-lookup"><span data-stu-id="b6773-139">Draws a circle or disk.</span></span>                                          |



 

<span data-ttu-id="b6773-140">Puede usar un objeto quadric para todos los Quadrics que quiera representar de maneras similares.</span><span class="sxs-lookup"><span data-stu-id="b6773-140">You can use one quadric object for all quadrics you want to render in similar ways.</span></span> <span data-ttu-id="b6773-141">En el ejemplo de código siguiente se usan dos objetos quadric para dibujar cuatro Quadrics, dos de ellos con textura.</span><span class="sxs-lookup"><span data-stu-id="b6773-141">The following code sample uses two quadric objects to draw four quadrics, two of them textured.</span></span>


```C++
GLUquadricObj    *texturedQuad, *plainQuad; 
 
texturedQuad = gluNewQuadric(void); 
gluQuadricTexture(texturedQuad, GL_TRUE); 
gluQuadricOrientation(texturedQuad, GLU_OUTSIDE); 
gluQuadricDrawStyle(texturedQuad, GLU_FILL); 
 
plainQuad = gluNewQuadric(void); 
gluQuadricDrawStyle(plainQuad, GLU_LINE); 
 
glColor3f (1.0, 1.0, 1.0); 
 
gluSphere(texturedQuad, 5.0, 20, 20); 
glTranslatef(10.0, 10.0, 0.0); 
gluCylinder(texturedQuad, 2.5, 5, 5, 10, 10); 
glTranslatef(10.0, 10.0, 0.0); 
gluDisk(plainQuad, 2.0, 5.0, 10, 10); 
glTranslatef(10.0, 10.0, 0.0); 
gluSphere(plainQuad, 5.0, 20, 20);
```



 

 




