---
title: Trasladar funciones de textura
description: Trasladar funciones de textura
ms.assetid: 03e0b0fc-3812-4744-a0f1-3dcb466d679d
keywords:
- Migración de la contabilidad de IRIS, textura
- portabilidad de IRIS GL, textura
- trasladar a OpenGL desde IRIS GL, textura
- Exportación de OpenGL desde IRIS GL, textura
- textura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2cba8b105089553084a93f997517d19cf371e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075948"
---
# <a name="porting-texture-functions"></a><span data-ttu-id="a7a93-108">Trasladar funciones de textura</span><span class="sxs-lookup"><span data-stu-id="a7a93-108">Porting Texture Functions</span></span>

<span data-ttu-id="a7a93-109">Al migrar funciones de textura de GL de IRIS a OpenGL, tenga en cuenta los puntos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a7a93-109">When porting IRIS GL texture functions to OpenGL, keep the following points in mind:</span></span>

-   <span data-ttu-id="a7a93-110">OpenGL no mantiene tablas de texturas; solo usa la textura 1D y la textura 2D.</span><span class="sxs-lookup"><span data-stu-id="a7a93-110">OpenGL doesn't maintain tables of textures; it uses either 1-D texture and 2-D texture only.</span></span> <span data-ttu-id="a7a93-111">Para reutilizar las texturas del código de GL de IRIS, colóquelas en una lista de visualización.</span><span class="sxs-lookup"><span data-stu-id="a7a93-111">To reuse the textures from your IRIS GL code, put them in a display list.</span></span>
-   <span data-ttu-id="a7a93-112">OpenGL no genera automáticamente mapas MIP.</span><span class="sxs-lookup"><span data-stu-id="a7a93-112">OpenGL doesn't automatically generate mipmaps.</span></span> <span data-ttu-id="a7a93-113">Si utiliza mapas MIP, primero debe llamar a la función [**gluBuild2DMipmaps**](glubuild2dmipmaps.md) .</span><span class="sxs-lookup"><span data-stu-id="a7a93-113">If you're using mipmaps, you must first call the [**gluBuild2DMipmaps**](glubuild2dmipmaps.md) function.</span></span>
-   <span data-ttu-id="a7a93-114">En OpenGL, se usa [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) para activar y desactivar las funcionalidades de la texturización.</span><span class="sxs-lookup"><span data-stu-id="a7a93-114">In OpenGL, you use [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) to turn texturing capabilities on and off.</span></span>
-   <span data-ttu-id="a7a93-115">En OpenGL, el tamaño de la textura se regula de forma más estricta que en el GL de IRIS.</span><span class="sxs-lookup"><span data-stu-id="a7a93-115">In OpenGL, texture size is more strictly regulated than in IRIS GL.</span></span> <span data-ttu-id="a7a93-116">El tamaño de una textura OpenGL debe ser:</span><span class="sxs-lookup"><span data-stu-id="a7a93-116">The size of an OpenGL texture must be:</span></span>

    <span data-ttu-id="a7a93-117">2 *n* + 2 *b*</span><span class="sxs-lookup"><span data-stu-id="a7a93-117">2 *n* + 2 *b*</span></span>

    <span data-ttu-id="a7a93-118">donde *n* es un entero y *b* es:</span><span class="sxs-lookup"><span data-stu-id="a7a93-118">where *n* is an integer and *b* is:</span></span>

    -   <span data-ttu-id="a7a93-119">0, si la textura no tiene borde</span><span class="sxs-lookup"><span data-stu-id="a7a93-119">0, if the texture has no border</span></span>
    -   <span data-ttu-id="a7a93-120">1, si la textura tiene un píxel de borde (las texturas OpenGL pueden tener bordes de 1 píxel).</span><span class="sxs-lookup"><span data-stu-id="a7a93-120">1, if the texture has a border pixel (OpenGL textures can have 1-pixel borders.)</span></span>

<span data-ttu-id="a7a93-121">En la tabla siguiente se enumeran las funciones de textura GL de IRIS y sus equivalentes de OpenGL generales.</span><span class="sxs-lookup"><span data-stu-id="a7a93-121">The following table lists IRIS GL texture functions and their general OpenGL equivalents.</span></span>



