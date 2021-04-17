---
title: Traducción de texgen
description: La función de GL de IRIS texgen se traduce en glTexGen para OpenGL.
ms.assetid: ddf398ed-37d4-4fb6-97be-20fe0564cb77
keywords:
- Migración de la contabilidad de IRIS, textura
- portabilidad de IRIS GL, textura
- trasladar a OpenGL desde IRIS GL, textura
- Exportación de OpenGL desde IRIS GL, textura
- textura
- Migración de la contabilidad de IRIS, texgen
- portabilidad de IRIS GL, texgen
- migración a OpenGL desde IRIS GL, texgen
- Exportación de OpenGL desde IRIS GL, texgen
- texgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07654fc35e20096ed71c3fe74ff9279214eb45c8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665727"
---
# <a name="translating-texgen"></a><span data-ttu-id="88262-113">Traducción de texgen</span><span class="sxs-lookup"><span data-stu-id="88262-113">Translating texgen</span></span>

<span data-ttu-id="88262-114">La función de GL de IRIS **texgen** se traduce en [glTexGen](gltexgen-functions.md) para OpenGL.</span><span class="sxs-lookup"><span data-stu-id="88262-114">The IRIS GL function **texgen** is translated to [glTexGen](gltexgen-functions.md) for OpenGL.</span></span>

<span data-ttu-id="88262-115">Con IRIS GL, se llama a **texgen** dos veces: una vez para establecer la ecuación de modo y plano simultáneamente, y otra para habilitar la generación de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="88262-115">With IRIS GL, you call **texgen** twice: once to set the mode and plane equation simultaneously, and once to enable texture-coordinate generation.</span></span> <span data-ttu-id="88262-116">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="88262-116">For example:</span></span>


```C++
texgen(TX_S, TG_LINEAR, planeParams); 
texgen(TX_S, TG_ON, NULL);
```



<span data-ttu-id="88262-117">Con OpenGL, realiza tres llamadas: dos a **glTexGen** (una vez para establecer el modo y otra para establecer la ecuación de plano) y una a [**glEnable**](glenable.md).</span><span class="sxs-lookup"><span data-stu-id="88262-117">With OpenGL, you make three calls: two to **glTexGen** (once to set the mode and once to set the plane equation), and one to [**glEnable**](glenable.md).</span></span> <span data-ttu-id="88262-118">Por ejemplo, el equivalente de OpenGL al código de GL de IRIS anterior es:</span><span class="sxs-lookup"><span data-stu-id="88262-118">For example, the OpenGL equivalent to the IRIS GL code above is:</span></span>


```C++
glTexGen(GL_S, GLTEXTURE_GEN_MODE, modeName); 
glTextGen(GL_S, GL_OBJECT_PLANE, planeParameters); 
glEnable(GL_TEXTURE_GEN_S);
```



<span data-ttu-id="88262-119">En la tabla siguiente se enumeran los nombres de coordenadas de textura del IRIS y sus equivalentes de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="88262-119">The following table lists the IRIS GL texture-coordinate names and their OpenGL equivalents.</span></span>