| <span data-ttu-id="a7a93-122">Función de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="a7a93-122">IRIS GL function</span></span> | <span data-ttu-id="a7a93-123">Función OpenGL</span><span class="sxs-lookup"><span data-stu-id="a7a93-123">OpenGL function</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="a7a93-124">Significado</span><span class="sxs-lookup"><span data-stu-id="a7a93-124">Meaning</span></span>                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7a93-125">**textdef2d**</span><span class="sxs-lookup"><span data-stu-id="a7a93-125">**textdef2d**</span></span>    | <span data-ttu-id="a7a93-126">[**glTexImage2D**](glteximage2d.md)[**glTexParameter**](gltexparameter-functions.md)</span><span class="sxs-lookup"><span data-stu-id="a7a93-126">[**glTexImage2D**](glteximage2d.md)[**glTexParameter**](gltexparameter-functions.md)</span></span><br/> [<span data-ttu-id="a7a93-127">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="a7a93-127">**gluBuild2DMipmaps**</span></span>](glubuild2dmipmaps.md)<br/>                                                                                                           | <span data-ttu-id="a7a93-128">Especifica una imagen de textura 2D.</span><span class="sxs-lookup"><span data-stu-id="a7a93-128">Specifies a 2-D texture image.</span></span>                                                              |
| <span data-ttu-id="a7a93-129">**textbind**</span><span class="sxs-lookup"><span data-stu-id="a7a93-129">**textbind**</span></span>     | <span data-ttu-id="a7a93-130">**glTexImage2DglTexParameter**</span><span class="sxs-lookup"><span data-stu-id="a7a93-130">**glTexImage2DglTexParameter**</span></span><br/> <span data-ttu-id="a7a93-131">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="a7a93-131">**gluBuild2DMipmaps**</span></span><br/>                                                                                                                                                                                            | <span data-ttu-id="a7a93-132">Selecciona una función de textura.</span><span class="sxs-lookup"><span data-stu-id="a7a93-132">Selects a texture function.</span></span>                                                                 |
| <span data-ttu-id="a7a93-133">**tevdef**</span><span class="sxs-lookup"><span data-stu-id="a7a93-133">**tevdef**</span></span>       | [<span data-ttu-id="a7a93-134">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="a7a93-134">**glTexEnv**</span></span>](gltexenv-functions.md)                                                                                                                                                                                                                                | <span data-ttu-id="a7a93-135">Define un entorno de asignación de texturas.</span><span class="sxs-lookup"><span data-stu-id="a7a93-135">Defines a texture-mapping environment.</span></span>                                                      |
| <span data-ttu-id="a7a93-136">**tevbind**</span><span class="sxs-lookup"><span data-stu-id="a7a93-136">**tevbind**</span></span>      | <span data-ttu-id="a7a93-137">**glTexEnv**[**glTexImage1D**](glteximage1d.md)</span><span class="sxs-lookup"><span data-stu-id="a7a93-137">**glTexEnv**[**glTexImage1D**](glteximage1d.md)</span></span><br/>                                                                                                                                                                                                           | <span data-ttu-id="a7a93-138">Selecciona un entorno de textura.</span><span class="sxs-lookup"><span data-stu-id="a7a93-138">Selects a texture environment.</span></span>                                                              |
| <span data-ttu-id="a7a93-139">**T2**</span><span class="sxs-lookup"><span data-stu-id="a7a93-139">**t2**</span></span>           | [<span data-ttu-id="a7a93-140">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="a7a93-140">**glTexCoord**</span></span>](gltexcoord-functions.md)                                                                                                                                                                                                                            | <span data-ttu-id="a7a93-141">Establece las coordenadas de textura actuales.</span><span class="sxs-lookup"><span data-stu-id="a7a93-141">Sets the current texture coordinates.</span></span>                                                       |
| <span data-ttu-id="a7a93-142">**texgen**</span><span class="sxs-lookup"><span data-stu-id="a7a93-142">**texgen**</span></span>       | <span data-ttu-id="a7a93-143">[**glTexGen**](gltexgen-functions.md)[**glGetTexParameter**](glgettexparameter.md)</span><span class="sxs-lookup"><span data-stu-id="a7a93-143">[**glTexGen**](gltexgen-functions.md)[**glGetTexParameter**](glgettexparameter.md)</span></span><br/> [<span data-ttu-id="a7a93-144">**gluBuild1DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="a7a93-144">**gluBuild1DMipmaps**</span></span>](glubuild1dmipmaps.md)<br/> [<span data-ttu-id="a7a93-145">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="a7a93-145">**gluBuild2DMipmaps**</span></span>](glubuild2dmipmaps.md)<br/> [<span data-ttu-id="a7a93-146">**gluScaleImage**</span><span class="sxs-lookup"><span data-stu-id="a7a93-146">**gluScaleImage**</span></span>](gluscaleimage.md)<br/> | <span data-ttu-id="a7a93-147">Controla la generación de coordenadas de textura. Escala una imagen a un tamaño arbitrario.</span><span class="sxs-lookup"><span data-stu-id="a7a93-147">Controls generation of texture coordinates.Scales an image to an arbitrary size.</span></span><br/> |



 

<span data-ttu-id="a7a93-148">Para obtener más información sobre la texturización, vea la *Guía de programación de OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="a7a93-148">For more information on texturing, see the *OpenGL Programming Guide*.</span></span>

<span data-ttu-id="a7a93-149">En este tema se incluye información sobre lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="a7a93-149">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="a7a93-150">Traducción de tevdef</span><span class="sxs-lookup"><span data-stu-id="a7a93-150">Translating tevdef</span></span>](translating-tevdef.md)
-   [<span data-ttu-id="a7a93-151">Traducción de texdef</span><span class="sxs-lookup"><span data-stu-id="a7a93-151">Translating texdef</span></span>](translating-texdef.md)
-   [<span data-ttu-id="a7a93-152">Traducción de texgen</span><span class="sxs-lookup"><span data-stu-id="a7a93-152">Translating texgen</span></span>](translating-texgen.md)

 

 