| <span data-ttu-id="88262-120">Coordenada de textura de la contabilidad de IRIS</span><span class="sxs-lookup"><span data-stu-id="88262-120">IRIS GL texture coordinate</span></span> | <span data-ttu-id="88262-121">Coordenadas de textura de OpenGL</span><span class="sxs-lookup"><span data-stu-id="88262-121">OpenGL texture coordinate</span></span> | <span data-ttu-id="88262-122">argumento glEnable</span><span class="sxs-lookup"><span data-stu-id="88262-122">glEnable argument</span></span>   |
|----------------------------|---------------------------|---------------------|
| <span data-ttu-id="88262-123">TX \_ S</span><span class="sxs-lookup"><span data-stu-id="88262-123">TX\_S</span></span>                      | <span data-ttu-id="88262-124">GL \_ S</span><span class="sxs-lookup"><span data-stu-id="88262-124">GL\_S</span></span>                     | <span data-ttu-id="88262-125">GL \_ Texture \_ gen \_ S</span><span class="sxs-lookup"><span data-stu-id="88262-125">GL\_TEXTURE\_GEN\_S</span></span> |
| <span data-ttu-id="88262-126">TX \_ T</span><span class="sxs-lookup"><span data-stu-id="88262-126">TX\_T</span></span>                      | <span data-ttu-id="88262-127">GL \_ T</span><span class="sxs-lookup"><span data-stu-id="88262-127">GL\_T</span></span>                     | <span data-ttu-id="88262-128">GL \_ Texture \_ gen \_ T</span><span class="sxs-lookup"><span data-stu-id="88262-128">GL\_TEXTURE\_GEN\_T</span></span> |
| <span data-ttu-id="88262-129">TRANSMISIÓN \_ R</span><span class="sxs-lookup"><span data-stu-id="88262-129">TX\_R</span></span>                      | <span data-ttu-id="88262-130">GL \_ R</span><span class="sxs-lookup"><span data-stu-id="88262-130">GL\_R</span></span>                     | <span data-ttu-id="88262-131">GL \_ Texture \_ gen \_ R</span><span class="sxs-lookup"><span data-stu-id="88262-131">GL\_TEXTURE\_GEN\_R</span></span> |
| <span data-ttu-id="88262-132">TX \_ Q</span><span class="sxs-lookup"><span data-stu-id="88262-132">TX\_Q</span></span>                      | <span data-ttu-id="88262-133">libro \_ de contabilidad</span><span class="sxs-lookup"><span data-stu-id="88262-133">GL\_Q</span></span>                     | <span data-ttu-id="88262-134">GL \_ Texture \_ gen \_ p</span><span class="sxs-lookup"><span data-stu-id="88262-134">GL\_TEXTURE\_GEN\_Q</span></span> |



 

<span data-ttu-id="88262-135">En la tabla siguiente se enumeran los modos de generación de texturas de IRIS GL y sus nombres de plano y modos de textura OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="88262-135">The following table lists the IRIS GL texture-generation modes and their equivalent OpenGL texture modes and plane names.</span></span>



| <span data-ttu-id="88262-136">Modo de textura de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="88262-136">IRIS GL texture mode</span></span> | <span data-ttu-id="88262-137">Modo de textura de OpenGL</span><span class="sxs-lookup"><span data-stu-id="88262-137">OpenGL texture mode</span></span> | <span data-ttu-id="88262-138">Nombre del plano OpenGL</span><span class="sxs-lookup"><span data-stu-id="88262-138">OpenGL plane name</span></span> |
|----------------------|---------------------|-------------------|
| <span data-ttu-id="88262-139">TG \_ lineal</span><span class="sxs-lookup"><span data-stu-id="88262-139">TG\_LINEAR</span></span>           | <span data-ttu-id="88262-140">\_objeto GL \_ lineal</span><span class="sxs-lookup"><span data-stu-id="88262-140">GL\_OBJECT\_LINEAR</span></span>  | <span data-ttu-id="88262-141">\_plano del objeto GL \_</span><span class="sxs-lookup"><span data-stu-id="88262-141">GL\_OBJECT\_PLANE</span></span> |
| <span data-ttu-id="88262-142">Perfil de TG \_</span><span class="sxs-lookup"><span data-stu-id="88262-142">TG\_CONTOUR</span></span>          | <span data-ttu-id="88262-143">\_ojo \_ lineal de contabilidad</span><span class="sxs-lookup"><span data-stu-id="88262-143">GL\_EYE\_LINEAR</span></span>     | <span data-ttu-id="88262-144">\_plano de ojo de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="88262-144">GL\_EYE\_PLANE</span></span>    |
| <span data-ttu-id="88262-145">\_SPHEREMAP TG</span><span class="sxs-lookup"><span data-stu-id="88262-145">TG\_SPHEREMAP</span></span>        | <span data-ttu-id="88262-146">\_mapa de esfera de GL \_</span><span class="sxs-lookup"><span data-stu-id="88262-146">GL\_SPHERE\_MAP</span></span>     |                   |



 

 

 




